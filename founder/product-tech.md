# Product & system design

Not part of the standard founder pack. It's here because the founder builds the software himself, and the software is the part he hopes to license later. Costs per message, model and hosting are in `research/business-model.md`.

## The design principle: the receipts are the price database

The founder's plan has an AI agent scraping supermarket websites to compare prices. Most Lebanese supermarkets' terms do not allow automated scraping (`research/suppliers.md` has the details), and scraped online prices often differ from shelf prices anyway. There is a better and fully legal data source: **every run produces receipts.** Photograph every receipt, OCR it, and every line updates `price_observations` with the real price paid, at the real store, on the real day. After 4–6 weeks of runs this beats any scraper on the ~150 SKUs that make up most village baskets. Add each store's weekly flyer (published on Instagram/Facebook) as a second source, entered by hand or parsed from the image.

## The daily cycle the software must run

```
06:00–14:00  INTAKE      WhatsApp text / voice note / photo of a handwritten list
                          -> parser -> canonical items -> quote sent back -> customer confirms
14:00        CUT-OFF     orders lock; late orders roll to tomorrow
14:05        BATCH       sum quantities per canonical SKU across all orders
14:10        PLAN        assign each SKU to a store (price + promo + stop cost) -> per-store pick lists
14:30–17:30  RUN         driver PWA: pick list by store/aisle, tick items, flag out-of-stock,
                          pick substitutions by pre-agreed rule, photo of each receipt
17:30–18:30  PACK        per-customer bag list, label/QR per bag, reconcile receipts vs plan
18:30–20:30  PICKUP      pickup-point check-off (scan QR or tick), take cash/wallet payment
20:30        CLOSE       ledger: revenue, cost of goods, fee, cash on hand per driver; savings report
```

## Components

| component | first version (week 0–2) | later |
| --- | --- | --- |
| Intake | WhatsApp Business **app** (free) on the business phone; owner forwards/pastes the list into the dashboard | WhatsApp **Cloud API** webhook; voice notes -> speech-to-text; photos of lists -> vision OCR |
| Parser | LLM call: free text in Lebanese Arabic / Arabizi / French / English -> `[{item, qty, unit, brand_pref, notes}]`, matched to the canonical catalogue by embedding + fuzzy match; owner confirms low-confidence lines | auto-confirm high-confidence lines; learn each customer's usual brands |
| Catalogue | ~150 canonical SKUs (the top items), each linked to `store_products` at 3–6 stores | grows from receipts |
| Quote | "Your basket: 14 items, max $38.40 incl. fee, pickup 7 p.m. at the church square. Reply 1 to confirm" | the price is a **guaranteed ceiling**: the customer never pays more than quoted |
| Planner | rules: buy at the store with the lowest last-observed price unless the difference is < the cost of an extra stop; apply multi-buy promos to pooled quantities | a small integer program (store selection + promo thresholds + stop cost), solvable in milliseconds for this size |
| Driver view | mobile PWA, works offline: per-store list sorted by aisle, tick, out-of-stock, substitute, receipt photo | live sync to the dashboard |
| Packing & pickup | printed bag labels with name + QR; check-off list per pickup point | customer gets "your bag is ready" message automatically |
| Payments | cash or wallet transfer (Whish/OMT) at pickup, logged per bag | prepaid wallet balance / subscription billing |
| Dashboard | orders, batch, plan, receipts vs plan, cash per driver, savings per customer, margin per run | multi-village view; per-tenant view for licensees |

## Data model (Postgres)

```
tenants(id, name)                                -- one per village operator; RLS on tenant_id from day 1
villages(id, tenant_id, name)
pickup_points(id, village_id, name, host, hours)
customers(id, tenant_id, phone, name, village_id, default_pickup_id, brand_prefs jsonb, sub_rules jsonb)
products(id, canonical_name, category, unit, size)              -- canonical catalogue
stores(id, name, branch, lat, lng)
store_products(id, store_id, product_id, sku_label, pack_size)
price_observations(id, store_product_id, price_usd, promo jsonb, source enum(receipt,flyer,manual,web), observed_at)
promos(id, store_id, rule jsonb, valid_from, valid_to)          -- e.g. {"type":"n_for","n":3,"price":5.00,"products":[...]}
orders(id, customer_id, run_date, status, quoted_total, raw_message, channel)
order_items(id, order_id, product_id, qty, quoted_unit_price, confidence, substitution_rule)
runs(id, tenant_id, run_date, driver_id, status)
run_assignments(id, run_id, store_id, product_id, qty, planned_unit_price)
purchases(id, run_id, store_id, receipt_photo_url, total_usd)
purchase_lines(id, purchase_id, product_id, qty, unit_price_paid)  -- feeds price_observations
bags(id, order_id, label_code, packed_at, collected_at)
payments(id, order_id, method enum(cash_usd,cash_lbp,whish,omt,card), amount_usd, received_by)
```

## How pooled promo savings are allocated (decide this before launch)

A "3 for $5" deal bought across three households has to be split. Three honest rules, pick one and publish it:

1. **Customer price = the store's normal shelf price, minus a fixed discount; the promo gain is the business's margin.** Simplest. Transparent if stated ("you pay at most the shelf price; we keep the bulk savings, that is how we earn").
2. **Pro-rata**: the promo price is shared equally; the business charges a visible fee instead.
3. **Split the saving**: the customer gets half of every saving below the reference shelf price, the business keeps half ("you always save, and we only earn when you save").

The CFO numbers model rule 3 as the base case (`numbers.json` notes). Whatever the rule, the quote is a **ceiling**: if the run comes in cheaper, the customer pays the lower amount, minus the business's share.

## Build order (each step usable on its own)

1. **Week 0, no code**: WhatsApp Business app + a Google Sheet as the order book + a printed pick list. Run 2–3 real batches by hand. This *is* the launch test in `launch.md`.
2. **Week 1–3**: dashboard + parser + catalogue + driver PWA. Next.js + Supabase (Postgres, auth, row-level security per tenant) or the founder's own preferred stack.
3. **Week 4–6**: receipt OCR -> price observations; planner with stop cost; automatic quote messages.
4. **Month 3+**: Cloud API intake with voice notes; savings report per customer ("you saved $11.20 this month"); only then the multi-tenant admin for a second village.

## What NOT to build yet

- Scrapers for supermarket websites (ToS risk, and receipts do the job better).
- A customer app. Villagers already have WhatsApp; an app is friction.
- Door-to-door routing. Pickup points are the whole cost advantage.
- A licensing portal. Sell the second village by hand first.
