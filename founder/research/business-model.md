# Business model research: Village Basket (Amchit group-buying grocery run)

Prepared 2026-11-17 for the founder board, the CFO and the pricing panel. Public sources only. Every fact has a link and a date. A page with no date of its own is marked "accessed 2026-11-17".

**Conventions**
- **[E]** marks an estimate I worked out. The arithmetic is shown next to it, and every input is either sourced or labelled as an assumption.
- "Unverified" means the only source is a blog, a vendor or a single secondary report.
- Currency: USD unless stated. MoET's own 30 March 2026 price file uses 1 USD = 89,700 LBP ([MoET weekly basket, 30-03-2026](https://www.economy.gov.lb/media/15131/weekly-basket-report30-03-2026.xlsx)). Spinneys Lebanon's site showed the same rate on 2026-11-17 ([spinneyslebanon.com](https://www.spinneyslebanon.com/)). EUR to USD uses the ECB reference rate of 1.1127 for 11 Nov 2026 ([Banca d'Italia copy of the ECB rates](https://www.bancaditalia.it/compiti/operazioni-cambi/cambio/cambi_rif_20261111)).
- Naming: the brief says "Tawfir Shop". The Lebanese soft-discount chain I found publishes as **Tawfeer** ("Tawfeer LB" app, which lists promotions and delivery slots: [App Store, accessed 2026-11-17](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055)). The founder should confirm it is the same store.

---

## 0. Summary for the panel

1. **The market punishes hidden margins and rewards visible savings.** Lebanon is poor, cash-based and facing high food inflation (figures in §1.0). The best-documented complaint about grocery platforms is fees and prices that are not shown clearly. The FTC alleged that Instacart's service fees "add as much as 15% to the order cost and were not clearly disclosed" ([FTC, 18 Dec 2025](https://www.ftc.gov/node/327255)).
2. **The models that fit best are, in order:**
   - **(c) a flat, visible fee per bag or per order.** It is simple to explain and easy to collect in cash.
   - **(f/g) a share-of-savings fee or hybrid, shown against a published reference price.** It is the only model that charges in proportion to the core promise ("cheaper than driving down"). I found no grocery company that uses it. Bill negotiators charge 25–60% of savings.
   - **(d) a low monthly membership for regulars**, once weekly habits exist.
   - A **supplier rebate (e)** is a bonus if Tawfeer agrees. It should not be the base of the model.
   - **A markup baked into prices (a)** is the most profitable in theory. It also conflicts directly with a price-comparison promise.
3. **Lessons from group buying.** Next-day pickup at existing shops, a limited range and local density worked. Subsidies, heavy warehouses and fresh-produce spoilage killed most players. Platform gross margins were about 15% ([TechBuzz China, 16 Feb 2024](https://techbuzzchina.substack.com/p/community-group-buying-the-us-military)). CityMall's founders: "No two people will ever ask for the same product at the same time" ([Inc42, 17 Sep 2025](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/)). That is a direct warning for a plan that depends on hitting multi-buy thresholds.
4. **SaaS benchmarks.**
   - WhatsApp CRM tools: about $50–$350 a month.
   - Delivery/dispatch SaaS: free up to roughly 100–300 orders, then $29–$499 a month plus $0.03–$0.25 per extra order.
   - White-label licences: $15k–$75k one-time (vendor estimate).
   - Small-business SaaS loses about 4% of customers a month, roughly 39% a year (CRV, June 2026).
5. **Tech cost [E].** About **$13 / $16 / $49 a month** at 50 / 200 / 1,000 orders on a lean stack: Cloud API direct, Claude Sonnet 5.5 parsing, a small VPS. About **$106–$142 a month** on off-the-shelf managed tools. Details in §4.6.
6. **WhatsApp pricing changed on 1 Oct 2026.** Replies inside the 24-hour window ("service" messages) are now charged after 1,000 free per number per month, at $0.0091 per message for Lebanon (Meta rate card, effective 1 Oct 2026). Older articles saying service replies are free are out of date.

---

## 1. Monetisation models, with evidence

### 1.0 Market facts that constrain any model

| Fact | Figure | Source (date) |
|---|---|---|
| Monetary poverty, Lebanon | 44% of residents in 2022 (12% in 2012). 33% among Lebanese, 87% among Syrians. From 2% in Beirut to 62% in Akkar | [World Bank, 23 May 2024](https://www.worldbank.org/en/news/press-release/2024/05/23/lebanon-poverty-more-than-triples-over-the-last-decade-reaching-44-under-a-protracted-crisis) |
| Dollarised cash economy | $9.9bn, 45.7% of GDP, in 2022 (26.2% in 2021) | [World Bank, 16 May 2023](https://www.worldbank.org/en/news/press-release/2023/05/16/lebanon-normalization-of-crisis-is-no-road-to-stabilization) |
| Food inflation | 18% year on year, June 2026 | [FAO GIEWS country brief (accessed 2026-11-17)](https://cb.apps.fao.org/country.jsp?code=LBN) |
| Household stress | 38.2% of 2,400 respondents cut spending on essentials (LCPS survey, Jan 2026). Headline inflation 12.2% in early 2026. About 85% of consumption is imported | [LCPS, 21 Jul 2026](https://www.lcps-lebanon.org/en/articles/details/6050/lebanons-cost-of-living-crisis-beyond-monitoring-and-enforcement-of-essential-food-prices) |
| Food insecurity | 1.24 million people expected at IPC Phase 3 or worse, Apr–Aug 2026. Vegetable prices +20% and bread +17% since 2 Mar 2026 | [WFP via GlobalSecurity, Apr 2026](https://www.globalsecurity.org/military/library/news/2026/04/mil-260429-wfp01.htm) |
| Digital wallets | Whish's CEO claims about 90% of Lebanon's local digital transaction market (self-reported, unverified) | [L'Orient Today interview (accessed 2026-11-17)](https://today.lorientlejour.com/article/1450086/whish-money-pioneer-of-digital-transactions-and-global-fintech-integration.html) |

**What this means for pricing.** Fees should be small, fixed or capped, payable in USD cash or by wallet, and shown separately. The buyer is in a market where people already cut essentials, so a fee only makes sense if the savings visibly exceed it.

### 1.1 (a) Markup baked into item prices

**Evidence**
- **Community group-buying platforms earn mainly by reselling goods.**
  - Overall community group-buying gross margin was about 15%. Front-warehouse grocers made about 30%. Meituan Select was at 14.9% (May–June 2023) and needed about 17% to be profitable ([TechBuzz China, 16 Feb 2024](https://techbuzzchina.substack.com/p/community-group-buying-the-us-military)).
  - At CityMall (India), regional brands earn 20–25% margin and private labels nearly 40% ([Inc42, 17 Sep 2025](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/)).
  - CityMall charges no handling or delivery fees, so all of its revenue is margin on goods ([TechCrunch, 1 Sep 2025](https://techcrunch.com/2025/09/01/indian-grocery-startup-citymall-raises-47m-to-challenge-ultra-fast-delivery-giants/)).
- **On Instacart, retailers set the prices and can make them higher than in store.**
  - A study of 437 shoppers by Consumer Reports and Groundwork found the same item shown at different prices. The average spread between lowest and highest price was 13%, up to 23%, and identical baskets differed by about 7% ([Groundwork report, Dec 2025](https://groundworkcollaborative.org/wp-content/uploads/2025/12/Same-Cart-Different-Price.pdf)).
  - Instacart then ended all item price tests ([CTV News, Dec 2025](https://www.ctvnews.ca/business/article/instacart-ends-ai-driven-price-experiments-after-criticism/)).

**Pros**
- No fee line to argue about.
- Works with cash.
- Captures the multi-buy discount: buy 3 at the bundle price, resell each at the single price.

**Cons for this market**
- It contradicts the price-comparison promise. If residents compare shelf prices (and Lebanese consumers have tools for this, see §5), any undisclosed markup turns into a trust problem.
- Margin is exposed to price changes between ordering and buying.

**What customers dislike.** Different or hidden prices for the same item (the Groundwork study above).

### 1.2 (b) Service fee as a % of the basket

**Evidence**
- **Instacart.**
  - The service fee "varies and is subject to change based on factors like location, weather, and the number and types of items in your cart". Instacart pickup orders "don't have service fees" ([Instacart Help, accessed 2026-11-17](https://www.instacart.com/help/article/service-fee)).
  - The FTC alleged the fee adds "as much as 15% to the order cost" and that "free delivery" was misleading because of it. Instacart agreed to $60M in refunds and denies wrongdoing ([FTC, 18 Dec 2025](https://www.ftc.gov/node/327255)).
  - Secondary sources put the usual rate at about 5–10% (unverified; Instacart publishes no rate).
- **Dumpling (independent personal shoppers, US).** Its recommended default is **15% of the grocery total with a $15 minimum**. It recommends percentage pricing so that shoppers "make enough money to cover your time and expenses" without relying on tips ([Dumpling Help, 12 Mar 2026](https://help.dumpling.us/en/articles/3800535-how-should-i-price-my-services)).

**Pros**
- Scales with effort and basket size.
- Familiar from delivery apps.

**Cons for this market**
- It penalises big family baskets, which are the very customers who benefit most from pooling.
- It looks like a tax on the price, and the fee rises when prices rise (food inflation is 18%).
- Without a cap it is hard to quote before shopping.

**What customers dislike.** Fees that vary, have no stated rule, or are not clearly shown (FTC allegation above).

### 1.3 (c) Flat per-order, per-bag or pickup fee

**Evidence**
- **Sprouts (via Instacart):** $3.99 pickup fee on orders under $35, none above ([Sprouts, accessed 2026-11-17](https://www.sprouts.com/pricing)).
- **Walmart:** a fee of about $6.99 on delivery orders under $35, per consumer sites ([Clark.com, accessed 2026-11-17](https://clark.com/shopping-retail/walmart-plus/); [ThePricer, accessed 2026-11-17](https://www.thepricer.org/how-much-does-walmart-grocery-delivery-cost/)). Unverified on walmart.com, which blocked automated access.
- **Flashfood:** a variable fee capped at $2.99 per order ([MoneyPantry review, accessed 2026-11-17](https://www.moneypantry.com/flashfood-review/)).
- **Wakilni (Lebanese courier), the local price anchor:**
  - $6 per delivery for all areas of Lebanon.
  - $3 return fee.
  - 2.5% surcharge for card payment on delivery.
  - $12 annual fee per business account from 1 Jul 2025 ([Wakilni proposal, accessed 2026-11-17](https://wiki.wakilni.com/quotations/fresh-beirut-proposal)).

**Pros**
- Easiest to explain and collect in cash.
- Predictable for the household.
- Covers the fixed cost of the driver run.

**Cons**
- Regressive for small baskets: a $2 fee on a $10 basket is 20%.
- Revenue does not grow with basket size.
- A minimum basket or a tiered fee (per bag) is usually needed.

**What customers dislike.** Below-minimum surcharges that only appear at checkout (the Walmart and Sprouts thresholds above).

### 1.4 (d) Monthly subscription or membership

**Evidence**
- **Instacart+:**
  - $9.99 a month or $99 a year.
  - $0 delivery fee on grocery orders of $10 or more.
  - "Service fees apply" ([Instacart+, accessed 2026-11-17](https://www.instacart.com/plus)).
  - The FTC alleged that free trials converted to paid memberships without clear consent ([FTC, 18 Dec 2025](https://www.ftc.gov/node/327255)).
- **Walmart+:** $98 a year or $12.95 a month, with free delivery on orders of $35 or more ([Clark.com, accessed 2026-11-17](https://clark.com/shopping-retail/walmart-plus/)). Secondary source.
- **talabat tPro, Jordan (nearest comparable market found):** JOD 3 a month or JOD 30 a year ([Jordan News, undated](https://www.jordannews.jo/Section-113/All/talabat-Jordan-launches-tPro-30437)).
- **Toters (Lebanon):** I found **no public subscription**. Toters' site mentions card or cash payment but no membership or fees ([totersapp.com, accessed 2026-11-17](https://totersapp.com/)).

**Pros**
- Recurring, predictable revenue.
- Rewards loyalty.
- Matches the founder's original idea.

**Cons for this market**
- A monthly charge is a commitment many households cut first in a crisis.
- Collecting cash every month is a hassle.
- It only pays off for people who order weekly.
- Customers dislike automatic renewals and trial conversions (FTC case above).

### 1.5 (e) Supplier-side commission or rebate

**Evidence: how community group-buying leaders were paid**

| Platform | Leader commission | Source (date) |
|---|---|---|
| Meituan Select (Youxuan) | 6.4% lowered to 6.3% (Q2 2023) | [TechBuzz China, 16 Feb 2024](https://techbuzzchina.substack.com/p/community-group-buying-the-us-military) |
| Meituan Select | 6.5–7%; about 6% called "healthy" | [TechBuzz China, 29 Apr 2023](https://techbuzzchina.substack.com/p/reports-about-the-death-of-community) |
| Duoduo Maicai (Pinduoduo) | about 4–4.05% (the same piece also gives 3.5%) | same, 29 Apr 2023 |
| Xingsheng Youxuan | 8.3% | same, 29 Apr 2023 |
| Industry | fell from about 20% to 5–10% by mid-2022 | same, 29 Apr 2023 |
| CityMall (India) | INR 10,000 monthly payout per leader. About 20,000 leaders served about 200,000 customers (end-2021) | [Inc42, 17 Sep 2025](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/) |

**Platform-side supplier money**
- Duoduo Maicai, the survivor, earns mainly from **merchant fees** (technology service, placement and campaign fees). Merchant funding became its main profit source once subsidies fell ([KrASIA, 23 Jul 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)).
- Instacart's "advertising and other" revenue was $1.065bn in FY2025, about 28.5% of its $3.742bn revenue ([Sacra, accessed 2026-11-17](https://sacra.com/research/instacart)). Earnings coverage put it at about 2.9% of GTV ([itiger / Dow Jones, Feb 2026](https://www.itiger.com/news/2611497092)); that figure is secondary.
- US hospital group purchasing organisations are paid an administrative fee by vendors, conventionally 3% or less of the purchase price, under the safe harbour at 42 CFR 1001.952(j) ([CASRAI guide, accessed 2026-11-17](https://casrai.org/guides/gpo-safe-harbor)).
- In Lebanon, delivery apps reportedly take 22–30% commission from merchants ([Voxire blog, undated, unverified](https://voxire.pages.dev/blog/delivery-apps-lebanese-stores-2026/)).

**Pros**
- No fee for residents.
- Fits the "direct supplier relationship" the founder wants with Tawfeer.

**Cons**
- It depends on one supplier's goodwill, and at tiny volumes (50–200 orders a month) a supermarket has little reason to pay.
- If undisclosed, it creates a conflict of interest with the "AI picks the cheapest store" promise.
- Supplier-funded profit only worked at Duoduo's scale.

### 1.6 (f) Share of savings (fee = % of measured savings against a reference price)

**Real examples (none in grocery)**

| Example | Fee | Source (date) |
|---|---|---|
| Rocket Money bill negotiation | 35–60% of first-year savings, chosen by the user. Nothing charged if no savings | [Rocket Money Help (accessed 2026-11-17)](https://help.rocketmoney.com/en/articles/9744474-bill-negotiation-charge) |
| BillShark | 40% of savings, capped at 2 years. No savings, no fee | [BillShark FAQ (accessed 2026-11-17)](https://billshark.freshdesk.com/support/solutions/articles/6000044197-how-much-does-it-cost-) |
| Paribus (price-drop refunds) | 25% of refunds obtained | [Good Morning America, c. 2019](https://www.goodmorningamerica.com/news/story/apps-find-refunds-purchase-47652404) |
| Earny (launch model) | 25% cut of refunds; later reported to have moved to a subscription | [TechCrunch, 6 May 2016](https://techcrunch.com/2016/05/06/earnys-app-gets-your-money-back-on-purchases-after-prices-drop) |
| Procurement "gainshare" consultants | from "10% or more" up to 50% of achieved savings | [TrinityP3 (accessed 2026-11-17)](https://www.trinityp3.com/?p=1869); [Education Business UK (accessed 2026-11-17)](https://www.educationbusinessuk.net/node/9689) |

**Grocery.** I found **no grocery service that charges a share of savings**; the searches returned only fees on order totals. This would be a new model, which is a risk and possibly a story.

**Reference price options in Lebanon**
1. **MoET weekly basket:** the official national average supermarket price for 60 items (see §5.3).
2. **The shelf price at the store the household would otherwise drive to**, recorded by the driver.
3. **The single-unit price before the multi-buy offer**, which measures the pooling discount itself.

**Pros**
- The only model where the fee is proven by the savings. It fits a price-sensitive buyer and the "share the savings" story.
- It can be shown on every receipt: "Shelf price $X, you paid $Y, you saved $Z, our fee is 30% of $Z".

**Cons**
- Disputes about the baseline: which store, which day, which brand.
- Revenue falls to zero when there are no deals.
- Encourages gaming the baseline.
- Contracts in the gainshare world must define baseline, scope and verification ([TrinityP3](https://www.trinityp3.com/?p=1869)).
- Needs a minimum fee to cover the driver on low-saving days.

### 1.7 (g) Hybrids, as real operators use them

- **Instacart stacks everything:** a delivery fee (waived for members on $10+ orders), a service fee, retailer-set prices, ads and membership (sources above). The stacking is exactly what the FTC targeted.
- **Dumpling:** a percentage with a $15 minimum ([Dumpling, 12 Mar 2026](https://help.dumpling.us/en/articles/3800535-how-should-i-price-my-services)).
- **Zoko (software):** a subscription plus a per-conversation markup on the Starter plan ([Zoko pricing, accessed 2026-11-17](https://www.zoko.io/pricing)).

**Hybrids for the panel to test.** These are design options, not evidence.
- H1: a flat fee per bag, plus a share of any savings above a threshold.
- H2: a monthly membership with a lower per-bag fee; non-members pay the full per-bag fee.
- H3: a share of savings with a minimum and a cap.
- H4: a flat fee, with any disclosed supplier rebate passed into lower prices.

### 1.8 Fee transparency: what customers say they dislike (all sourced above)

- Fees that are mandatory but advertised as "free" (FTC v Instacart, Dec 2025).
- Fees with no stated rule ("varies") (Instacart Help).
- Different prices for the same item for different people (Groundwork / Consumer Reports, Dec 2025).
- Subscriptions that start without clear consent (FTC).
- Refunds paid into wallets that expire instead of to the original payment method (DealShare users, [Inc42, 5 Aug 2023](https://inc42.com/features/dealshare-on-shaky-ground-ceo-vacuum-underscores-operational-mess/)).

### 1.9 Recommendation framework (for the panel and CFO to decide)

| If… | …the model that fits | Why |
|---|---|---|
| Pilot phase, fewer than about 50 households, savings not yet proven | **(c) flat fee per bag or order**, shown on a separate line, payable in cash or Whish | Simplest to explain and collect. Tests willingness to pay without arguments about a baseline |
| The driver can reliably record the "would-have-paid" shelf price, or MoET or a partner gives a credible reference | **(f) share of savings with a minimum** (H3), with savings printed on each receipt | Proves the value proposition every week. No grocery precedent, so test carefully |
| A core of households orders weekly | **(d) membership for regulars plus (c) for occasional users** (H2) | Recurring revenue only once habits exist |
| Tawfeer (or another store) agrees to a volume discount or rebate | **(e) as a bonus**, disclosed, never the only revenue | Volumes are too small to rely on, and an undisclosed rebate conflicts with "AI picks the cheapest" |
| The operator keeps multi-buy discounts instead of passing them on | This *is* model **(a)** and should be named as such | Pooled multi-buy savings belong either to residents or to the operator; decide this explicitly |
| A big basket would pay a disproportionate fee | Cap any % model | Avoids penalising the families who save the most |

**[E] Illustrative arithmetic only; the basket and savings figures are hypotheticals, not data.** For a $40 basket that saved $5 against the reference:

| Model | Calculation | Fee |
|---|---|---|
| (b) 5% of basket | 0.05 × 40 | $2.00 |
| (c) flat fee | per bag or order | $2.00 |
| (f) 30% of savings | 0.30 × 5 | $1.50 |
| (f) 40% of savings | 0.40 × 5 | $2.00 |

The CFO should replace these with real basket and savings data from the pilot.

---

## 2. Community group buying: unit economics and lessons

### 2.1 Unit economics benchmarks

| Platform (country) | Average order value (AOV) | Gross margin | Leader pay | Fulfilment / other | Status | Sources |
|---|---|---|---|---|---|---|
| Meituan Select / Youxuan (China) | RMB 11.6 (Q2 2023), RMB 12.2 (Q3 2023); about 3 items per order | 14.9% (May–Jun 2023); about 17% needed | 6.3–6.5% | Fulfilment 10% of revenue (Q2 2023); subsidies 4% of revenue; loss 5–6% | Closed in 18 provincial-level regions in Jun 2025; left Guangzhou 15 Dec 2025; "never overall profitable" | [TechBuzz China, Feb 2024](https://techbuzzchina.substack.com/p/community-group-buying-the-us-military); [KrASIA, 23 Jul 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| Meituan new initiatives segment | n/a | n/a | n/a | Lost ¥77.7bn in 2020–22; profit per order "under ¥1" | as above | [Pandaily, 25 Jun 2025](https://pro.pandaily.com/p/community-group-buyings-decline-how) |
| Duoduo Maicai (China) | Average item value ¥8 (2022) | 14–17% | about 4% | Spoilage under 5% vs about 8% industry average; operating costs about 15% below Meituan's | Survivor: 44% share (2024 report); first full-year profit in 2024 | [TechBuzz China, Apr 2023](https://techbuzzchina.substack.com/p/reports-about-the-death-of-community); [Pandaily](https://pro.pandaily.com/p/community-group-buyings-decline-how); [KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| Xingsheng Youxuan (China) | RMB 30 (2020); about RMB 10 (2023) | 23.1% (Sep 2022); about 20% | 8.3% | Net loss −2.9% (Sep 2022). About 280,000 leaders and 13,000 convenience stores (2020) | Retreated from 6 provinces by end-2021; 17% share (2024 report) | [TechBuzz China, Apr 2023](https://techbuzzchina.substack.com/p/reports-about-the-death-of-community); [KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| CityMall (India) | INR 450–500 (about $5–6) | 20–25% on regional brands; about 40% on private label | INR 10,000 a month; now fulfilment only | Delivery cost INR 50 per order (≈11% of AOV [E]: 50 / 450). EBITDA margin worse than −30% last financial year | Pivoted away from social commerce; FY25 GMV INR 768 Cr | [Inc42, 17 Sep 2025](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/); [TechCrunch, 1 Sep 2025](https://techcrunch.com/2025/09/01/indian-grocery-startup-citymall-raises-47m-to-challenge-ultra-fast-delivery-giants/) |
| DealShare (India) | n/a | "thin margins" | n/a | FY22 loss INR 431 Cr; FY23 loss INR 502.7 Cr | Shut Maharashtra and Hyderabad (2023); CEO exit; refocused on Delhi NCR and Rajasthan | [Inc42, 5 Aug 2023](https://inc42.com/features/dealshare-on-shaky-ground-ceo-vacuum-underscores-operational-mess/); [YourStory, Jan 2024](https://yourstory.com/2024/01/dealshare-wholesale-grocery-social-commerce-fy23-financials) |
| Super (Indonesia) | n/a | Private-label revenue and margins grew more than 4x in one year; exclusive brands lift margin 2–5x | Agents resell to neighbours (rates not disclosed) | More than 48,000 agents in 48 cities (2024) | No shutdown found; shifted toward private label and exclusive brands for margin | [Insignia podcast, 7 Jun 2024](https://review.insignia.vc/2024/06/07/call-165-superapp-nadira-zahiruddin-gisella-tjoanda-part-1/) |
| KitaBeli (Indonesia) | n/a | n/a | n/a | Raised a $10M Series A (2021) | Listed as "Bankrupt" by CB Insights; DailySocial reports liquidation (article could not be opened, headline only) | [CB Insights](https://www.cbinsights.com/investor/kitabeli); [DailySocial](https://en.dailysocial.id/post/social-commerce-we-buy-liquidation); [TechCrunch, 2021](https://techcrunch.com/?p=2129495) |

### 2.2 Why they shrank, closed or pivoted

- **Subsidy-funded growth stopped when regulators acted.**
  - China's "nine prohibitions" (Dec 2020) ended below-cost selling ([KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)). Pandaily dates the rules to March 2021 ([Pandaily](https://pro.pandaily.com/p/community-group-buyings-decline-how)).
  - Platforms sometimes gave up nearly all revenue on an order to subsidise leaders ([KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)).
- **Heavy assets and perishables.** Multi-layer warehouses, high fixed costs and produce spoilage ([Pandaily](https://pro.pandaily.com/p/community-group-buyings-decline-how)).
- **Centralised decisions** on pricing and subsidies hurt local flexibility. Purchase limits on resellers cut GMV ([KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)).
- **Demand rarely lines up for group discounts.** "No two people will ever ask for the same product at the same time" (CityMall founders). CityMall cut its reliance on WhatsApp order aggregation and moved to an app and private labels ([Inc42, 17 Sep 2025](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/)).
- **Leaders became a cost.** CityMall switched leaders to fulfilment only "to reduce costs" ([TechCrunch, 1 Sep 2025](https://techcrunch.com/2025/09/01/indian-grocery-startup-citymall-raises-47m-to-challenge-ultra-fast-delivery-giants/)).
- **Operations failures erode trust.** DealShare users reported auto-cancelled orders, refunds to an expiring wallet and tampered packages ([Inc42, 5 Aug 2023](https://inc42.com/features/dealshare-on-shaky-ground-ceo-vacuum-underscores-operational-mess/)).

### 2.3 What worked

- **Next-day pickup with a fixed cut-off.**
  - Meituan Select: order before 23:00, pick up the next day before 16:00 ([TechBuzz China, Apr 2023](https://techbuzzchina.substack.com/p/reports-about-the-death-of-community)). The pickup-window rules changed again in Aug 2023 ([TechBuzz China, Feb 2024](https://techbuzzchina.substack.com/p/community-group-buying-the-us-military)).
  - Taobao Maicai: order by 21:59, delivered by 12:00 the next day (same Feb 2024 source).
  - CityMall delivers "in a day rather than in minutes" (TechCrunch 2025).
  - This matches the founder's 2 p.m. cut-off.
- **Pickup points in existing shops.** Xingsheng ran on about 13,000 convenience stores and waived the leader deposit that rivals charged (about RMB 5,000) ([TechBuzz China, Apr 2023](https://techbuzzchina.substack.com/p/reports-about-the-death-of-community); [KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)). CityMall kept the leaders with "stronger local reach and larger storage capacity" ([Inc42](https://inc42.com/startups/citymall-left-turns-pivots-inr-1000-cr-revenue-club/)).
- **Regional density before expansion.** Xingsheng was near break-even in its home province of Hunan. Duoduo succeeded through warehouse density, lean staffing and merchant-funded margin ([KrASIA](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)).
- **A limited, value-focused range, with private label for margin.** CityMall carries about half a quick-commerce app's range and gets about 40% margin on private label. Super's private-label margins grew more than 4x (sources above).

### 2.4 What this means for Amchit (based on the evidence above, not new data)

- Gross margins of about 15% on goods were not enough at scale with subsidies. A village operation needs either an explicit fee or a margin on goods. It has no venture money to subsidise either.
- Multi-buy pooling is the core of the pitch, but CityMall's experience says baskets rarely overlap. Pilot data should measure **the share of basket value that actually hit a multi-buy threshold**.
- Spoilage was a killer in fresh produce, so shelf-stable goods are lower risk at the start.

---

## 3. SaaS and licensing angle

### 3.1 What comparable software charges small operators (accessed 2026-11-17 unless dated)

**WhatsApp commerce and CRM tools**

| Product | Tiers (per month) | Message fees | Source |
|---|---|---|---|
| WATI | Growth $59 (3 users), Pro $119 (5 users, +$39 per user), Business $279 (5 users, +$89 per user). Billed annually | Varies by category and country; "no setup fee" for the API | [wati.io/pricing](https://www.wati.io/pricing/) |
| respond.io | Starter $79 (annual) / $99 (monthly), Growth $159 / $199, Advanced $279 / $349 | "WhatsApp fees are not included" | [respond.io/pricing](https://respond.io/pricing) |
| Interakt | Growth $55, Advanced $69 (+ taxes); AI agent add-on $74.99 | Template charges extra; Enterprise has "No Markup Charges" | [interakt.shop/pricing](https://www.interakt.shop/pricing/) |
| Zoko | Starter $49.99 (+$0.015 markup per conversation), Plus $79.99, Elite $139.99 | Meta fees paid directly to Meta | [zoko.io/pricing](https://www.zoko.io/pricing) |
| 360dialog (provider for the WhatsApp API) | €49 / €99 / €500 per number per month (≈$54.52 for the €49 plan [E]: 49 × 1.1127) | "no markup on Meta fees" | [360dialog.com/pricing](https://360dialog.com/pricing) |
| Twilio | pay as you go | $0.005 per message in or out, plus Meta's fee | [twilio.com WhatsApp pricing](https://www.twilio.com/en-us/whatsapp/pricing) |

**White-label grocery and delivery platforms**

| Product | Model and tiers | Source |
|---|---|---|
| Shipday | Free (300 orders a month). Paid plans $29 / $49 / $99 / $199 / $399 a month. Extra orders $0.06–$0.25 each. The page's tables conflict on included orders | [shipday.com/pricing](https://www.shipday.com/pricing) |
| Tookan (JungleWorks) | Free (100 tasks, 2 agents). Startup $89 annual / $129 monthly (1,000 tasks). Growth $239 / $299 (3,000). Standard $389 / $499 (6,000). Extra tasks $0.03–$0.15 | [jungleworks.com/tookan/pricing](https://jungleworks.com/tookan/pricing/) |
| Yelo (JungleWorks) | Annual bundles of 12,000 / 18,000 / 24,000 orders, $0.10 per extra order. Plan prices "talk to sales" | [jungleworks.com/yelo/pricing](https://jungleworks.com/yelo/pricing/) |
| Enatega | One-time licence; price not public; frontend MIT-licensed on GitHub, backend proprietary | [GitHub](https://github.com/ninjas-code-official/food-delivery-singlevendor); vendor market estimate below |
| Market estimate (published by Enatega, a vendor) | SaaS $49–$400+ a month; one example setup fee of about $299; ready-made licence $15k–$75k; solo operators $50–$500 a month | [Enatega blog, 22 Oct 2026](https://enatega.com/white-label-delivery-software-cost/) |
| Zeew | No public price found; Capterra blocked access | [Capterra listing](https://www.capterra.com/p/218150/Zeew/) |

**POS and ERP for small grocers (MENA and global)**

| Product | Price | Source |
|---|---|---|
| Loyverse POS | Free core POS. Add-ons $7–$25 per month per store | [loyverse.com/pricing](https://www.loyverse.com/pricing) |
| Odoo | One app free. Standard $24.90 per user per month (the discount lasts 12 months; other figures shown are $31.10 and $38.90) | [odoo.com/pricing](https://www.odoo.com/pricing) |
| Zoho Inventory (UAE page) | Free (50 orders). $29 / $79 / $129 / $249 per month, billed annually | [zoho.com/ae/inventory/pricing](https://www.zoho.com/ae/inventory/pricing/) |
| Foodics (restaurants, MENA) | AED 199 / 375 / 556 per month, billed annually | [foodics.com/pricing](https://www.foodics.com/pricing/) |
| Shopify | Basic $39 monthly or $29 a month billed yearly; 2% fee when using a third-party payment provider | [shopify.com/pricing](https://www.shopify.com/pricing) |
| Lebanese POS sellers (OLX) | One-time bundles of about $199–$699 including "free software" | [OLX Lebanon](https://www.olx.com.lb/q-new-po/) |
| Lebanese chain example | Promarché adopted LS Central SaaS (enterprise level) | [LS Retail (accessed 2026-11-17)](https://www.lsretail.com/resources/promarche-becomes-the-first-supermarket-chain-in-lebanon-to-adopt-ls-central-in-saas) |

**Common pricing models**
- Monthly tiers by volume plus per-order overage (Shipday, Tookan, Yelo).
- Per-seat pricing (WATI, Odoo).
- A markup on message fees (Zoko Starter).
- A one-time licence plus maintenance; 15–20% of build cost a year is the vendor's rule of thumb (Enatega).
- Free tiers up to about 50–300 orders.

### 3.2 Who in Lebanon could buy it

| Buyer | Evidence | Ability to pay |
|---|---|---|
| Municipalities | 1,065 municipalities (Ministry of Interior, 2025). Some ran food relief drives and fuel distribution during the crisis ([Arab Reform Initiative, Sep 2025](https://www.arab-reform.net/publication/empowering-lebanons-municipalities-amid-crisis/)) | Weak. Transfers to municipalities for 2022 onward were still unpaid as of June 2025. One mayor said revenues covered less than half of staff salaries by 2024 (same source) |
| Cooperatives | About 850 registered with the General Directorate of Cooperatives. Records are "largely paper-based" and not fully updated since 2007; the ILO is digitising them ([ILO, 23 Sep 2026](https://www.ilo.org/resource/news/new-partnership-set-strengthen-lebanon%E2%80%99s-cooperative-sector-through-better)) | Unknown; often donor-funded (no data found) |
| Government or market monitors | Awfarli, a Lebanese price-comparison app, now powers a Ministry of Economy and Trade market-monitoring dashboard under an MoU ([Berytech, 20 Jul 2026](https://berytech.org/from-app-to-national-infrastructure-how-awfarli-grew-beyond-its-own-vision/)) | A precedent that **price data**, not just software, can be sold to the state |
| Village entrepreneurs, mini-markets, parish or church committees | **No public data found** on their number or software spending. This is a hypothesis to test in interviews | Unknown |

### 3.3 Honest note on selling SaaS to micro-operators

- **Churn.** Small-business SaaS (about $500–$5,000 in annual contract value) loses about **4.1% of customers a month, roughly 39% a year** ([CRV, 19 Jun 2026](https://crv.com/content/saas-churn-rate)). Micro-operators in a crisis economy are likely to be worse; that is an inference, not data.
- **Ability to pay.** Municipalities lack cash (§3.2). The comparable tools above cost $29–$279 a month, which may exceed a village operator's monthly profit. The CFO should check this against the unit economics.
- **The founder becomes support.** A white-label buyer needs onboarding, WhatsApp number setup with Meta, and training. Vendors charge for this separately: WATI and respond.io sell dedicated onboarding as an add-on (sources above).
- **What tends to fit low ability to pay:** a free tier, per-order or revenue-share pricing that grows with use (Shipday or Tookan style), and a paid setup package. The evidence for this is the pricing pages above; it is not proof of demand.

---

## 4. Tech costs to run it

### 4.1 WhatsApp Business app (free)

- **Broadcast lists:**
  - Up to 256 contacts per list; unlimited lists.
  - Recipients must have saved the business's number.
  - Mobile only.
  - "People in some countries might see a monthly broadcast limit" ([WhatsApp Help, accessed 2026-11-17](https://faq.whatsapp.com/861663048350950/)).
- **Catalogue:** up to 500 items, each with up to 10 photos or videos ([WhatsApp Business, accessed 2026-11-17](https://whatsappbusiness.com/resources/resource-library/whatsapp-business-app-resources/whatsapp-business-catalog)).
- **Devices:** up to four linked devices ([WhatsApp Help, accessed 2026-11-17](https://faq.whatsapp.com/378279804439436)).
- **Automation is not allowed on the free app.** The Terms ban "bulk messaging, auto-messaging, auto-dialing" and creating accounts "through unauthorized or automated means" ([WhatsApp Terms, effective 4 Jan 2021](https://www.whatsapp.com/legal/terms-of-service)). An unofficial bot built on the free app risks a ban, so automated parsing needs either manual copy-paste or the Cloud API.

### 4.2 WhatsApp Business Platform (Cloud API): per-message pricing

**Rules**
- Per-message pricing since **1 Jul 2025**. Only delivered messages from the business are charged.
- The customer service window lasts 24 hours from the user's last message. Outside it, only templates may be sent.
- Lebanon (+961) falls in the **"Rest of Middle East"** pricing region ([Meta developer docs, accessed 2026-11-17](https://developers.facebook.com/docs/whatsapp/pricing/)).

**Changes from 1 Oct 2026** ([Meta pricing updates, accessed 2026-11-17](https://developers.facebook.com/docs/whatsapp/pricing/updates-to-pricing/))
- **Service messages became chargeable**, with **1,000 free per business phone number per month** (no rollover).
- **Utility templates sent inside an open window are no longer free.**
- Rest of Middle East marketing rates went up.
- A new "Meta Business Agent" category is billed at $2.00 per 1M tokens.

**Rate card for Rest of Middle East (USD per delivered message, effective 1 Oct 2026)**

| Category | Rate |
|---|---|
| Marketing | $0.0392 |
| Utility | $0.0091 |
| Authentication | $0.0091 |
| Service (after the 1,000 free) | $0.0091 |

From Meta's "USD list rates" file, downloaded 2026-11-17 via the [rate-card section](https://developers.facebook.com/docs/whatsapp/pricing/). For comparison: Saudi Arabia marketing $0.0576, UAE $0.0576, Egypt $0.0644.

**Conflicts between Meta's own pages**
- Meta's marketing page still says it does "not charge for service messages" and describes a 72-hour free window after click-to-WhatsApp ads ([whatsappbusiness.com, accessed 2026-11-17](https://whatsappbusiness.com/products/platform-pricing/)).
- The developer docs and the rate card say service messages are charged after the free tier from 1 Oct 2026, and that the ad-entry window lasts up to 7 days.
- I treat the developer docs as authoritative.

**Provider fees (§3.1).** Meta's docs list only per-message charges and no separate platform fee. Provider options add €49 a month per number (360dialog), $0.005 per message (Twilio), or a $49–$279 subscription (CRM tools).

### 4.3 LLM cost to parse a messy grocery list (1,500 input + 500 output tokens per order, as given)

Prices: Anthropic from the [official pricing page (accessed 2026-11-17)](https://platform.claude.com/docs/en/about-claude/pricing); OpenAI from its [pricing page (accessed 2026-11-17)](https://developers.openai.com/api/docs/pricing); Google from its [pricing page (accessed 2026-11-17)](https://aistudio.google.com/docs/pricing).

| Model | Input / output per 1M tokens | Cost per order [E] | Calculation |
|---|---|---|---|
| Claude Haiku 5.5 (prompts up to 100k tokens) | $0.10 / $0.50 | **$0.00040** | 1,500 × 0.10 / 1M + 500 × 0.50 / 1M = 0.00015 + 0.00025 |
| Claude Sonnet 5.5 | $2 / $10 | **$0.0080** | 0.0030 + 0.0050 |
| Claude Opus 5.5 | $4 / $20 | **$0.0160** | 0.0060 + 0.0100 |
| OpenAI gpt-5-nano (alternative) | $0.05 / $0.40 | $0.000275 | 0.000075 + 0.0002 |
| OpenAI gpt-5-mini (alternative) | $0.25 / $2.00 | $0.001375 | 0.000375 + 0.001 |
| Google gemini-2.5-flash-lite (alternative) | $0.10 / $0.40 | $0.00035 | 0.00015 + 0.0002; a free tier also exists |

- Anthropic's Batch API halves these prices for jobs that do not need an instant answer, such as the overnight price-matching run ([Anthropic pricing](https://platform.claude.com/docs/en/about-claude/pricing)).
- **Caveat:** the 500-token output figure excludes any model reasoning tokens. Measure on 50 real Arabizi, Arabic, French and English lists before fixing a budget.
- **[E] Price-comparison agent run** (an assumption, not data): one run a day, each 50,000 input + 10,000 output tokens, 30 runs a month.
  - On Sonnet 5.5: 30 × (50,000 × 2 / 1M + 10,000 × 10 / 1M) = 30 × $0.20 = **$6.00 a month**.
  - On Haiku 5.5: 30 × ($0.005 + $0.005) = **$0.30 a month**.

### 4.4 Speech-to-text for WhatsApp voice notes

**Price per minute** ([OpenAI pricing, accessed 2026-11-17](https://developers.openai.com/api/docs/pricing))

| Model | Price per minute |
|---|---|
| gpt-4o-mini-transcribe | $0.003 |
| gpt-transcribe | $0.0045 |
| gpt-4o-transcribe | $0.006 |
| Whisper | $0.006 |

Google gemini-2.5-flash-lite charges $0.30 per 1M audio input tokens ([Google pricing](https://aistudio.google.com/docs/pricing)).

**Quality on Lebanese Arabic.** The most recent benchmark I found is the Sada-ASR paper ([arXiv, 14 Nov 2026](https://arxiv.org/html/2611.19512)). It was written by the vendor of one of the systems tested and uses a private test set with 5.0 hours of Lebanese audio.

Word error rate on Lebanese:

| System | Word error rate |
|---|---|
| Microsoft MAI-Transcribe-2 | 23.05% |
| Sada-ASR (the authors' own system) | 24.96% |
| ElevenLabs Scribe v2 | 29.37% |
| IFM Jais-ASR | 30.35% |
| OpenAI gpt-transcribe | 30.43% |
| Google Gemini 3.5 Transcribe | 31.73% |
| Speechmatics Enhanced | 34.37% |
| OpenAI Whisper large-v3 | 45.41% |

- Lebanese was the hardest variety for the leading systems.
- The paper did **not** test French or Arabizi code-switching.

**[E] What this means.** Even the best systems got roughly 1 word in 4 wrong on Lebanese. Voice orders need a "here is what I understood, reply OK" confirmation step.

### 4.5 Hosting (accessed 2026-11-17)

- **Supabase:**
  - Free: 500 MB database, 50,000 monthly active users, 2 projects. Projects are "paused after 1 week of inactivity".
  - Pro: from $25 a month, including $10 of compute credit ([supabase.com/pricing](https://supabase.com/pricing)).
- **Vercel:**
  - Hobby: $0, but restricted to **non-commercial personal use** ([Vercel fair use guidelines](https://vercel.com/docs/limits/fair-use-guidelines)).
  - Pro: $20 a month, including $20 of usage credit ([vercel.com/pricing](https://vercel.com/pricing)).
- **Hetzner Cloud:** Regular Performance (shared) server from **€5.49 a month** excl. VAT, about **$6.11** [E]: 5.49 × 1.1127 ([hetzner.com/cloud](https://www.hetzner.com/cloud/)).

### 4.6 Monthly tech cost estimate [E]

**Assumptions** (mine; the CFO should change them as needed)
- A1: per order, the business sends 3 service replies inside the window (confirmation, clarification, total) plus 1 utility template ("your bag is ready") outside the window.
- A2: one WhatsApp number.
- A3: 30% of orders include a 1-minute voice note.
- A4: list parsing on Claude Sonnet 5.5.
- A5: the price-agent run from §4.3, $6.00 a month on Sonnet 5.5.
- A6: no marketing templates (use the free app's broadcast lists or a WhatsApp group for "orders open today").
- Excluded: SIM or phone line, domain, Meta Verified, payment fees, the founder's time.

**WhatsApp (Cloud API, Rest of Middle East rates)**
- 50 orders: 150 service messages, all within the 1,000 free, so $0. Utility 50 × $0.0091 = $0.46. **Total $0.46.**
- 200 orders: 600 service messages, free. Utility 200 × $0.0091 = $1.82. **Total $1.82.**
- 1,000 orders: 3,000 service messages minus 1,000 free = 2,000 × $0.0091 = $18.20. Utility 1,000 × $0.0091 = $9.10. **Total $27.30.**

**Speech-to-text (gpt-transcribe, $0.0045 a minute)**
- 50 orders: 15 minutes = $0.07
- 200 orders: 60 minutes = $0.27
- 1,000 orders: 300 minutes = $1.35

| Line item | 50 orders a month | 200 orders a month | 1,000 orders a month |
|---|---|---|---|
| WhatsApp Cloud API (direct) | $0.46 | $1.82 | $27.30 |
| List parsing, Sonnet 5.5 ($0.008 per order) | $0.40 | $1.60 | $8.00 |
| Price agent, Sonnet 5.5 | $6.00 | $6.00 | $6.00 |
| Voice transcription | $0.07 | $0.27 | $1.35 |
| Hosting: Hetzner VPS | $6.11 | $6.11 | $6.11 |
| **Lean total** | **$13.04** | **$15.80** | **$48.76** |
| *Managed stack: replace Hetzner with Supabase Pro + Vercel Pro ($45) and add 360dialog (€49 ≈ $54.52)* | *$106.45* | *$109.21* | *$142.17* |
| *Lean stack, but all LLM work on Haiku 5.5 (parsing $0.0004 per order, agent $0.30)* | *$6.96* | *$8.58* | *$35.46* |

**How the totals add up**
- Lean, 50 orders: 0.46 + 0.40 + 6.00 + 0.07 + 6.11 = 13.04.
- Managed: lean total − 6.11 + 45 + 54.52. For 50 orders: 13.04 − 6.11 + 99.52 = 106.45.
- Haiku row: lean total − parsing − 6.00 + Haiku parsing + 0.30. For 1,000 orders: 48.76 − 8.00 − 6.00 + 0.40 + 0.30 = 35.46.

**Marketing templates are the expensive line.** One template to 100 subscribers on 22 working days would cost 100 × 22 × $0.0392 = **$86.24 a month** [E]. That is more than the whole lean stack.

**At 50 orders a month the API may not be needed.** The free WhatsApp Business app with manual copy-paste into the parser removes the WhatsApp line.

---

## 5. Price data and scraping

### 5.1 Legal notes (not legal advice; for a lawyer to confirm)

- **No Lebanese scraping law found.** I found no statute or court decision in Lebanon that deals specifically with web scraping (searches on 2026-11-17, not exhaustive). The nearest rules:
  - **Law 81/2018 (Electronic Transactions and Personal Data), Article 110, illegal access to an information system.**
    - Penalty: 3 months to 2 years in prison and a fine of LBP 1–20 million.
    - Aggravated cases (data deleted or altered, or the system disrupted): 6 months to 3 years and LBP 2–40 million.
    - Source: the Council of Europe's Octopus Lebanon profile ([coe.int, accessed 2026-11-17](https://www.coe.int/en/web/octopus/-/lebanon)). The PDF could not be opened; the figures come from the search summary, so verify against the Arabic gazette.
    - [E] At 89,700 LBP per USD, LBP 20 million ≈ $223 (20,000,000 / 89,700). The fines are now small; the prison term is the real exposure.
    - **Implication:** bypassing logins, CAPTCHAs or rate limits is the risky part. Reading public pages slowly is far less so.
  - **Law 75/1999 (copyright), Article 3:** protects "collections of information, whether in machine-readable form or any other form" where "the selection or arrangement of the content is original" ([Arabic text on Wikisource](https://ar.wikisource.org/wiki/%D9%82%D8%A7%D9%86%D9%88%D9%86_%D8%B1%D9%82%D9%85_75_%D9%84%D8%B3%D9%86%D8%A9_1999_%D8%A7%D9%84%D8%B1%D8%A7%D9%85%D9%8A_%D8%A5%D9%84%D9%89_%D8%AD%D9%85%D8%A7%D9%8A%D8%A9_%D8%A7%D9%84%D9%85%D9%84%D9%83%D9%8A%D8%A9_%D8%A7%D9%84%D8%A3%D8%AF%D8%A8%D9%8A%D8%A9_%D9%88%D8%A7%D9%84%D9%81%D9%86%D9%8A%D8%A9_(%D9%84%D8%A8%D9%86%D8%A7%D9%86))). Individual prices are facts. Copying a whole catalogue layout, product photos or descriptions is riskier.
  - **Personal data.** Prices are not personal data. Customers' WhatsApp numbers and orders are, and Law 81/2018 applies to them.
- **General principles from abroad (persuasive only, not Lebanese law)**
  - **Website terms are enforceable as a contract.**
    - In hiQ v LinkedIn (US), the court found hiQ breached LinkedIn's User Agreement by scraping. The case ended with a permanent injunction in Dec 2022 ([Proskauer, 8 Dec 2022](https://newmedialaw.proskauer.com/2022/12/08/hiq-and-linkedin-reach-proposed-settlement-in-landmark-scraping-case/)).
    - In Ryanair v PR Aviation (EU Court of Justice, C-30/14, 15 Jan 2015), the court held that the owner of a database not protected by database law is free to restrict its use by contract ([Kluwer Copyright Blog, 26 Jan 2015](https://legalblogs.wolterskluwer.com/copyright-blog/ryanair-ltd-v-pr-aviation-bv-contracts-rights-and-users-in-a-low-cost-database-law/)).
  - **robots.txt** is not a lock: "These rules are not a form of access authorization" ([RFC 9309, Sep 2022](https://www.rfc-editor.org/rfc/rfc9309)). It does show the site owner's wishes, and ignoring it weakens a good-faith defence.

### 5.2 Practical notes (checked 2026-11-17)

- **robots.txt and access checks**
  - **Spinneys Lebanon:** robots.txt disallows `/catalog/` and every URL containing `?` ([robots.txt](https://www.spinneyslebanon.com/robots.txt)). Its site shows a 1 USD = 89,700 LBP rate and delivery zones (Beirut, Greater Beirut, Mount Lebanon) ([spinneyslebanon.com](https://www.spinneyslebanon.com/)).
  - **tawfeermarket.com:** robots.txt allows everything except admin paths ([robots.txt](https://tawfeermarket.com/robots.txt)). The homepage is images plus an app-download link, so prices may live only in the app, which is harder and riskier to scrape.
  - **Others:** several other Lebanese chain sites were unreachable from our network (tawfeer.com.lb, Charcutier Aoun, Fahed). That says nothing about their policies.
- **Online and shelf prices can differ.** Libnanews' automated price index warns that "online and in-store prices may differ" and that errors occur in "scraping, matching, or currency conversion" ([Libnanews CPI, accessed 2026-11-17](https://price.libnanews.com/en/about)). The driver's receipt is the real truth.
- **Others already collect Lebanese supermarket prices** automatically (Libnanews) or as a platform (Awfarli, now inside a MoET dashboard: [Berytech, 20 Jul 2026](https://berytech.org/from-app-to-national-infrastructure-how-awfarli-grew-beyond-its-own-vision/)). A licence or partnership may be cheaper than building scrapers.

### 5.3 Lower-risk alternatives

1. **Official MoET weekly basket reports** ([30-03-2026 file](https://www.economy.gov.lb/media/15131/weekly-basket-report30-03-2026.xlsx); latest checked: 30 Mar 2026).
   - Contents: national average supermarket prices for **60 items**, a separate sheet for greengrocers and butchers (23 items) by region, and year-on-year and week-on-week changes.
   - It gives **averages, not named stores**, so it suits a "reference price" for model (f), not store choice.
   - Older monthly MoET reports did rank named supermarkets ([example, Jul 2020](https://www.economy.gov.lb/media/13047/summaryinfopricejuly2020en-rank.pdf)).
2. **A direct supplier partnership** (the founder's plan with Tawfeer): ask for a weekly price and offer file (CSV or WhatsApp catalogue). That removes scraping for the main supplier.
3. **Flyers and in-app promotions:** Tawfeer's app lists promotions ([App Store](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055)). These can be captured manually or with OCR on images the store sends.
4. **Manual checks by the driver:** photograph shelf tags and receipts each run. This also produces the audit trail that a share-of-savings fee needs.
5. **Receipts from members:** households who still shop elsewhere can share receipts.
6. **Licensing data** from Awfarli or Libnanews (no pricing found; to ask).

**If scraping is still used**
- Public pages only; never bypass logins or CAPTCHAs (Article 110 risk).
- Respect robots.txt and the terms; ask permission where possible.
- Identify the bot, rate-limit it and cache results.
- Store prices only, not photos or descriptions (Law 75/1999 Art. 3).
- Get a Lebanese lawyer's opinion before commercial use.

---

### Source notes and gaps
- No public Toters subscription or customer-fee schedule was found.
- Rewaa, Salla and Zeew pricing pages blocked access or showed no prices.
- Walmart's own page blocked automated access; Walmart figures are secondary.
- The Council of Europe PDF and the DailySocial KitaBeli article could not be opened; their figures come from search summaries.
- No data was found on the number of Lebanese mini-markets or parish committees, or their software spending.
- The search budget ran out while verifying the AED/USD peg, so Foodics prices are left in AED.
