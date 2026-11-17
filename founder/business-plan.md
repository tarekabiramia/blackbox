# Village Basket (working name) · Business plan

**Verdict: Profitable**

- ✓ Each bag earns $1.69 before fixed costs (60% contribution).
- ✓ Year 1 operating profit: $769.
- ✓ Break-even is 12 bags a day against a capacity of 20.
- ✓ 5 of 20 simulated buyers buy (25%, the bar is 25%).

| key number | |
| --- | ---: |
| Price | $2.80 a bag |
| Profit margin at plan | 25% per bag |
| Break-even | 12 bags a day |
| Year 1 operating profit | $769 |
| Startup spend | $2,975 |
| Cash needed before it pays for itself | $3,103 |
| Startup money earned back | not in year 1 |
| Buyer panel | 5 buy · 15 pass |

## The idea

- What it is: a daily group-buying grocery service for Amchit and its neighbouring villages: residents send their shopping list (mostly by WhatsApp) before a daily cut-off (e.g. 2 p.m.), software consolidates every order into one batch, an AI agent compares prices across 5–6 chosen supermarkets/suppliers (Tawfir Shop first) and exploits multi-buy promotions ("buy 3, get a discount") that a single household can't use, a driver buys the batch in one run, and residents collect their bags at a central pickup point in each village.
- Who it is for: households in Amchit (Jbeil/Byblos district, Mount Lebanon) and its neighbouring villages who today drive "down to the city" to get good supermarket prices, or pay more at the village mini-market.
- What it sells, at what price: the groceries at (close to) discount-supermarket prices, plus the service of not going to the city. How the business earns is NOT decided yet: candidates are a subscription, a percentage on each invoice, a margin kept from the promo/bulk savings, or a mix.
- Where and how: orders by WhatsApp (later an app/web form) until the daily cut-off; an owner dashboard tracks orders, batches, suppliers and money; a driver view lists what to pick at which store for a fast run; pickup at one central point per village (no door-to-door at the start).
- Budget and constraints: the founder is an R&D full-stack developer (also builds 3D websites, AI enthusiast) and will build the software himself. Limited liquidity: cannot fund many villages at once, so start in Amchit only. Plans to approach Tawfir Shop (a Lebanese store with many multi-buy offers) for a direct supplier relationship. Long-term: license/rent the software to other villages or operators outside Amchit, using his own village as the live showcase.

## Summary

**What it is.** A twice-weekly pooled grocery run, under the working name Village Basket (`brand.md` recommends *Sallet el-Jiran, سلّة الجيران*). Households in the hill villages above Amchit (Bejjeh, Ghalboun, Aabaydat, Kfoun) and car-less households in Amchit send a staples list on WhatsApp. One run buys everything at Tawfeer MAX Jbeil at its quantity and carton prices, and each bag waits at the village's own mini-market or the doorstep. Each bag carries a copy of the till receipt and a line-by-line slip.

**Verdict: Profitable, computed by `compile.py` and only just.** All four checks pass, none with room to spare:
- **Margin:** 25% at plan; each bag leaves $1.69.
- **Break-even:** 12 bags a run, against a car's ~20.
- **Year 1:** $769 operating profit.
- **Panel:** 5 of 20 simulated buyers, exactly the 25% bar.

The same tool says **Not yet** for the idea as originally pitched (daily runs, a $2 fee, till price passed through: −$7,498 in year 1). It also says Not yet for v2 if a driver is hired (−$1,607) or if pooled orders never reach Tawfeer's tiers (−$1,122).

**Where the board and the panel agreed.** It's a commodity offer unless it sells certainty and time, not price. The pitched 5–6-store comparison agent should go: cherry-picking across stores saves only 3–6% (`research/suppliers.md`) and adds stops. A hand-run pilot comes before code. **Where they differed:** the board debated whether the asset is the data, the experience or the guarantee. The panel answered with who buys: car-less households (6 of the 8 buyers across both panels). They buy access, not a discount. On the base bag a customer pays ~$0.15 more than Tawfeer's shelf price, in exchange for the trip not taken.

**The biggest risk** is the unmeasured gap between Tawfeer MAX's single-item price and its quantity/carton price. Half of each bag's revenue depends on it, and nobody publishes it. It is measured first, on the shelf, in test T1 (`launch.md`).

**What the founder needs to start.** About **$3,100 in hand**. Only **$775** of it is spent and gone; the other $2,200 is a float that comes back after each weekly settlement. Plus about 15–22 hours a week. It pays him under $1.30 an hour at plan, so the money alone does not justify the time. **The reason to do it is what it proves.** A measured, pooled village channel is something Tawfeer, with 41 branches and a 500-store target, cannot easily build alone (`tawfeer-pitch.md`). That conversation, not licensing software to villagers, is the upside (`board.md`, Monopoly lens; `research/business-model.md` §3).

**Not financial, legal or tax advice.** The panel is simulated buyers and every number is a projection. Real customers and real quotes confirm them.

**The one thing to do this week:** by **Sat 21 Nov**, photograph the PV1/PV2/PV3 price tags at Tawfeer MAX Jbeil for the 40 staples villagers buy most, and ask staff what quantity triggers each tier. Then call 1626 to ask for a meeting. If fewer than a quarter of a typical bag's value can reach the lower tiers, the model changes before anything else is built.

## What the board said

**Vote: 3 FUND IF, 0 FUND, 0 PASS. Average score 4.3 / 10** (Offers 4, Monopoly 4, Product 5).

Nobody passed, nobody funded outright. The board sees a real mechanism (pooled buying, a daily cut-off, pickup points, near-zero cost to reach buyers on WhatsApp) wrapped in an offer that today only says "cheaper", resting on savings the business does not control.

Memos: `board/offers.md`, `board/monopoly.md`, `board/product.md`.

### Risks more than one member raised (most dangerous first)

1. **The saving may not survive the costs.** (Offers #1, Monopoly #1, Product #2.) The money to share is multi-buy discounts plus price gaps between stores. The driver, fuel, bags, the pickup point, cash handling and the fee all come out of it. Every extra store adds a stop and driver time, which the original plan does not count. Nobody has priced a real basket yet.
2. **The edge is rented from the supplier.** (Offers #3, Monopoly #1.) Multi-buy offers are Tawfir's decision. A buyer pooling a whole village to hit "buy 3" is exactly what retailers cap per customer or end. Showing Tawfir the village's demand also shows it a market it could serve itself.
3. **One wrong bag ends trust.** (Offers #3, Product #1.) Free-text and voice-note orders, out-of-stock items, substitutions chosen by a stranger, and a total that changes. There is no substitution rule, guarantee or final receipt yet. In a village, one bad batch spreads fast.
4. **Too many features, no focus.** (Product #2, Offers, Monopoly #3.) A 5–6-store scraping agent, split batches, a dashboard, a driver app and licensing all come before the one-sentence promise exists. All three members want a pilot with one or two stores, run by hand, before any code.
5. **Easy to copy, and licensing sells the least defensible part.** (Monopoly #2–3, Offers.) To a villager this is a WhatsApp number, a car and a bag. The mini-market, a neighbour who drives down daily, or a delivery app can copy it. Licensing now would publish the playbook and create rivals chasing the same promotions.
6. **The pain may be weak in Amchit itself.** (Offers #2, Monopoly questions.) Amchit is next to Jbeil, so "going down to the city" is a short drive there. Inland villages likely feel it more.

### Where they disagreed (kept on purpose)

- **What the asset is.** Monopoly: the aggregated village demand data and buying power, not the promotions. Product: the experience of a correct bag. Offers: the guarantee plus time saved.
- **Licensing.** Monopoly would redesign it into a buying network: licensees buy through the founder's consolidated purchasing and he earns on network volume. Offers and Product simply say not yet.
- **How much the comparison agent matters.** Product would drop it from the pilot entirely. Monopoly sees scraping as fragile. Offers keeps it as a later optimisation.

### Conditions checklist (the rest of the pack tests these)

- [ ] **C1 Prove the gap on paper.** Price 3 real baskets bought alone vs pooled, minus the cost per order. The remainder must cover a fee buyers accept. *(competitors, research/suppliers, cfo)*
- [ ] **C2 Supply terms that don't depend on public promos.** Written direct or wholesale terms from Tawfir or a distributor. Monopoly's vote turns to PASS if the business only works on retail multi-buys. *(ops, cfo)*
- [ ] **C3 Sell time, certainty and a guarantee, not just price.** One-sentence promise, a guarantee for wrong or missing items, the saving printed on every receipt. *(offer, marketing)*
- [ ] **C4 Substitution rule + confirmation + final receipt** before the first order: every line marked "similar OK / skip / ask me". *(offer, ops)*
- [ ] **C5 Pilot by hand.** 2–4 weeks with WhatsApp, a spreadsheet, 1–2 stores and payment at cut-off. Write the pass marks first. *(launch)*
- [ ] **C6 Test the fee.** Flat per order vs % of bill vs subscription. *(consumer, pricing)*
- [ ] **C7 Pick the launch village by pain.** Compare Amchit with an inland neighbour. *(research/market-lebanon, consumer)*
- [ ] **C8 Settle money and the pickup handover.** Who fronts the cash, how people pay, a named host and hours, a fridge, a rule for uncollected bags. *(ops, cfo)*
- [ ] **C9 Density first.** Repeat households at or above the CFO's per-run break-even, held for a set period, before a second village. *(cfo, launch)*
- [ ] **C10 Defer licensing; redesign it as a buying network.** Not before two adjacent villages run well. *(plan)*
- [ ] **C11 Competitor map.** Show nobody already serves the village grocery run at a comparable price. *(competitors)*

### The strongest version of this business the board can see

It is not "an AI that finds the cheapest supermarket". It is a **village buying club**. Households join, send their list by 2 p.m., and collect a checked bag in their own village that evening. They are guaranteed to pay no more than the city shelf price plus one small, visible fee, and they see on every receipt what they saved. The club buys from one or two stores, ideally on negotiated wholesale terms that need the club's pooled volume, so the edge is the club's own and not a promo someone else can switch off. It starts in the village where the trip down hurts most, not necessarily Amchit centre. The software stays an internal tool until the club works. The long-term play is a **network of village pickup points buying through one consolidated purchasing account**, which gets stronger with every village, rather than a SaaS licence that creates rivals. This differs from the pitch in three ways: fewer stores, a guarantee instead of only a price promise, and a network instead of a licence. The board says so plainly.

## The competition

Researched 2026-11-17, from public sources only. Every fact has a link and a date ("read 2026-11-17" means a live page read that day). The quotes are short and verbatim, and they are research, not testimonials. Where something could not be confirmed, this report says so and does not guess.

> **Naming note.** "Tawfir Shop" in the idea is taken to be **Tawfeer (توفير)**, the Lebanese discount chain of Tawfeer International / Capital Partners. Its format is the one the idea describes: prices fall as quantity rises. A search for "Tawfir" plus offers returns only Tawfeer ([search, read 2026-11-17](https://www.beiruting.com/news/141422/tawfeer-max-a-new-era-of-value-retail-in-lebanon)). If the founder means a different shop, the Tawfeer findings below still apply, because Tawfeer is the nearest discounter to Amchit.

### The short version

- **Nobody in the area pools village orders today.** I found no public trace of a group-buying or pooled-run service for Amchit or the Jbeil villages. The competition is (a) delivery apps that bring one household's order to the door and (b) the household's own car.
- **One chain already delivers to Amchit by name.** Le Charcutier's coverage list includes "Amsheet, Byblos" and about 90 other villages in the district ([lecharcutier.com/delivery-coverage, read 2026-11-17](https://www.lecharcutier.com/delivery-coverage)). It publishes no fee or minimum.
- **Tawfeer opened a 2,000 m² "Buy More, Pay Less" store in Jbeil (Qartaboun) on 21–22 May 2026.** It has a three-tier price system: per piece, by quantity, and by carton or wholesale ([Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677); [Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%8A%D9%81%D8%AA%D8%AA%D8%AD-%D9%81%D8%B1%D8%B9%D9%87-%D8%A7%D9%84%D8%AC%D8%AF%D9%8A%D8%AF-%D9%81%D9%8A-%D8%AC%D8%A8%D9%8A%D9%84-%D9%88%D9%8A%D8%B7%D9%84%D9%82-%D9%86%D9%85%D9%88%D8%B0%D8%AC-%D8%A7%D9%84%D8%AA%D8%B3%D8%B9%D9%8A%D8%B1-%D8%A7%D9%84%D8%AB%D9%84%D8%A7%D8%AB%D9%8A-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D9%85%D9%86%D8%AE%D9%81%D8%B6-%D8%A7%D9%84%D9%83%D9%84%D9%81%D8%A9)). The idea's core trick, pooling to reach the cheaper quantity price, now has a store built for it on the Jbeil highway, a few km from Amchit. The same company also runs a delivery app, which is the biggest threat.
- **The only published delivery fees are $1.45 to $1.85 per order:** Carrefour's 130,000 LBP for Hazmieh–Baabda and noknok's $1.85 with no minimum. Toters, Tawfeer LB and Le Charcutier do not publish theirs. Village Basket's fee, or the saving it promises, will be compared against roughly $2 per order.
- **Top complaints about the delivery apps:** late or unpredictable delivery, support that does not fix anything, and missing or spoiled items (including Toters Fresh groceries). Paying above shelf price comes fourth.

---

### 1. The table, sorted by how directly each competes

"Reaches Amchit?" means a public source names Amchit/Amsheet or Jbeil in that service's coverage. "Unverified" means no public page says either way, and the founder should check by entering an Amchit address in the app (see section 8).

| # | Competitor | Type | Reaches Amchit? | Comparable "price": fee per order / minimum basket | Positioning (their words) | Rating (count) | Source, date |
|---|---|---|---|---|---|---|---|
| 1 | **Le Charcutier online** (Le Charcutier Aoun, 19 branches) | Direct | **Yes**: "Amsheet, Byblos", plus Blat, Halat, Mastita, Qartaboun and others | Not published; scheduled or express | "Your neighborhood superstore" | 5.0 App Store (8, new app) | [coverage, read 2026-11-17](https://www.lecharcutier.com/delivery-coverage); [App Store, read 2026-11-17](https://apps.apple.com/app/id6760022832) |
| 2 | **Tawfeer LB app** (Tawfeer home delivery) | Direct | Unverified (areas not published) | Not published; date and time slot; cash or card on delivery | "Shop Smart, Save Big" | 4.8 App Store (301); 4.06 Google Play (508), 87K+ installs | [App Store, read 2026-11-17](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055); [AppGoblin, updated 2026-11-12](https://appgoblin.info/apps/ma.osp.shopping_app.twds.android); [tawfeer.market, read 2026-11-17](https://tawfeer.market) |
| 3 | **Toters** (plus own dark stores "Toters Fresh" and the "Butler" buy-anything service) | Direct | Unverified. The FAQ says to enter your address in the app | Not published: "Delivery cost varies depending on the store, hour, and your location"; no subscription found in official sources | "Fast & easy delivery." | 4.8 App Store LB (23k); 3.78 Google Play (~38K), 9M+ installs | [FAQ](https://www.totersapp.com/faq) and [site](https://www.totersapp.com), read 2026-11-17; [App Store LB, read 2026-11-17](https://apps.apple.com/lb/app/toters/id1015006220); [AppGoblin, updated 2026-11-11](https://appgoblin.info/apps/com.toters.customer); [GDI, 13 Jul 2022](https://gdi.ch/blog/trend-updates/so-geht-quick-commerce-im-nahen-osten) |
| 4 | **noknok** | Direct | Unverified. The FAQ lists Batroun, Keserwan, Metn, Beirut, Tripoli, Zahle, Amioun but not Jbeil | **$1.85 flat, no minimum**; average 30 min | "everything. anything. one touch." | 4.4 App Store (28) | [FAQ, read 2026-11-17](https://noknok.co/faq); [Beiruting, 9 Oct 2025](https://www.beiruting.com/news/141299/%E2%80%9Cnoknok%E2%80%9D-celebrates-the-successful-launch-of-its-new-%E2%80%9Ceverything-app%E2%80%9D-in-beirut) |
| 5 | **Spinneys Lebanon online** | Direct | Unverified. Covers "Beirut, Greater Beirut and Mount Lebanon"; fulfilled from Hazmieh, Elissar, Ajaltoun; Jbeil not named | **Minimum $30**; fee not published | "Deliver to Beirut, Greater Beirut and Mount Lebanon" | 3.2 App Store (92) | [spinneyslebanon.com, read 2026-11-17](https://www.spinneyslebanon.com); [App Store, read 2026-11-17](https://apps.apple.com/lb/app/spinneys-lebanon/id1518229592) |
| 6 | **Carrefour Lebanon online** (Majid Al Futtaim) | Direct | Unverified (the site returned HTTP 503 to my reader) | **130,000 LBP (~$1.45)** shown for Hazmieh–Baabda; minimum not found | not read | n/a | Carrefour product pages as shown in search results, read 2026-11-17 ([example](https://carrefourlebanon.com/maflbn/en/beans/aoun-red-round-beans-900g/p/37043)) |
| 7 | **InstaShop** (Talabat) | Direct | Unverified. Listed as operating in Lebanon | Not found | Marketplace that "connects users with vendors" | n/a | [Wamda, 6 Mar 2025](https://www.wamda.com/2025/03/talabat-fully-acquires-instashop-32-million) |
| 8 | **AntounGreens** (Rasmaska farm, produce only) | Direct (narrow) | Listing says Tuesday delivery for "Batroun, Byblos" | Fee not found; order before 6 PM for next day; cash on delivery | not read (site unreachable) | n/a | [antoungreens.com](https://antoungreens.com/Delivery-Batroun-Jbeil-Jounieh-Beirut-p194901664): did not resolve on 2026-11-17; facts are from search-result text only |
| 9 | **Village dekkene / mini-markets** in Amchit and each neighbouring village | Indirect | Yes (on foot) | No fee. Founder says shelf prices are higher than in the city; **no public price data found** | n/a | n/a | No public listing found (search, 2026-11-17) |
| 10 | **Tawfeer MAX Jbeil** (in-store, Qartaboun, Beirut–Jbeil highway) | Indirect | Customer drives | No fee. Three tiers: lowest single-unit price, lower price for larger quantities, wholesale prices for small businesses, shops, restaurants and cafés (Annahar, translated) | "Buy More, Pay Less"; "cheap by the piece, cheaper by quantity, and cheapest by the carton" | n/a | [Beirut.com, 15 May 2026](https://www.beirut.com/en/?p=775151); [Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677); [Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%8A%D9%81%D8%AA%D8%AA%D8%AD-%D9%81%D8%B1%D8%B9%D9%87-%D8%A7%D9%84%D8%AC%D8%AF%D9%8A%D8%AF-%D9%81%D9%8A-%D8%AC%D8%A8%D9%8A%D9%84-%D9%88%D9%8A%D8%B7%D9%84%D9%82-%D9%86%D9%85%D9%88%D8%B0%D8%AC-%D8%A7%D9%84%D8%AA%D8%B3%D8%B9%D9%8A%D8%B1-%D8%A7%D9%84%D8%AB%D9%84%D8%A7%D8%AB%D9%8A-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D9%85%D9%86%D8%AE%D9%81%D8%B6-%D8%A7%D9%84%D9%83%D9%84%D9%81%D8%A9) |
| 11 | **Spinneys Jbeil** (in-store) | Indirect | Customer drives | No fee | none found | n/a | [Daleeeel, read 2026-11-17](https://daleeeel.com/en-lb/chain/2841/spinneys) |
| 12 | **Le Charcutier Aoun Jbeil, Mastita** (in-store) | Indirect | Customer drives | No fee | "Your neighborhood superstore" | n/a | [Daleeeel, page updated Jul 2021](https://www.daleeeel.com/en-lb/chain/2900/le-charcutier-aoun) |
| 13 | **Mobile vegetable vans** | Indirect | Not verified | Not found | n/a | n/a | No public source found for Amchit (2026-11-17) |
| 14 | **Via Appia weekly market**, Byblos old town | Indirect | Customer drives | No fee; prices not published | Producers' market, Saturdays 4–10 pm | n/a | [No Garlic No Onions, 14 Jul 2018](https://www.nogarlicnoonions.com/via-appia-jbeil-a-new-farmers-market-opens-in-byblos); 2025–26 status not confirmed |
| 15 | **Drive down to Jbeil weekly or monthly** | Substitute | Amchit is about 3.5 km from Byblos port | Fuel: 2,837,000 LBP (~$31.63) per jerrycan of 95-octane, plus time | n/a | n/a | [Almodon, 2 Oct 2026](https://www.almodon.com/economy/2026/10/02/%D8%A3%D8%B3%D8%B9%D8%A7%D8%B1-%D8%A7%D9%84%D9%85%D8%AD%D8%B1%D9%88%D9%82%D8%A7%D8%AA-%D8%AA%D8%AA%D8%B1%D8%A7%D8%AC%D8%B9-%D9%83%D9%85-%D8%B3%D8%AC%D9%84%D8%AA); distance from [hotel listing (search result)](https://www.sembo.com/places/lebanon/hotels/15151899/amchit-grand-hotel) |
| 16 | **Monthly bulk shop** (stock up at Tawfeer MAX's quantity or carton tier) | Substitute | Customer drives | No fee; needs cash up front and storage | see #10 | n/a | [Beirut.com, 15 May 2026](https://www.beirut.com/en/?p=775151) |
| 17 | **Ask a commuting relative or neighbour** | Substitute | Yes | Free (a favour) | n/a | n/a | No public source; this is the founder's own observation |

Also checked but left out, because nothing tied them to Jbeil: Yala Stop (35 stores, mostly at petrol stations; [Berytech](https://berytech.org/yala-stop-convenience-in-store-online/)), Hachem Online, Fahed and Bou Khalil (no Jbeil branch or delivery terms found), and TSC (nothing found). The full set of rows is in `founder/competitors.csv`.

Context: Amchit (Amsheet) is about 40 km north of Beirut and has a population of "around 25,000" (2010 citation) ([Wikipedia, read 2026-11-17](https://en.wikipedia.org/wiki/Amchit)). Cost pressure is high in this region. In a January 2026 survey of 2,400 respondents, rising living costs were felt "most noticeably in Baalbek-El Hermel, followed by Keserwan-Jbeil" ([LCPS, 21 Jul 2026](https://www.lcps-lebanon.org/en/articles/details/6050/lebanons-cost-of-living-crisis-beyond-monitoring-and-enforcement-of-essential-food-prices)).

---

### 2. Price range for the comparable item (the fee per order and the minimum basket)

Only two delivery services publish a per-order fee that could apply to the area:

| Measure | Lowest | Median | Highest | n |
|---|---|---|---|---|
| Delivery fee per order (published) | **$1.45** (Carrefour, 130,000 LBP, Hazmieh–Baabda zone) | **$1.65** | **$1.85** (noknok, any location it covers) | 2 |
| Minimum basket (published) | **$0** (noknok) | n/a | **$30** (Spinneys online) | 2 |
| In-store options (Tawfeer MAX, Spinneys Jbeil, the dekkene) | $0 fee, but the household pays in fuel, time and carrying | | | |

- **Not published:** Toters ("varies depending on the store, hour, and your location"), Tawfeer LB, Le Charcutier and InstaShop.
- **The hidden price is the mark-up.** A Toters reviewer (5 Sep 2025) wrote: "the toters price is 20% to 30% over the in store menu price." Another reviewer (17 Jun, no year) said Toters charges stores "a shocking 27% fee on all orders." Both are single reviewer claims, not verified ([App Store LB, read 2026-11-17](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)).
- **Fuel benchmark for the "drive down" substitute:** a jerrycan of 95-octane costs 2,837,000 LBP, about $31.63 at 89,700 LBP/$ ([Almodon, 2 Oct 2026](https://www.almodon.com/economy/2026/10/02/%D8%A3%D8%B3%D8%B9%D8%A7%D8%B1-%D8%A7%D9%84%D9%85%D8%AD%D8%B1%D9%88%D9%82%D8%A7%D8%AA-%D8%AA%D8%AA%D8%B1%D8%A7%D8%AC%D8%B9-%D9%83%D9%85-%D8%B3%D8%AC%D9%84%D8%AA)). Amchit town is only a few km from Byblos, so for a household with a car the fuel cost of one trip is small. The real cost is time.
- **The saving to beat:** Tawfeer says its prices are "15%-20% less than other supermarkets" (company claim, [Beiruting, 11 Jul 2025](https://www.beiruting.com/news/141219/tawfeer-supermarket-fuels-growth-opens-36th-store-in-saida-amidst-ambitious-500-store-vision-by-2030)). The extra discount from its quantity and carton tiers is **not published**. It has to be priced in the store (section 8).

**For `/founder-pricing`:** households will compare any per-bag fee with "about $2 delivered to my door" (noknok, Carrefour). A pickup-point service that is slower than door delivery must either charge clearly less than that or show a basket saving several times larger than it.

---

### 3. Positioning map

Axes chosen for an Amchit household:
- **Price paid** (left = more expensive, right = cheaper), counting shelf price plus fees and mark-ups.
- **Effort** (top = comes to you, bottom = you drive, park and carry).

The price axis is evidence-light. Tawfeer's position comes from its own claim and published tiers, the dekkene's from the founder, and Toters' mark-up from one review.

```
                         COMES TO YOU (low effort)
                                   ^
  Toters  *                        |                 * Tawfeer LB app   <-- danger zone if it
  (fee varies; +20-30% per         |                   (fee/areas         serves Amchit cheaply
   one review)                     |                    unpublished)
          Le Charcutier online *   |
          (delivers Amsheet;       |   * noknok ($1.85, no min; Jbeil not named)
           fee unpublished)        |
  Spinneys online *                |   * Carrefour online (~$1.45, zone unverified)
  ($30 min; Jbeil not named)       |
                                   |
  Village dekkene *                |          [ VILLAGE BASKET target:            ]
  (walk; pricier per founder)      |          [ quantity/carton-tier prices, shelf    ]
                                   |          [ receipt passed through, collect in    ]
                                   |          [ the village at a fixed hour           ]
  PRICIER  <-----------------------+------------------------------------>  CHEAPER
                                   |
  Spinneys Jbeil (in-store) *      |      * Tawfeer MAX Jbeil, single units (tier 1)
  Le Charcutier Mastita (in-store)*|                     * Tawfeer MAX by quantity/carton
                                   |                       (= the monthly bulk-shop substitute)
  Via Appia Saturday market *      |
                                   v
                         YOU DRIVE, PARK, CARRY (high effort)
```

What the map shows: the low-price side of the map is reached only by driving to Tawfeer MAX and buying in quantity. The door-delivery side is all at single-unit prices plus a fee. The empty space is the middle-right: tier prices without the drive. That is where Village Basket would sit. The Tawfeer LB app sits right next to that space and could fill it.

---

### 4. What their customers complain about, ranked

Reviews read: Toters (App Store Lebanon and US storefronts, a Google Play mirror, ComplaintsBoard), Tawfeer LB (App Store), Spinneys Lebanon (App Store) and noknok (App Store). I read 1–3 star reviews first. Counts are reviews mentioning the theme. A theme is marked **thin** below three. Many App Store dates show no year. Toters' US storefront also carries Iraqi reviews, and those were excluded where the text showed it (IQD prices).

| Rank | Theme | Count | Where | Short verbatim quotes |
|---|---|---|---|---|
| 1 | **Late or unpredictable delivery, no driver assigned** | ~14 (Toters 10, Tawfeer LB 3, Spinneys 1) | Toters, Tawfeer LB, Spinneys | "Took an hour for my order to arrive and the branch is literally 2 mins away from me" (Tawfeer LB, 28 Aug 2025, [link](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055?see-all=reviews)) · "Always the delivery is late and they lie 5 minutes 10 minutes and it takes more than 2 hours" (Tawfeer LB, 25 May 2024, [link](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055?see-all=reviews)) · "Orders get confirmed immediately, you give me an estimated delivery time, and then… nothing." (Toters, Aug, no year, [link](https://apps.apple.com/us/app/toters-totrz/id1015006220?l=en&see-all=reviews)) · "No drivers are ever available, and orders are taking 1-2 hours." (Toters, undated, [ComplaintsBoard](https://www.complaintsboard.com/toters-b148439)) |
| 2 | **Support that answers but does not fix** | 17+ (Toters LB storefront 9, Toters US storefront 3, ComplaintsBoard 4+, Tawfeer LB 1) | Mostly Toters | "I received no call from customer service only an email saying they would call." (Toters, 5 Sep 2025, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) · "their support team takes far too long to respond." (Toters, 17 Nov 2024, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) · "Toters has unfortunately become the most unprofessional delivery app I’ve used." (Toters, 15 Oct 2025, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) |
| 3 | **Missing, wrong, unavailable or spoiled items** (groceries included) | ~9 (all Toters; +1 wrong-address order at Tawfeer LB) | Toters, Toters Fresh | "For a service that calls itself “Fresh,” this is unacceptable." (Toters Fresh: rotten or expired items on four orders, 14 Aug 2025, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) · "they dont tell u ahead of time that an item is unavailable" (Toters, 2 Aug 2024, [link](https://apps.apple.com/us/app/toters-totrz/id1015006220?l=en&see-all=reviews)) · "they all arrived with grey spots all over them and they smelled rotten" (mangoes, Toters, 14 Jun, no year, [link](https://apps.apple.com/us/app/toters-totrz/id1015006220?l=en&see-all=reviews)) · "Always Pay by cash after you check your order." (Toters, 25 Oct 2022, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) |
| 4 | **Paying more than in the store** (mark-ups, rising fees, fake promos) | 6 (Toters 4, noknok 1, Spinneys 1). Only **one** is a dated 2025 Lebanese mark-up claim | Toters, noknok, Spinneys | "the toters price is 20% to 30% over the in store menu price." (Toters, 5 Sep 2025, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) · "False advertisement on products and fake promotions." (noknok, 9 Jun, no year, [link](https://apps.apple.com/app/id1360852720)) · "the price getting more expensive with the worst supporting customer service" (Toters, undated, [ComplaintsBoard](https://www.complaintsboard.com/toters-b148439)) |
| 5 | Loyalty points worth little | 3 (borderline) | Toters | "The points system is laughable." (22 Jul 2024, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) · "the rewards program lacks value, and the customer service is among the worst." (2 Feb 2025, [link](https://apps.apple.com/lb/app/toters/id1015006220?see-all=reviews)) |
| 6 | App slow or won't log in | 3 (borderline; mostly older) | Spinneys LB | "The application is so slow to open" (11 May 2024) · "it never logs in. Please fix" (27 Feb 2025) ([link](https://apps.apple.com/lb/app/spinneys-lebanon/id1518229592?see-all=reviews)) |

What customers praise: Tawfeer LB's prices ("Great deals and prices", 29 Aug 2022, plus two similar reviews). Toters is credited with range and drivers. One reviewer called it the only functioning delivery app in Lebanon (22 Jul 2024).

Not found: Google Maps reviews for Tawfeer MAX Jbeil or Spinneys Jbeil (not readable by my reader), and Reddit r/lebanon threads about grocery delivery to Jbeil (none surfaced in search).

---

### 5. THE GAP

**What nobody does well:** getting quantity- and carton-tier discount prices to a household that buys single units, without the household driving, and with the shelf receipt shown so no hidden mark-up is possible. Collection would be at a known hour in the village, from a known local person on WhatsApp.

The evidence for it:
1. **The cheapest prices in the district need volume.** Tawfeer MAX Jbeil's tiers are "cheap by the piece, cheaper by quantity, and cheapest by the carton" ([Beirut.com, 15 May 2026](https://www.beirut.com/en/?p=775151)), and tier 3 is wholesale for shops ([Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%8A%D9%81%D8%AA%D8%AA%D8%AD-%D9%81%D8%B1%D8%B9%D9%87-%D8%A7%D9%84%D8%AC%D8%AF%D9%8A%D8%AF-%D9%81%D9%8A-%D8%AC%D8%A8%D9%8A%D9%84-%D9%88%D9%8A%D8%B7%D9%84%D9%82-%D9%86%D9%85%D9%88%D8%B0%D8%AC-%D8%A7%D9%84%D8%AA%D8%B3%D8%B9%D9%8A%D8%B1-%D8%A7%D9%84%D8%AB%D9%84%D8%A7%D8%AB%D9%8A-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D9%85%D9%86%D8%AE%D9%81%D8%B6-%D8%A7%D9%84%D9%83%D9%84%D9%81%D8%A9)). A single household buying three of something never reaches tier 2. A pooled village order can.
2. **Door delivery is single-unit price plus a fee.** Published fees are $1.45–$1.85. The others don't publish, and one Toters reviewer reports a 20–30% mark-up. None of the delivery apps advertises tier pricing.
3. **The top complaints are reliability, support and spoiled items**, not range. A fixed daily collection hour, a bag checked at handover and a named local organiser on WhatsApp answer complaints 1–3 directly. Passing the shelf receipt through answers complaint 4.
4. **Demand pressure is real.** Keserwan-Jbeil ranked second in Lebanon for felt cost-of-living increases in January 2026 ([LCPS, 21 Jul 2026](https://www.lcps-lebanon.org/en/articles/details/6050/lebanons-cost-of-living-crisis-beyond-monitoring-and-enforcement-of-essential-food-prices)).

**Said plainly, the gap is narrow and could close fast:**
- **"Going down to the city" is a short trip for Amchit town.** It is about 3.5 km to Byblos port, and Tawfeer MAX, Spinneys Jbeil and Le Charcutier Mastita are all on the Jbeil highway. For a household with a car, the pain is time, not distance. The pain is bigger for households without a car, older residents and the higher villages. None of these could be sized from public sources.
- **Le Charcutier already delivers to "Amsheet".** Tawfeer already has a delivery app. If the Tawfeer LB app delivers to Amchit for about $2, the gap shrinks to "tier-2/3 prices through pooling" alone. That saving is unpublished and has to be measured.
- **Price comparison across 5–6 supermarkets is weaker here than it sounds.** Within the run there are only three named chain stores near Amchit (Tawfeer MAX, Spinneys Jbeil, Le Charcutier Mastita). Every extra store adds driver time.

---

### 6. THE THREAT: who could copy this fastest

1. **The village dekkene owner: fastest (days).** The owner already has the location (the natural pickup point), the trust, the WhatsApp contacts and a vehicle for restocking. They can now buy at Tawfeer MAX's tier-3 wholesale prices, offered to small businesses, shops, restaurants and cafés ([Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%8A%D9%81%D8%AA%D8%AA%D8%AD-%D9%81%D8%B1%D8%B9%D9%87-%D8%A7%D9%84%D8%AC%D8%AF%D9%8A%D8%AF-%D9%81%D9%8A-%D8%AC%D8%A8%D9%8A%D9%84-%D9%88%D9%8A%D8%B7%D9%84%D9%82-%D9%86%D9%85%D9%88%D8%B0%D8%AC-%D8%A7%D9%84%D8%AA%D8%B3%D8%B9%D9%8A%D8%B1-%D8%A7%D9%84%D8%AB%D9%84%D8%A7%D8%AB%D9%8A-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D9%85%D9%86%D8%AE%D9%81%D8%B6-%D8%A7%D9%84%D9%83%D9%84%D9%81%D8%A9)) or from **Toters Trade**, Toters' wholesale unit "providing restaurants, cafés, hotels, supermarkets…" ([Toters job post, 31 Jul 2026](https://jobs.mevp.com/companies/toters/jobs/88265487-demand-planner-toters-trade)). "Send me your list by 2 pm, collect at 6" needs no software. **Defence:** recruit the dekkene as the pickup point and pay it per bag, rather than competing with it. This is what the winners abroad did (section 7).
2. **Tawfeer itself: most dangerous (weeks).** It owns the prices, the Jbeil store, a delivery app with 87K+ Android installs ([AppGoblin](https://appgoblin.info/apps/ma.osp.shopping_app.twds.android)) and a B2B tier. It plans 500 stores by 2030 ([Beiruting, 11 Jul 2025](https://www.beiruting.com/news/141219/tawfeer-supermarket-fuels-growth-opens-36th-store-in-saida-amidst-ambitious-500-store-vision-by-2030)) and listed 41 branches as of April 2026 ([tawfeer.market](https://tawfeer.market)), so it could open a small Amchit store or add a village pickup slot. Asking Tawfeer for a direct supply deal shows them the demand. **Defence:** own the customer list and the WhatsApp relationship, keep at least two suppliers, and consider offering Tawfeer the village channel as a partner. Operating on Tawfeer's ground while hiding the plan is risky.
3. **Le Charcutier: already in Amchit.** It could add a cheaper scheduled village drop tomorrow.
4. **Toters: least likely to bother with one town.** Its model is on-demand with per-order fees. It does have Butler, Fresh dark stores and drivers, and could add scheduled batched slots.

The threat to the long-term **software-licensing plan** is lower. The chains have their own tech. The natural buyers would be other village organisers and dekkene owners.

---

### 7. Analogs abroad: community group buying with pickup points

| Player | Model | Peak scale | What happened | Sources |
|---|---|---|---|---|
| **Meituan Youxuan** (China) | Next-day pre-order, collected from a neighbourhood "group leader"; head office funded subsidies and set prices | 20 million orders a day within 5 months | "New initiatives" (incl. Youxuan) lost RMB 20.2bn in 2023. It quit loss-making regions in June 2025, kept parts of Guangdong and Zhejiang, and left Guangzhou on 15 Dec 2025 | [TechNode, 25 Jun 2025](https://technode.com/2025/06/25/meituan-expands-instant-retail-scales-back-community-group-buying-in-unprofitable-areas/); [KrASIA, 23 Jul 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| **Duoduo Maicai** (Pinduoduo, China) | Marketplace: merchants pay platform fees; it set maximum prices and picked lowest-bid suppliers | 44% market share (2024) | First full-year profit in 2024 | [KrASIA, 23 Jul 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| **Xingsheng Youxuan** (China) | Built by a Hunan convenience-store chain. Only store managers could be group leaders; no deposit, commissions paid | RMB 10bn GMV and ~8m orders a day (2019); raised ~$1.5bn in 2020 | Close to breakeven in Hunan; retreated to 3 central provinces by end-2021; 17% share (2024) | [KrASIA, 23 Jul 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom) |
| **DealShare** (India) | Group discounts sold over WhatsApp, then an app | Claimed 1.5 lakh daily orders; ~$400M raised; >$1.7bn valuation | Shut B2B and exited states in 2023. FY24 revenue down ~75% to INR 499 Cr, loss INR 167.7 Cr. In Aug 2026, in acquisition talks and could "shut down its remaining operations" | [Inc42, 5 Aug 2023](https://inc42.com/features/DealShare-on-shaky-ground-ceo-vacuum-underscores-operational-mess); [Inc42, 12 Nov 2024](https://inc42.com/buzz/dealshares-fy24-revenue-plummets-75-to-inr-500-cr/amp); [Lapaas Voice citing Entrackr, 25 Aug 2026](https://lapaasvoice.com/dealshare-in-acquisition-talks-amid-shutdown-risk/) |
| **CityMall** (India) | Tier 2–4 towns; community leaders now used only for fulfilment; next-day; **no delivery or handling fee**; margin from private label and supply chain | 60 cities; average order ₹450–500 (~$5–6); $165M raised | $47M Series D in Sept 2025 at a flat $320M valuation. Says it is "operationally profitable", while Entrackr reported >30% negative EBITDA margins | [TechCrunch, 1 Sep 2025](https://techcrunch.com/?p=3041326) |
| **Super** (Indonesia) | "Agents" (individuals or warungs, i.e. village shops) resell and handle the last mile; restocked within 24h | 30 cities; thousands of agents; $106M raised | No 2023–26 public update found | [TechCrunch, 1 Jun 2022](https://techcrunch.com/2022/06/01/indonesian-hyperlocal-social-commerce-app-super-gets-70m-led-by-nea) |
| **KitaBeli** (Indonesia) | "Team buying" of FMCG through an app, tier 2–3 towns | ~$30M raised | Reported "in the process of liquidation" for lack of product-market fit (unconfirmed; article date not visible, page returned 503) | [DailySocial](https://en.dailysocial.id/post/social-commerce-we-buy-liquidation) (seen via search, 2026-11-17) |

**Lebanese precedent:** Dikkeneh Co-op in Basta al-Tahta, Beirut. Members paid monthly dues "as little as 5,000 Lebanese pounds" to buy at cost, and non-members paid 10% more. Dues did not cover running costs, and it was still a pilot ([The Public Source, 3 Jul 2021](https://thepublicsource.org/we-all-benefit-little-dikkeneh-coop-could)).

**The lessons that matter for a village operator:**
1. **Volume bought with discounts leaves with the discounts.** "Once subsidies were stopped, order volume fell off a cliff..." ([KrASIA, 2026](https://kr-asia.com/after-the-cash-burn-what-remains-of-chinas-community-group-buying-boom)). The saving has to come from structure (the tier prices, one run, supplier-funded multi-buys), not from launch promos.
2. **The survivors piggy-backed on an existing shop and stayed dense.** Xingsheng used only store managers as leaders and was near breakeven only in its home province. Super uses warungs. Meituan kept only its profitable regions. Make the dekkene the pickup point, and stay in Amchit until one run pays for itself.
3. **Stay light, and don't make the per-bag fee the business.** Duoduo Maicai's merchant-funded marketplace became profitable, while Meituan's centralised model did not. CityMall charges no fee on $5–6 baskets and earns from margin. DealShare's thin margins needed venture money to grow. Hold no stock, let suppliers fund the promotions, and earn from the pooled saving or a supplier commission. A household will hold a fee up against noknok's $1.85.

---

### 8. What could not be verified, and the field check that settles it

| Unknown | Why it matters | How to check (about 2 hours) |
|---|---|---|
| Whether Toters, Tawfeer LB, noknok, Spinneys, Carrefour and InstaShop deliver to Amchit, and their actual fee and minimum | Decides whether the "comes to you" side of the map is crowded | Enter an Amchit address in each app; screenshot the fee and minimum at checkout |
| Le Charcutier's fee and minimum to "Amsheet" | It is the one confirmed door-delivery rival | Same: put a basket in the app and reach checkout |
| How much Tawfeer MAX's quantity and carton tiers actually save | This is the whole margin of the idea | Price 20 everyday items at tiers 1, 2 and 3 in the Qartaboun store |
| Dekkene shelf prices vs Tawfeer and Spinneys | The founder's claim, with no public data | Price the same 20 items at two Amchit dekkenes |
| Informal WhatsApp grocery runners and vegetable vans in Amchit | Possible direct competitors invisible online | Ask at the municipality, the church or mosque groups, and two dekkenes |
| Whether the Via Appia Saturday market still runs | Indirect competitor for produce | Visit or ask the Byblos municipality |

Blocked during research: carrefourlebanon.com (HTTP 503), antoungreens.com (did not resolve), poidata.io and L'Orient Today (HTTP 403), Google Maps and Google Play review pages (not readable by my reader), and an OpenStreetMap shop query (connection reset).

## The buyer panel

**5 buy · 15 pass** (25% buy) out of 20 simulated buyers. Seed 2026, so the same cards can be dealt again.

These are simulated buyers, not customers. Use this to find objections and weak spots, then confirm the big ones with real people before you spend.

### By segment

| group | buyers | buy rate |
| --- | ---: | ---: |
| Comfortable family on two salaries or remittances from abroad | 3 | 33%  (thin) |
| Older person or couple who rarely or never drives | 3 | 33%  (thin) |
| Hill-village household (Bejjeh, Ghalboun, Aabaydat or Kfoun), 20 to 25 minutes by car from the Jbeil supermarkets | 7 | 29%  (thin) |
| Amchit-centre household, 5 to 6 minutes by car from Spinneys, Tawfeer MAX and Le Charcutier in Jbeil | 7 | 14%  (thin) |

### By buying behaviour

| group | buyers | buy rate |
| --- | ---: | ---: |
| Delivery app user | 2 | 100%  (thin) |
| Picky about fresh food | 2 | 50%  (thin) |
| Deal hunter | 3 | 33%  (thin) |
| Daily mini-market top-up | 4 | 25%  (thin) |
| Commuter | 3 | 0%  (thin) |
| Weekly big shop | 4 | 0%  (thin) |
| Relies on family or neighbours | 2 | 0%  (thin) |

### By income

| group | buyers | buy rate |
| --- | ---: | ---: |
| $15,000 and up | 8 | 38% |
| under $11,000 | 6 | 17%  (thin) |
| $11,000 to $15,000 | 6 | 17%  (thin) |

### Why they pass

| reason | buyers | in their words |
| --- | ---: | --- |
| habit | 7 | "I already drive down to Tawfeer or Spinneys once a week and fill the boot, and the dekkene owner is my neighbour and lets me pay at the end of the month. Sharing half the saving and paying $1.25 a bag doesn't beat that for me." (P007) · "My son or the neighbour already brings what I need, and the dekkene owner lets me pay at the end of the month. I don't see why I'd pay a fee and pay cash on the spot to someone I don't know." (P012) |
| need | 3 | "I already stop at a supermarket on my way home from Jounieh, and Tawfeer MAX is five minutes from my house. Half of the bulk saving minus $1.25 a bag is probably a few dollars at best, so I don't see why I would hand my list to someone else." (P001) · "I pass a supermarket on my way home anyway and Tawfeer is only 5 or 6 minutes away, so I don't need someone to shop for me. And I want to choose my own vegetables and meat, which they don't do." (P003) |
| convenience | 3 | "I already drive down to Tawfeer or Spinneys once a week and it takes me five minutes. Sending a list the night before, then collecting it, is more hassle than going myself, and I would pay a bag fee for something I can already do." (P002) · "I already drive to Jbeil every Saturday for the big shop and top up at the dekkene daily, so this doesn't fix a problem I have. I'd still have to go and collect it, at their hour, not mine." (P008) |
| trust | 1 | "I already have my tab at the dekkene and my son or the neighbour brings what I need. I do not know this person, and I am afraid of getting the wrong item or a bad one when I cannot go and check at the shop myself." (P010) |
| price | 1 | "I already drive to Jbeil every Saturday and catch the Tawfeer and supermarket offers myself, so paying $1.25 a bag to get half the saving is just giving away money. I also want to see and choose what I buy." (P014) |

### Why they buy

| reason | buyers | in their words |
| --- | ---: | --- |
| convenience | 2 | "With no car, getting to the Jbeil supermarkets means paying someone or a taxi, so a bag waiting at the mini-market in my village for $1.25 is easier. I would try the free first bag and keep going only if the receipt really matches." (P005) · "We have no car, so getting to the Jbeil supermarkets is a hassle and a cost. The first bag is free and pickup is at the mini-market in my village, so I would try it for the heavy staples like oil, rice, detergent and milk. I would still go buy my vegetables and meat myself." (P018) |
| need | 1 | "We have no car right now, so getting to Tawfeer MAX means a taxi or asking someone for a lift. If the Tawfeer prices are real and I only pay $1.25 a bag, that is cheaper than a ride. The first bag has no fee, so I will try it and check the slip against the receipt." (P006) |
| price | 1 | "The first bag is free and the fresh things stay mine to choose, so I would try it for the cartons of oil, detergent and diapers I now pay the dekkene extra for. If the slip really shows I saved something, I keep going, but not for every little thing." (P011) |
| trust | 1 | "The first bag has no fee and I can hand back anything wrong, so I'll try it once or twice for the packaged things and the cleaning stuff. I keep choosing my own vegetables and meat anyway, so it doesn't touch what I care about." (P017) |

### What would flip a no

- A guarantee that I always save more than the bag fee, shown on the first two slips, and a neighbour I know vouching for them.
- If the saving was clearly big and written on the slip every time, with no bag fee, and I could still change my list on the morning of the run.
- If they also picked fresh vegetables and meat the way I would, or if I could not get to the supermarket for a while, for example because I was ill or the car was in the garage.
- If the slip showed real savings of several dollars a bag, clearly more than the fee, on the items I actually buy, and the first bag was free so I could check it.
- If the slip showed I save a clear amount, like $5 or more a bag, and I could pay at the end of the month like at the dekkene.
- Free delivery to my door with no extra fee, and a clear proof on the first bag that I saved more than I paid in fees.
- Free delivery to my door on the same day, with no tab-style charge, and daily or on-demand ordering instead of only Tuesday and Friday.
- If my neighbour or someone from the family already used it and told me it was honest, and if I could pay later like at the dekkene, I would try one small bag.
- If it was run by someone I know and let me pay at the end of the month like the dekkene, with no bag fee, and the saving on the slip was clearly more than I'd pay.
- A first bag from someone I know in the village that turns out right, with the savings shown clearly, and no fee unless the bag saves me more than it costs.
- No fee at all and the full bulk saving passed on, or a week when I truly cannot get down to Jbeil.
- If the dekkene itself took the order and I could keep my tab with the same man, with no fee per bag.

Buyers say they would buy **2.6 times** in the first month on average.

20 buyers gave all four price answers. Run founder-pricing's van_westendorp.py on the answers folder.

## Pricing

### 1. The price

**$1.25 service fee per bag, plus half of the measured bulk saving. Doorstep drop +$1.50. First bag, no fee.** After the `ops.md` cost corrections, $1.25 leaves only $769 for year 1, so the CFO's preferred price is $1.50 if the test in §4 shows conversion holds.

Why this, and not the pitched $2:

- **What buyers said** (`pricing-curve.md`, 50 simulated buyers, all gave four answers):
  - acceptable range $0.51 to $2.50;
  - indifference price (as many call it a bargain as expensive) **$1.01**;
  - median "getting expensive" **$2.00**, median "too expensive" $3.50.
  - $2 sits inside the range but right on the point where half the panel starts to call it expensive. $1.25 sits just above the indifference point.
- **What the alternatives cost** (`competitors.md`, `research/market-lebanon.md`):

  | alternative | cost per trip or order | notes |
  | --- | --- | --- |
  | Household's own trip, Amchit centre | ~$2.60 (fuel + time) | estimate |
  | Household's own trip, Bejjeh / hill villages | ~$6.90 | estimate |
  | Published delivery fees (Carrefour Hazmieh 130,000 LBP ≈ $1.45; noknok $1.85) | $1.45–$1.85 | neither confirmed for Amchit or Jbeil |
  | Wakilni courier | ~$6 | |

  Pickup at $1.25 sits under every delivery fee. Doorstep at $2.75 ($1.25 + $1.50) is under a hill-village trip and well under a courier.
- **What the business needs** (`cfo.md`, unit_economics.py at each candidate):

  | fee | revenue / bag | break-even (bags a run) | year 1 operating profit |
  | ---: | ---: | ---: | ---: |
  | $1.00 | $2.55 | 14 | $339 |
  | **$1.25** | **$2.80** | **12** | **$769** |
  | $1.50 | $3.05 | 11 | $1,199 |
  | $2.00 | $3.55 | 9 | $2,058, but at the panel's median "getting expensive" point |

  The fee alone can never carry it. If no item ever reaches a tier price, the bag earns $1.70 and break-even is 34 bags a run, above what a car carries. **The savings split is half the revenue, so the price promise and the margin are the same number.** That number has to be measured at Tawfeer MAX.

**The savings split is visible.** Every bag comes with a slip with three columns (shelf price, what we paid, what you paid), plus a copy of the run's pooled till receipt with the household's lines marked. The customer pays the single-item shelf price minus half the bulk saving. This answers the panel's #1 objection, 40 of 50 asking for the receipt or proof of no markup. It is not a hidden markup, because the slip shows it.

### 2. The ladder

| rung | what you get | price | why step up |
| --- | --- | --- | --- |
| **Pickup bag** | twice-weekly staples run, collect at the partner shop 5–9 p.m. or next morning | $1.25 + half the saving | the default |
| **Doorstep** | same, left at your door on the driver's loop | +$1.50 | for car-less, older or late-working households: the only group that bought |
| **Basket Club** (only after 3 months of data) | unlimited pickup bags + weekly settlement + "same as last time" standing order | ~$4 a month (to test) | once a household orders ~3 bags a month, the club is cheaper than 3 fees |

Don't launch the club on day one. Memberships only work once the weekly habit exists (`research/business-model.md` §1.4, §1.9).

### 3. The opening offer

- **First bag: no fee.** It costs about $1.25 × ~60 households, $75–175 in total, budgeted in `numbers.json` startup. It answers "the fee is a sure cost and the saving is a maybe" (P025) by showing the saving on the slip before asking for a fee.
- **Founding households (the first 40):** weekly settlement from their 3rd bag instead of paying at each pickup. This partly answers the dekkene-tab objection (24 of 50) without open-ended credit. The cap is real: the cash float only covers about 40 households.
- It ends when the 40 places fill, or at the end of the pilot month, whichever comes first. No fake countdown.

### 4. What to test with real buyers

1. **$1.25 vs $1.50**, one per village cluster (e.g. Kfoun + Ghalboun at $1.25, Bejjeh + Aabaydat at $1.50) for 4 weeks. Measure first-bag → second-bag conversion. The CFO shows $1.50 adds ~$430 to year 1 if conversion holds ($769 → $1,199).
2. **Flat fee vs 3% of bag value** (min $1, max $2.50) on half the founding households, if baskets vary a lot in size.
3. **Real tier capture:** for every run, log the share of bag value that hit a PV2/PV3 price and the average gap. This decides whether the model works at all.

### 5. The panel's own words on price (top three)

- "The $2 is a sure cost while the savings are only a maybe." (P025)
- "A $2 fee on a small daily bag eats whatever I would save, and I lose the tab and the fresh bread I pick up when I need it." (P010)
- "Another fee on top of my groceries. I pass Spinneys and Tawfeer MAX anyway, so I would be paying $2 just to have someone else do what I already do, and I have no proof the bulk prices come out lower than the fee." (P006)

Simulated buyers. These pick what to test; they are not proof.

## The offer

Method: the Offers lens in `.claude/skills/founder-board/lenses.md`, a summary of a published framework, not anyone's words. Inputs: `panel/results.md` (v1 panel, 3 buy · 47 pass), `competitors.md`, `numbers.json`, `board.md`.

### 1. The problem list (in the buyers' words; counts are from the 50 v1 answers)

**Before buying**
1. "How do I know they didn't add a little on top of the till?" *(40 of 50 mention receipts, till price or markup)*
2. "The $2 is a sure cost while the savings are only a maybe." *(39 mention the fee)*
3. "I don't know who these people are." *(36 mention a stranger, trust or a neighbour)*
4. "I'm five minutes from Tawfeer, I can see the shelf price myself."
5. "The dekkene owner is my neighbour and lets me pay at the end of the month." *(24 mention a tab, credit or month-end)*
6. "Sending a list before 2 p.m. every time is a hassle." *(14)*
7. "I send voice notes, I don't type lists." / "I'm not comfortable with WhatsApp."
8. "I need small things every day, not a big bag."

**While it's being bought**
9. "Someone else picking my tomatoes and meat." *(15 mention produce or meat)*
10. "The wrong size, the wrong brand."
11. "If it's out of stock, who decides what I get instead?"
12. "I won't know what I'm paying until the pickup."
13. "The total will change after I've ordered."

**After**
14. "I'd still have to collect it at their hour, not mine." *(38 mention pickup, the hour or collecting)*
15. "No car: who carries the bag home from the pickup point?" *(15 ask for delivery)*
16. "A rotten or damaged item, and who do I argue with?" *(10)*
17. "Paying cash on the spot, mid-month, when money is tight."
18. "What happens to my bag if I'm late?"
19. "Is the labneh still cold at 8 p.m.?"
20. "Who sees my list and my number?"

### 2. Solutions, scored (value to buyer 1–5 / cost to deliver 1–5)

| # | solution | value | cost | keep? |
| --- | --- | ---: | ---: | --- |
| 1, 4 | **A copy of the run's pooled till receipt in every bag, with the household's lines marked, plus a 3-column slip (shelf price / what we paid / what you paid).** One receipt per run, because the items are bought together (`ops.md`); a photocopy per bag costs pennies, inside the $0.15 packaging line. | 5 | 1 | **core** |
| 2 | **First bag with no fee**: the saving is shown before any fee is asked | 4 | 1 | **bonus** |
| 2 | **Fee $1.25** (panel indifference $1.01), not $2 | 4 | 2 | **core** |
| 3 | **A named neighbour runs it; the pickup is at the village's own mini-market** | 5 | 1 | **core** |
| 5, 17 | **Weekly settlement after the 3rd bag**, capped at 40 founding households | 4 | 2 | **bonus** |
| 5 | Open-ended monthly tab | 4 | 5 | dropped: the float can't carry it |
| 6 | **Twice-weekly runs, list by 9 p.m. the night before, "same as last time" standing order** | 5 | 1 | **core** |
| 6 | Daily runs | 3 | 5 | dropped: kills density (v1 lost $7,498) |
| 7 | Voice notes accepted and read back; or order in person at the host shop | 4 | 2 | keep |
| 8 | Daily top-ups | 2 | 5 | dropped: that stays the dekkene's job |
| 9 | **No fresh produce or meat in the basket** | 5 | 1 | **core** (removes the problem) |
| 10, 11 | **Line rules: brand and size locked; every line marked "similar OK / skip / ask me"** | 5 | 1 | **core** (board condition C4) |
| 12, 13 | **Item list + estimated total sent before the run; the final can't exceed it by more than 10% without your OK** | 4 | 2 | keep |
| 14 | **Pickup 5–9 p.m. or the next morning** (the host shop's hours) | 5 | 1 | **core** |
| 15 | **Doorstep drop on the loop, +$1.50** | 5 | 3 | **bonus** (paid), aimed at the only segment that bought |
| 15 | Free home delivery | 5 | 5 | dropped |
| 16 | **Check at pickup: hand back anything wrong or damaged and you don't pay for it; replaced on the next run** | 5 | 2 | **guarantee** |
| 18 | Bag held until next morning; uncollected after that returns to stock, fee only | 3 | 1 | keep |
| 19 | Dairy in cool boxes; host-shop fridge | 3 | 2 | keep |
| 20 | One-line privacy note: the list is used for your order only | 3 | 1 | keep |
| — | Price comparison across 5–6 stores | 2 | 4 | dropped: measured gain 3–6% (`research/suppliers.md`), each store adds a stop |

### 3. The stack

- **The core, described by the outcome:** *your Tawfeer stock-up, done for you twice a week. You never pay more than the shelf price, and the receipt in the bag proves it.*
- **Bonuses, each killing one objection:**
  1. *First bag, no fee* kills "the fee is sure, the saving is a maybe".
  2. *Doorstep drop for $1.50* kills "no car, who carries it home".
  3. *Weekly settlement from your 3rd bag* (founding households) kills "I lose my tab".
- **The guarantee:** check your bag at pickup; anything wrong or damaged, hand it back and you don't pay for it. **Cost, modelled with the CFO's tool:**
  - base write-offs: 0.5% of bag value, which leaves year 1 at $769 (with the `ops.md` cost corrections);
  - write-offs doubled to 1%: year 1 **$288**, break-even 15 bags a run;
  - tripled: year 1 **−$194**, break-even 18.
  - Shelf-stable refused items mostly go back to stock or to the host shop, so the base case is the realistic one. The guarantee is affordable only while write-offs stay near 0.5%, which is why there is no fresh produce. Track it weekly (`launch.md`).
- **Urgency and scarcity, true ones only:** 40 founding places (the cash float really covers about 40 households), and the first-bag offer ends with the pilot month.
- **The name of the offer:** *The Twice-Weekly Stock-Up, receipt in every bag.* The brand name is `/founder-brand`'s job.

### 4. Value-equation scores (1–10)

| element | v1 pitch | v2 offer | what moved it |
| --- | ---: | ---: | --- |
| Dream outcome | 4 ("cheaper, maybe") | 6 | outcome stated as "your stock-up done, never above shelf price" |
| Perceived likelihood | 2 (strangers, no proof) | 6 | receipt + slip, a named neighbour, the village shop as host, refuse-at-pickup |
| Time delay | 6 (same day) | 5 | twice-weekly instead of daily; fine for stock-ups, worse for urgent items |
| Effort and sacrifice (higher = less effort) | 3 | 6 | standing order, list the night before, a 16-hour pickup window or the doorstep, keep choosing your own produce, keep the dekkene |

### 5. Re-test

The new offer is in `pitch.md` (the old one is `pitch-v1.md`; the v1 panel is kept in `panel-v1/`). It was re-run on `/founder-consumer --quick` (20 buyers, same customer, same seed 2026). Result: see section 6, added after the run.

### 6. Re-test result (20 simulated buyers, same customer profile, seed 2026)

| | v1 pitch (50 buyers, `panel-v1/`) | v2 offer (20 buyers, `panel/`) |
| --- | ---: | ---: |
| **Buy rate** | **6%** (3 of 50) | **25%** (5 of 20) |
| Car-less households | 3 of 10 | 3 of 4 |
| Everyone else | 0 of 40 | 2 of 16 |
| Passes for "trust" | 9 of 47 (19%) | 1 of 15 (7%) |
| Passes for "price" | 4 of 47 | 1 of 15 |
| Passes for "habit" (already shops weekly / dekkene tab) | 12 of 47 (26%) | 7 of 15 (47%) |
| Fee indifference price (IPP) | $1.01 (fee $2.00 shown) | **$1.25** (fee $1.25 shown) |

**What moved:** the receipt + slip, the first bag with no fee and the village-shop pickup almost removed the trust and price objections. The two non-car buyers bought for exactly those reasons: "The first bag is free and the fresh things stay mine to choose, so I would try it for the cartons of oil, detergent and diapers" (P011); "The first bag has no fee and I can hand back anything wrong, so I'll try it once or twice" (P017). **What didn't move:** habit. Households that drive to Jbeil weekly still pass, and the offer should not chase them. **What's still asked for:** month-end payment from the first bag, and proof on the first slips that the saving beats the fee (P018: "she would stop after the first bag if the slips showed the saving was smaller than the fee").

**Read it honestly:** 20 buyers, every segment thin, simulated and agreeable. 25% is an upper bound that sits exactly on the plan's default bar. The real test is the 4-week pilot in `launch.md`. One design rule follows from P018: **the first slip must show a saving larger than the fee**, or the household is lost. That depends on the Tawfeer tier gap, the same number the CFO flags.

**Wording corrected after the re-test.** The 20 re-test buyers saw "every bag comes with the till receipt". Pooled buying produces one till receipt per run, not per bag (`ops.md`), so `pitch.md` now promises a copy of the run's receipt in every bag, with the household's lines marked, plus the slip. The trust mechanism is the same, but the change was not re-tested. Watch for it in the T2 sign-up conversations (`launch.md`).

## The numbers

### The CFO's note (read this first)

**The original pitch does not work.** Daily runs at a $2 fee, with the till price passed straight through (`numbers-v1.json`), need **30 bags a day** to break even against a car that carries about 20. They lose **$7,498 in year 1**.

**The redesigned version (v2) is a thin, founder-run micro-business.** Costs here include the corrections from `ops.md`: fuel $8 a run, insurance and accountant placeholders, and a float for two runs.
- **The margin.** Each bag brings in $2.80: a $1.25 fee, plus half of the bulk saving (~$1.10), plus $0.45 average doorstep fees. Its own costs are $1.11, so each bag leaves **$1.69 (60%)**. Fixed costs are $178 a month. **Break-even is 12 bags a run.** At the plan of 20 bags a run, twice a week, the margin is **25%** and year 1 makes **$769** on operations.
- **That $769 is the founder's entire pay** for about 15 hours a week in the slow months and about 22.5 at plan (`ops.md`). That is **under $1 an hour.** With a paid half-day driver, break-even is **25 bags a run, above what a car carries**, and year 1 is **−$1,607**.
- **The line to watch is the bulk saving.** $1.10 of the $2.80 per bag is the business's half of the gap between Tawfeer MAX's single-item price and its quantity/carton price. It is unpublished and unmeasured. If pooled orders never reach the tiers, break-even is **34 bags a run** and year 1 is **−$1,122**.
- **Cash.** $2,975 to start. **$2,200 of that is a float** to front two runs before weekly settlement, and it comes back. Sunk spend is **$775**, roughly earned back by month 12 (−$6). The founder needs about **$3,100 in hand** at the low point. Requiring Whish prepayment at confirmation would cut the float to near zero. That is the cheapest cash lever.

**What the customer gets, in money.** On the base bag, the customer's half of the bulk saving (~$1.10) is slightly below the $1.25 fee, so a pickup bag costs about **$0.15 more than buying the same items at Tawfeer's shelf price yourself**. The customer is paying for the trip not taken (~$2.60 from Amchit, ~$6.90 from Bejjeh, a taxi for a car-less household; `research/market-lebanon.md` §3.3), not for a net discount. That is why only car-less and hill households buy (`offer.md` §6), and why no copy may claim a net saving unless the slip shows one (`marketing.md`). A bigger tier gap or bigger carton-heavy bags flip it to a real saving. T1 in `launch.md` finds out.

**Three ways to improve the margin (tool what-ifs, not guesses):**
1. **Fee $1.50 instead of $1.25:** year 1 rises from $769 to **$1,199** and break-even falls to 11. A $2.00 fee gives **$2,058** and break-even 9, but $2 is the panel's median "getting expensive". Test $1.25 against $1.50 (`pricing.md`).
2. **Keep the host commission at $0.25.** At $0.50, year 1 falls to **$339** and break-even rises to 14.
3. **Fill the vehicle, then grow it.** Fuel and the fixed costs are spread over bags. A 40-bag van with a paid driver earns **$1,082** in year 1 on a 26-bag break-even, before van rent, which is not quoted. Don't do it until runs reliably exceed 20 bags.

**Sensitivity** (`numbers.json`, tool): price −10% gives $288; volume −20% gives $188; volume −40% gives **−$393**; unit costs +15% give $483. The business survives a bad month but not a bad quarter.

**Board conditions about money (`board.md`):**
- **C1 (prove the gap): not met.** It hinges on the unmeasured tier gap; `launch.md` test T1 measures it in the first week.
- **C8 (who fronts the cash): answered.** It is a $2,200 float, or Whish prepayment.
- **C9 (density): defined.** 12 bags a run is break-even, roughly 36 regular households ordering 3 bags a month.
- **C2 (supply terms that don't depend on public promos): partly met.** MAX tiers are permanent public prices, not promotions, but they are still Tawfeer's to change.

**What this is:** a low-risk experiment with about $775 at risk. It is not a living. Its value is the proof it creates: a measured, pooled village channel, which is what `tawfeer-pitch.md` and `business-plan.md` build on.

Revenue is before tax. Lebanon's VAT registration threshold is LBP 5bn turnover (~$55,900) (`research/market-lebanon.md`). As a fee-paid buying agent this business may count only its fees; as a reseller the whole basket counts. Confirm which with an accountant. An accountant should check the structure, any payroll, and tax before money moves. Not financial, tax or legal advice.

---

## Unit economics: Village Basket v2: twice-weekly staples run, founder drives, receipt-backed savings split

Every number below comes from the input file. Nothing is looked up or guessed.

### One bag

| line | per bag |
| --- | ---: |
| Price | $2.80 |
| Bags, labels, printed receipt and savings slip (est.) | -$0.15 |
| Pickup-host commission to the partner mini-market (proposed) | -$0.25 |
| Payment fees and cash shortfalls, ~0.6% of a $55 bag (est.) | -$0.33 |
| Refused or damaged items written off, ~0.5% of a $55 bag (est.) | -$0.28 |
| Doorstep drops: extra fuel and time, averaged over all bags (est.) | -$0.10 |
| **Contribution** (what each bag leaves to pay the fixed costs) | **$1.69** (60%) |

### The margin that matters

Fixed costs: $178 a month (Fuel, ~60 km run day at $8 a run x 9 runs (ops.md estimate) $72, Software, lean stack $16, Business phone line and data (est.) $10, Crates, cool boxes, wear (est.) $15, Printed flyers and village posters (est.) $20, Vehicle wear and commercial-use insurance, placeholder until quoted (ops.md) $20, Accountant, ongoing bookkeeping, placeholder until quoted (est.) $25).

- **Break-even: 12 bags a day.** Below that you lose money every month.
- **Profit margin at your plan** (20 a day): **25%** of every sale, after every cost.
- Capacity: 20 a day.

### Year 1, month by month

| month | bags a day | revenue | profit | cumulative (after $2,975 startup) |
| ---: | ---: | ---: | ---: | ---: |
| 1 | 6 | $151 | -$87 | -$3,062 |
| 2 | 9 | $227 | -$41 | -$3,103 |
| 3 | 12 | $302 | $5 | -$3,098 |
| 4 | 14 | $353 | $35 | -$3,063 |
| 5 | 16 | $403 | $65 | -$2,998 |
| 6 | 17 | $428 | $81 | -$2,917 |
| 7 | 18 | $454 | $96 | -$2,822 |
| 8 | 19 | $479 | $111 | -$2,711 |
| 9 | 20 | $504 | $126 | -$2,584 |
| 10 | 20 | $504 | $126 | -$2,458 |
| 11 | 20 | $504 | $126 | -$2,332 |
| 12 | 20 | $504 | $126 | -$2,206 |

- **Year 1 operating profit: $769** on $4,813 of revenue.
- After the $2,975 startup spend: -$2,206.
- Startup money earned back: not within year 1.
- Cash you need before it pays for itself: **$3,103**.

### What if

| scenario | margin at plan | break-even a day | year 1 profit |
| --- | ---: | ---: | ---: |
| Base plan | 25% | 12 | $769 |
| Price -10% | 17% | 15 | $288 |
| Volume -20% | 16% | 12 | $188 |
| Unit costs +15% | 19% | 13 | $483 |

### Red flags

- The startup spend is not earned back within year 1.

## Marketing

Inputs: `panel-v1/results.md` (50 buyers, 6% buy), `panel/results.md` (20 buyers, 25% buy), `offer.md`, `pitch.md`, `pricing.md`, `competitors.md`, `numbers.json`, `cfo.md`, `research/market-lebanon.md`. Panel answers are simulated. They are research, never customer quotes.

### 1. Who to talk to first

- **Car-less households buy. Almost nobody else does.** v1: 3 of 10 car-less households bought, 0 of the other 40. v2: 3 of 4 car-less, 2 of the other 16. Every car-less buyer gave the trip as the reason.
- **The other two v2 buyers (P011, P017)** bought for the free first bag, keeping their own fresh food and the hand-back rule, for cartons of oil, detergent and diapers.
- **Habit doesn't move.** Habit passes rose from 26% to 47%; weekly big-shop households bought 0 of 4, commuters 0 of 3. We spend nothing on weekly drivers.
- **Where:** Bejjeh, Ghalboun, Aabaydat and Kfoun, plus car-less households in Amchit.

**An honest limit on the saving.** On the CFO's average bag, the customer's half of the bulk saving (~$1.10) is slightly below the $1.25 fee. So we never claim "you save money" after the fee. We claim what the slip proves: never above the shelf price, one visible fee, no trip. Bigger carton bags push the saving above the fee, so every message names the heavy staples.

### 2. Positioning

| | Line | Panel evidence |
|---|---|---|
| **A, recommended** | For households in Amchit and the villages above it **with no car at home**, who now need "a taxi or a lift" to get oil, rice, detergent and milk from Jbeil, Village Basket is **the twice-weekly neighbour's run** that leaves their stock-up at the village shop or their door, **at no more than the Jbeil shelf price plus one visible fee**, unlike a taxi, a favour or the dekkene's carton prices. | 6 of the 8 buyers across both panels are car-less. The car-less buy rate is 30–75%; everyone else's is 0–13%. |
| B | For hill-village households who suspect any shopper adds "a little on top of the till", Village Basket is the village buying run with **the till receipt and a three-column slip in every bag**, unlike delivery apps, whose fees and mark-ups aren't published. | Receipt/markup: 40 of 50 answers. Trust passes fell from 19% to 7% with the slip, but nobody bought for the receipt alone. |
| C | For village families who **buy their cartons at the dekkene and pay extra**, Village Basket is the twice-weekly carton run that brings Jbeil's quantity prices to the village shop while they **keep choosing their own fresh food**. | P011 and P017 only: thin. |

**Use A as the position, B's receipt as the proof in every message, C as the second message** (counter sign, post 2). B alone chases the habit-bound 47%; C rests on two simulated buyers.

### 3. Channels: three to start

| Channel | Why it fits | Cost | How we know it worked |
|---|---|---|---|
| **1. Village, parish and municipality WhatsApp groups**, posted by the admin or with their OK, plus our own WhatsApp Business Status and an opt-in broadcast list | People "read the village and parish WhatsApp groups every day". WhatsApp is already how they talk to shops (`market-lebanon.md` §8). | $0 | Every first order is asked "how did you hear?" Aim for at least 2 reservations per post per village. |
| **2. The partner mini-market** in each village: counter sign, flyers at the till, the owner's word, orders taken in person | The bag is collected there, and the owner is the trusted neighbour. Recruiting the dekkene is the defence against it copying us (`competitors.md` §6). | Printing only. The $0.25 a bag is already in costs. | Share of first orders that say "the shop" |
| **3. The people who know who has no car**: mukhtar, municipality, parish committee (in Amchit's mixed neighbourhoods, the local community figures), then word of mouth from households served | They reach older and car-less households that no ad can find. "A neighbour I know vouching" comes up again and again in both panels' flips. | Time | Car-less share of first orders: at least 60% |

**What we are not doing:**
- **No paid social at launch:** a few hundred households in four villages, $20 a month, many older buyers.
- **No app or website:** WhatsApp is the habit; board condition C5 says pilot by hand.
- **No Instagram/TikTok content** (reserve the handles), creators, paid search or Google Maps listing (no storefront).
- **No targeting of weekly drivers or commuters.**
- **No discounts beyond the first bag:** "volume bought with discounts leaves with the discounts" (`competitors.md` §7).
- **No posting without a group admin's OK;** at most two posts a week per group.
- **No political or religious symbols;** the same respectful message in every village.

### 4. The offer and its end date

- **First bag: no fee. Doorstep: +$1.50. The first 40 founding households** settle weekly from their 3rd bag.
- **Ends** when 40 places fill or after the **Friday 5 February 2027 run** (end of the pilot month), whichever is first. Every posted count is true; no fake countdown.
- **Fee test** (`pricing.md`): Kfoun, Ghalboun and Amchit flyers say $1.25; Bejjeh and Aabaydat flyers say $1.50. If asked, say openly that two fees are being tried for four weeks.

### 5. Ten hooks, each answering a named objection

| # | Objection (panel count) | Format | English | Lebanese Arabic |
|---|---|---|---|---|
| 1 | Markup, "did they add on top of the till?" (40/50) | Flyer headline | A copy of the supermarket's till receipt is in every bag, with your items marked. Check every price yourself. | نسخة عن فاتورة السوبرماركت بكل كيس، وغراضك معلّمين عليها. شيّك عَ كل سعر بعينك. |
| 2 | The fee is sure, the saving a maybe (39/50) | Group post, first line | Your first bag has no fee. See the difference on the slip before you pay us anything. | أول كيس بلا رسم. شوف الفرق عالورقة قبل ما تدفعلنا ولا قرش. |
| 3 | Pickup at their hour (38/50) | Counter sign | Collect at your village shop, 5 to 9 p.m. or the next morning. Or at your door for $1.50. | بتستلم من دكانة ضيعتك من 5 لـ 9 المسا أو تاني يوم الصبح. أو عَ بابك بـ 1.50$ زيادة. |
| 4 | "I don't know these people" (36/50) | Group post sign-off | I'm [Name] from Amchit. I do the shopping myself, and this is my own number. | أنا [الاسم] من عمشيت. أنا بنزل بشتري بإيدي، وهيدا رقمي الشخصي. |
| 5 | Losing the dekkene tab (24/50) | 1-to-1 message | First 40 households: from your 3rd bag, settle once a week. | لأول 40 بيت: من تالت كيس، بتحاسب مرّة بالجمعة. |
| 6 | No car, who carries it home (15 asked for delivery; every car-less buyer) | Flyer headline | No car at home? Your oil, rice and detergent come up the hill twice a week. No taxi, no favour to ask. | ما في سيارة بالبيت؟ الزيت والرز والمسحوق بيطلعولك عالضيعة مرّتين بالجمعة. بلا تاكسي وبلا جميلة حدا. |
| 7 | "Someone else picking my tomatoes and meat" (15/50) | Counter sign | We don't pick your tomatoes or your meat. Just the heavy staples. Keep buying your bread here. | ما منختارلك لا بندورة ولا لحمة. بس الغراض التقيلة. وخبزك ضلّ اشتريه من هون. |
| 8 | A rotten or damaged item (10/50) | Status image | Wrong or damaged? Hand it back at pickup and you don't pay for it. | في شي غلط أو مخبوط؟ رجّعو وقت الاستلام وما بتدفع حقّو. |
| 9 | Wrong brand or size; "the total will change" | Group post | Your brand, your size. You get the list and an estimated total before we shop, and it can't go more than 10% over without your OK. | نفس الماركة ونفس الحجم. منبعتلك اللايحة والمجموع التقريبي قبل ما نتسوّق، وما بيزيد أكتر من 10% بلا موافقتك. |
| 10 | "Sending a list is a hassle"; "I send voice notes" (14/50) | Status / 1-to-1 | Send a voice note, or just reply "same as last time". | بعتلنا فويس، أو بس قول: "متل المرّة الماضية". |

Write the Arabic with Western digits, the way the till receipt prints them. Never use the noun توفير. It is the supplier's trademark, so write الفرق ("the difference") instead.

### 6. The calendar: Tuesday 29 Dec 2026 to Thursday 28 Jan 2027 (launch Tuesday 12 Jan)

Runs are on Tuesdays and Fridays. Lists close at 9 p.m. the night before.

| Date | Channel | What goes out or gets done |
|---|---|---|
| Tue 29 Dec (L−14) | In person | Sign up host shops in Bejjeh, Ghalboun, Aabaydat, Kfoun and Amchit: $0.25 a bag, counter space, a fridge shelf. Owners tell car-less customers; you collect no names. |
| Wed 30 Dec (L−13) | In person | See the mukhtar or municipality in Bejjeh and Ghalboun and ask the group admins to OK posts on 4 and 8 Jan. Set up WhatsApp Business (`brand.md`). |
| Thu 31 Dec (L−12) | — | No posts (New Year's Eve). Get print quotes. Make one flyer per village with that village's fee. |
| Fri 1 Jan (L−11) | — | Holiday. Nothing goes out. |
| Sat 2 Jan (L−10) | In person | Aabaydat, Kfoun and Amchit: mukhtar or municipality, and parish committee (in Amchit's mixed areas, the local figures). Same neutral message everywhere. |
| Sun 3 Jan (L−9) | Host shops | Counter signs go up (hooks 3 and 7). Flyers at each till. |
| Mon 4 Jan (L−8) | Village groups, Status | **Post 1:** hook 6, how it works, the village's fee, "40 founding places, reply to reserve". |
| Tue 5 Jan (L−7) | Status | Dry run: buy your own list of about 15 staples and price the tiers (the CFO's number). Post your own real receipt and slip, labelled "sample: my own shopping, 5 Jan". |
| Wed 6 Jan (L−6) | — | Public holiday (Epiphany / Armenian Christmas). No promotion. Answer replies only. |
| Thu 7 Jan (L−5) | 1-to-1 | Write to everyone who replied: how to order, voice notes welcome (hook 10), the privacy line. In Amchit, host shop and parish pass on the doorstep flyer (hook 3). |
| Fri 8 Jan (L−4) | Village groups | **Post 2:** hook 7, plus hook 8. |
| Sat 9 Jan (L−3) | Status | "How a bag works" in four photos: list, estimate, crate, slip (hook 9). |
| Sun 10 Jan (L−2) | Village groups | **Post 3:** hook 2. "First run Tuesday 12 Jan, lists by 9 p.m. Monday." True count of places left. |
| Mon 11 Jan (L−1) | Broadcast | 5 p.m. reminder. Lists close at 9 p.m. By 10 p.m., send each household its items and estimated total. |
| **Tue 12 Jan (LAUNCH)** | Run 1 | Shop, pack, label. Bags at host shops by 5 p.m., then the doorstep loop. Status: crates loading. Evening: thank each household; ask them to check slip against receipt. |
| Wed 13 Jan (L+1) | 1-to-1 | Morning pickups. Ask every first-bag household "did everything match?" Log every hand-back and its cause. |
| Thu 14 Jan (L+2) | Village groups | "Friday's run: lists by 9 p.m. tonight. Founding places left: X of 40." |
| Fri 15 Jan (L+3) | Run 2, Status | The cool box for dairy. |
| Sat 16 Jan (L+4) | Status | Behind the scenes: brand and size locked, the "similar OK / skip / ask me" marks. |
| Sun 17 Jan (L+5) | Internal | **Weekly numbers #1** (section 8). |
| Mon 18 Jan (L+6) | 1-to-1 | To first-bag households: "Same as last time for tomorrow?" (hook 10). |
| Tue 19 Jan (L+7) | Run 3, groups | **Post 4:** real week-1 totals (bags, hand-backs, average slip difference). If below the fee, say "about the shelf price, without the trip". Never round up. |
| Wed 20 Jan (L+8) | In person | Visit each host shop: what customers say. Replace worn signs. |
| Thu 21 Jan (L+9) | Village groups | **Post 5:** hook 1, plus hook 9. |
| Fri 22 Jan (L+10) | Run 4, Status | "Item of the week": one carton price from this week's real receipt, shelf price against quantity price. |
| Sat 23 Jan (L+11) | 1-to-1 | Ask regulars once whether they know a household without a car. They forward the flyer in their own words. No reward, no script. |
| Sun 24 Jan (L+12) | Internal | **Weekly numbers #2.** First read of the $1.25 vs $1.50 second-bag rates. Too early to decide. |
| Mon 25 Jan (L+13) | Amchit groups | Hooks 6 and 3 (doorstep $1.50) for car-less Amchit households. |
| Tue 26 Jan (L+14) | Run 5, 1-to-1 | Founding households reaching their 3rd bag: explain weekly settlement (hook 5). |
| Wed 27 Jan (L+15) | In person | Second round with the mukhtars and parishes: share the real totals and ask them to mention it again. |
| Thu 28 Jan (L+16) | Village groups | "Places left: X of 40. The no-fee first bag ends after the Friday 5 Feb run." Weekly numbers #3 on Sunday 31 Jan. |

**When there is nothing new to post:** the 7 a.m. run, the cool box, labelled crates, a slip checked against its receipt, one real carton price of the week, the host shop's counter (with the owner's OK). Never a customer's face, name or basket.

### 7. Budget, and the most we can pay to win a household

**Budget split:**

| Line | Amount |
|---|---|
| First-bag fee waivers (~60 bags × $1.25) | ~$75 |
| Launch printing: 5 laminated counter signs, ~400 black-and-white A5 flyers, sample slips (est.; get a quote in Jbeil) | ~$100 |
| Monthly reprints (`numbers.json`) | $20 |
| Paid ads | $0 |

That is $175 at launch, plus $20 a month.

**The most we can pay to win a household:**
- Contribution per bag: **$1.69** (`cfo.md`).
- Bags per regular household: **3 a month**. The CFO's plan of 180 bags a month comes to about 60 households, and v2 buyers said 2.6 bags in their first month.
- **Retention assumption, not measured:** a household that takes a second bag stays **6 months** on average, so about 1 in 6 regulars stops each month. The pilot measures this.
- **Ceiling:** $1.69 × 3 × 6 = **$30.42 per regular household**. Spending above that loses money.
- **Working cap: $10 per regular household**, which is two months of contribution ($1.69 × 3 × 2 = $10.14). Cash is tight and retention is a guess. If half of first bags turn into regulars, a trial is worth up to **$5**.
- **Stress tests:** 3 months' retention gives a $15.21 ceiling; if the bulk tiers are never reached, contribution falls to $0.59, giving $0.59 × 3 × 6 = $10.62 (working cap ~$3.50).
- **The plan's actual spend:** ($175 + $20) ÷ 60 households ≈ **$3.25 per household**, under every cap.

### 8. Three numbers to watch every Sunday

| Number | Watch | Change something when… | What to change |
|---|---|---|---|
| **Bags per run** (average of the week's two runs) | Break-even is 9. The plan ramps to 6 a run in month 1, 9 in month 2 and 20 at plan. | Under 6 in week 3, or under 9 by week 6. Above 20 means the car is full. | Under target: another host shop, the Amchit car-less push, a second mukhtar round. Above 20: stop recruiting. |
| **Second-bag rate** (first-bag households that order again within 14 days), split by $1.25 and $1.50 | The pricing test reads this number | Under 50% | Call every household that didn't come back and ask why. Check their slip against their receipt. |
| **Difference per bag on the slip** (shelf total minus what we paid; half goes to the customer) | The CFO assumes ~$2.20 in total, ~$1.10 to each side | Our half averages under $0.80 a bag, or the customer's half is below the fee on more than half the bags (P018 stops after one such slip) | Push carton items and bigger bags. Re-price the tiers. Raise it with Tawfeer (`tawfeer-pitch.md`). |

### 9. Rules

- No fake reviews, testimonials, follower counts or "as seen on". Panel quotes never appear in any message.
- Every saving claim must be on a real slip. Always show the fee (Law 659/2005, consumer protection; not legal advice).
- **Disclose the paid partner:** each counter sign says "[Shop] is our pickup point and is paid per bag."
- **The supplier's name** (Tawfeer MAX Jbeil) appears only as a fact in how-it-works text and on slips: never in a headline or logo, never with its colours, no implied partnership until one exists in writing.

Next: `/founder-brand`, then `/founder-launch`.

## Brand

The brief, from `marketing.md`:
- **Audience and position:** car-less households in Bejjeh, Ghalboun, Aabaydat, Kfoun and Amchit. "The twice-weekly neighbour's run … at no more than the Jbeil shelf price plus one visible fee." Proof: the till receipt in every bag.
- **Why buyers bought** (`panel/results.md`): no car, the free first bag, pickup at their village shop, keeping their own fresh food, the hand-back rule.
- **Stay clear of** (`competitors.md`): the delivery-app look and the supplier's name and colours.

### 1. Ten name candidates

| # | Name | Style | What it says, how it sounds | On a sign / 32px icon | Risk |
|---|---|---|---|---|---|
| 1 | **Village Basket** | Descriptive, English | What it is; foreign to older villagers | Long; weak icon | Generic; villagebasket.com taken |
| 2 | **Sallet el-Jiran** سلّة الجيران | Descriptive and evocative, Arabic | "The neighbours' basket": pooled, run by a neighbour. Warm, natural | Strong sign; icon needs a mark | Common words: protection comes mostly from the logo |
| 3 | **Sallet el-Day'a** سلّة الضيعة | Descriptive, Arabic | "The village basket" | Fine | Very generic; Amchit-town may not feel like a ضيعة |
| 4 | **Wasla** وصلة | Evocative, Arabic | "A lift": what car-less people ask for. Two syllables | Excellent icon | Suggests passenger rides; likely used regionally; wasla.com taken |
| 5 | **Mishwar** مشوار | Evocative, Arabic | "The errand we make for you" | Good | Very common; weak to protect |
| 6 | **Mouneh** مونة | Evocative, Arabic | "Household provisions" | Good | Promises homemade preserves we don't sell; crowded |
| 7 | **Tlata w Jem'a** تلاتا وجمعة | The schedule | "Tuesday and Friday": says when | Long | Locks the schedule |
| 8 | **Sallitna** سلّتنا | Coined, Arabic | "Our basket" | Good | May be in use regionally |
| 9 | **[First name]'s Basket** سلّة [الاسم] | Founder's name | A named neighbour (stranger objection, 36/50) | Fine | Ties the business to one person |
| 10 | **Amchit Basket** سلّة عمشيت | Place | Where it comes from | Fine | Hill villages may feel it isn't theirs; limits expansion |

Rule for every name: **nothing from the root و-ف-ر** (توفير، وفّر، وفرة). توفير is the supplier's trademark. Also nothing close to Toters, noknok, Le Charcutier, Spinneys, Carrefour or InstaShop.

### 2. The shortlist, and the checks you must finish yourself

1. **Sallet el-Jiran, سلّة الجيران (recommended).** It names what sold: a neighbour, and a basket collected in your own village. Neutral in every village. English gloss: "the Neighbours' Basket".
2. **Wasla, وصلة.** The sharpest name for car-less households, but the most likely to clash with an existing mark.
3. **Sallet el-Day'a, سلّة الضيعة.** Keeps continuity with "Village Basket", the bilingual working name.

**Trademark (Lebanon):**
- **Where:** the Intellectual Property Protection Office, Ministry of Economy and Trade (Azarieh building, Beirut). Official page: <https://www.economy.gov.lb/en/news/registering-a-commercial-or-industrial-trademark> (found by search; it returned a bot check to my reader, so open it in a browser). Contacts: <https://www.wipo.int/en/web/country-profiles/contact?code=lb>. A WIPO country profile says the ministry's site offers a trademark search; if you can't find it, ask the office or a Lebanese trademark agent.
- **Search** the Arabic form, the Latin spellings (Sallet el Jiran, Sallit al-Jiran, Salet Jiran) and, later, the logo.
- **Classes:** 35 (buying goods for others, retail-type services) and 39 (delivery, packaging and storage of goods), plus 42 if the software is ever licensed. Confirm with the office.
- **Regional marks:** <https://branddb.wipo.int> (WIPO Global Brand Database), for example Gulf apps named Wasla.

**Domains** (checked 17 Nov 2026 by RDAP lookup at Verisign for .com and at LBDR, the Lebanese registry, for .com.lb):

| Name | .com | .com.lb |
|---|---|---|
| Sallet el-Jiran | salletjiran.com, salletejiran.com, salletaljiran.com: **no record** | salletjiran.com.lb: **no record** |
| Wasla | wasla.com: **registered**; waslabasket.com: no record | wasla.com.lb: no record |
| Sallet el-Day'a | salletdaya.com, salletelday3a.com: no record (villagebasket.com: **registered**) | salletdaya.com.lb, villagebasket.com.lb: no record |

- **"No record" is not "available"**: names can be reserved or premium. Confirm at a registrar before paying.
- The LBDR lookup found google.com.lb, so its .com.lb answers are meaningful. Bare .lb names couldn't be checked (even google.lb returned nothing).
- LBDR (<https://www.lbdr.org.lb>) may ask for a Lebanese trademark or commercial registration for a .com.lb. Check its current rules: one more reason to file the trademark first.

**Handles:** search @salletjiran and @sallet.eljiran on Instagram and TikTok. I could not check them from here. Reserve them now, even though `marketing.md` posts nothing there. WhatsApp Business display name: "سلّة الجيران · Sallet el-Jiran".

**Plainly:** these are public lookups only. A Lebanese trademark agent or lawyer confirms the name, and nothing is yours until you file and it registers. This is not legal advice.

### 3. Promise, taglines, voice

**Promise:** *Every item at or below the Jbeil shelf price, plus one visible fee. In your village on the day we said, with a copy of the till receipt in the bag.*

Arabic: كل غرض بسعر الرف بجبيل أو أقل، وفوقن رسم واحد واضح. بضيعتك باليوم يلّي قلناه، ونسخة الفاتورة بالكيس.

(The promise names the fee on purpose. On the CFO's base bag the customer's half of the saving, ~$1.10, is below the $1.25 fee, so the total is not below shelf price; `cfo.md`.)

**Taglines:**
1. **"The receipt is in the bag."** «الفاتورة بالكيس.» **Recommended:** answers the top objection (40 of 50), works in every village.
2. "Jbeil prices, in your village." «أسعار جبيل، بضيعتك.» Flyer headline, always with the fee next to it.
3. "We bring the heavy stuff up the hill." «نحنا منطلّعلك التقيل.» For car-less messages.

**Voice:**

| Adjective | Do | Don't |
|---|---|---|
| **Neighbourly** | Write Lebanese Arabic as people speak it. Sign with your own name and village. Answer a voice note with a voice note | Formal فصحى, "dear valued customer", "we at…" |
| **Exact** | Days, hours, dollars, and the fee every time | "Huge savings", "best prices", "up to 30% off", any number that isn't on a real slip |
| **Modest** | Say what we don't do (no fresh produce, two runs a week). Own mistakes first | Hype, countdowns, rows of emojis or exclamation marks, naming other shops or apps |

**Before** (`pitch.md`): "You pay the normal single-item shelf price minus half of the bulk saving, plus $1.25 a bag, and no fee on your first bag."

**After:** "On every item we split the difference between the shelf price and what we paid: half for you, half for us. Then $1.25 for the bag. Your first bag: no fee."

Arabic: «عكل غرض منقسم الفرق بين سعر الرف واللي دفعناه: نص إلك ونص إلنا. وفوقن 1.25$ عالكيس. أول كيس بلا رسم.»

### 4. The look, as a brief

**Colour.** An earthy palette, the colours of a paper bag and a village kitchen:

| Colour | Hex | Job | Text contrast (WCAG 2.x) |
|---|---|---|---|
| **Carob** (خرّوب) | `#3B2314` | Wordmark and all body text | On Wheat **12.14:1**, on white **14.62:1** (passes AA and AAA) |
| **Wheat** (قمح) | `#F4E9D2` | Background of flyers, signs and WhatsApp images | Carob text 12.14:1; Za'atar text **6.21:1** (passes AA) |
| **Za'atar** (زعتر) | `#4E5A1E` | Accent: the "you pay" column, the band on signs, buttons | White text on it **7.49:1**, Wheat text 6.21:1 (passes AA). **Never Carob on Za'atar: 1.95:1, fails** |

- **Black only:** labels and photocopies are black on white (21:1), and the label printer is one colour, so everything must work in black.
- **Clear of competitors:** Tawfeer's red `#E70127` (its site also uses `#1439C7` blue) and Toters' teal-green `#00B392` and coral `#F0523D`, read from their sites' CSS on 17 Nov 2026. Our three colours sit well away from them.
- **Clear of politics:** in Lebanon some saturated solid colours read as party colours, and red-white-and-cedar reads as the flag. An earthy palette stays neutral in every village.

**Type.** Both faces are free on Google Fonts under the SIL Open Font License, which allows commercial use and logos. Keep the licence file.
- **Display: El Messiri** (Arabic and Latin), SemiBold for the wordmark and headlines.
- **Text: IBM Plex Sans Arabic** (Arabic and Latin), with clear digits for slips.
- **Backups:** Noto Naskh Arabic for long Arabic text; Tajawal and Reem Kufi also include Arabic (subsets checked on Google Fonts, 17 Nov 2026).
- **Western digits throughout**, matching the till receipt.

**Logo brief:**
- **What it says:** neighbours and a basket, Arabic first. The wordmark is سلّة الجيران in El Messiri, with "Sallet el-Jiran" smaller beneath.
- **The mark:** a simple woven basket whose handle is two arcs meeting, like two neighbours' hands or two village roofs.
- **Where it must work:** black only at 15 mm on a thermal label; a 32px circular WhatsApp avatar (mark only); an A4 counter sign readable at 3 m; a rubber stamp on plain paper bags (the cheapest branded bag); a black-and-white photocopy.
- **Avoid:** cedars, flags or any religious symbol; carts, scooters, riders and speed lines (the delivery-app look); "%" bursts and price tags (the discounter look); red, teal-green and coral; the supplier's name.
- **Concepts:** I can generate concepts with an image tool connected here. They would be concepts, not a finished logo. A designer finishes it, and you own the rights.

### 5. The first five touchpoints

**1. WhatsApp Business profile and first auto-reply**
- **Name:** سلّة الجيران · Sallet el-Jiran.
- **About:** "تلاتا وجمعة من جبيل لضيعتك".
- **Description:** "Twice-weekly staples run for Bejjeh, Ghalboun, Aabaydat, Kfoun and Amchit. Run by [Name] from Amchit."
- **Hours:** 8 a.m. to 9 p.m. No catalogue.
- **Greeting message:**

> أهلا وسهلا! أنا [الاسم] من عمشيت، وهيدي سلّة الجيران. منشتري الغراض التقيلة من جبيل كل تلاتا وجمعة، وبتستلمها من دكانة ضيعتك أو عَ بابك (+1.50$). بعتلي لايحتك كتابة أو فويس قبل الساعة 9 المسا اليوم يلّي قبل، أو قول «متل المرّة الماضية». برجعلك بكل غرض ومجموع تقريبي قبل ما إشتري. أول كيس بلا رسم. الفاتورة الأصلية بالكيس. لايحتك ورقمك منستعملن بس لطلبيتك.
>
> *Hi, I'm [Name] from Amchit. Tuesday and Friday runs; list (text or voice note) by 9 p.m. the night before. You get each item and an estimated total before I shop. First bag, no fee. Receipt in the bag. Your list and number are used for your order only.*

**2. Bag label** (thermal, black only, about 50 × 30 mm). It shows a first name and initial only, and never a phone number.

```
سلّة الجيران                               #07
Rita K. · غلبون Ghalboun · [Shop]
Tue 12 Jan · 14 items · COLD 2 (shop fridge)
Check it here. Hand back anything wrong.
```

**3. The slip** (80 mm thermal or A6). The numbers below are illustrative, not prices.

```
سلّة الجيران · Sallet el-Jiran          Bag #07 · Tue 12 Jan
Item / الغرض        Shelf/سعر الرف  We paid/دفعنا  You pay/بتدفع
Sunflower oil 1.8L        4.90          4.30          4.60
...                        ...           ...           ...
Items total              48.20         43.80         46.00
Bag fee / رسم الكيس                                    1.25 (first bag 0.00)
Doorstep / عالباب                                         —
TO PAY / المجموع                                      47.25
Your half of the difference / الفرق إلك: 2.20
"You pay" = halfway between shelf price and what we paid.
Till receipt attached. Anything wrong? Hand it back now: you don't pay for it.
[Name] · [number]
```

Print the "You pay" column in Za'atar or bold. Arabic labels sit right, English left; right-align every number.

**4. The first flyer and village-group post** (Ghalboun version; $1.25 fee)

> **ما في سيارة بالبيت؟** الزيت والرز والمسحوق والحفاضات بيطلعولك عَ غلبون كل تلاتا وجمعة.
> • عكل غرض منقسم الفرق بين سعر الرف بجبيل واللي دفعناه: نص إلك ونص إلنا. وفوقن 1.25$ عالكيس. **أول كيس بلا رسم.**
> • الفاتورة الأصلية بالكيس.
> • بتستلم من [الدكانة] من 5 لـ 9 المسا أو تاني يوم الصبح، أو عَ بابك بـ 1.50$.
> • شي غلط أو مخبوط؟ رجّعو وما بتدفع حقّو.
> أول 40 بيت بس. أول نزلة: التلاتا 12 كانون التاني. بعتلي لايحتك قبل الاتنين 9 المسا.
> [الاسم] من عمشيت · [الرقم] — [الدكانة] نقطة الاستلام، وبتاخد رسم صغير عن كل كيس.

A5 flyer: Wheat background, headline in Carob El Messiri, fee line in Za'atar, and one English line at the foot ("No car? Your heavy staples, twice a week. First bag, no fee."). The group post uses the same text, sent only with the admin's OK.

**5. Reply to the first complaint** (within an hour in the daytime; answer a voice note with a voice note)

> معك حق، وآسف. [الغرض] مش يلّي طلبتو. ما بتدفع حقّو: رجّعو للدكانة أو خلّيه عندك، وبجيبلك الصح بنزلة الجمعة بلا ولا قرش. وهيك بعمل من هلّق كرمال ما تتكرّر: [what changes]. [الاسم]
>
> *You're right, and I'm sorry. [Item] isn't what you ordered, so you don't pay for it. Return it or keep it; I'll bring the right one on Friday at no charge. From now on: [what changes]. [Name]*

Always: sorry first, the guarantee applied without being asked, the fix named, the case logged in the weekly numbers. Never argue in a group chat; move it to a private chat.

Next: `/founder-ops` and `/founder-launch`.

## Operations

How the twice-weekly staples run works on day one. Written 17 Nov 2026 from `offer.md`, `numbers.json`, `cfo.md`, `product-tech.md` and `research/`. **[EST]** = my estimate. **QUOTE** = only a supplier can price it. Not legal or tax advice.

**Read first:**
1. **One pooled till receipt per run, not one per bag.** Tier prices need a pooled purchase. Each slip cites its lines on that receipt, and the receipt photo goes out on WhatsApp. *(Done: the promise in `pitch.md` and `offer.md` is now "a copy of the run's till receipt in every bag, your lines marked". Add one photocopy per bag to the packing SOP.)*
2. **Weekly settlement doubles the float** (§8).
3. **At plan the founder works ~22.5 h a week for ~$1.30 an hour** ($126 a month operating profit at 20 bags a run, per `cfo.md` after the §8 corrections were applied). The legal minimum is ~$1.50 (`market-lebanon.md` §3.3).

### 1. The twice-weekly cycle

The table shows Mon → Tue; Thu → Fri runs the same way. ● = the customer sees this step.

| when | step | |
|---|---|---|
| Sun/Wed 18:00 | "Orders open" broadcast, plus tier near-misses (SOP-6) | ● |
| to Mon 21:00 | **Intake:** text, voice note, list photo, "same as last time", or paper left at the host. Every line is read back (SOP-1) | ● |
| Mon 21:00 | **Cut-off.** Late lists roll to Friday | ● |
| 21:00–22:00 | **Confirm:** items and an estimated total; changes allowed until 07:30 | ● |
| 22:00 | **Batch:** total per SKU, checked against the PV2/PV3 thresholds | |
| Tue by 08:00 | **Order sent to Tawfeer MAX** for pre-picking if they agree; otherwise the founder shops it | |
| ~10:00–11:00 | **Store:** check, apply the line rules, pay, photograph the receipt and shelf tags (SOP-2) | ● ("ask me" lines) |
| 11:00–12:45 | **Pack by village** at home in Amchit, dairy in the fridge (SOP-3) | |
| 12:45 | "Bag ready at [host] from 5 p.m." + slip photo | ● |
| 13:00–15:45 | **Loop:** the Amchit host and 4 hill hosts, plus doorstep drops | ● |
| 17:00–21:00, Wed to 12:00 | **Pickup:** check, refuse, pay (SOP-4) | ● |
| 21:00–21:45 | **Close:** run sheets, cash/Whish, ledger, photos (SOP-7) | |
| Wed | **Price-tier log** (SOP-6) | |

Times assume 20 bags (`launch.md` plans ~10). OSRM puts the loop at 61 min (`market-lebanon.md` §1.4); drive it and time it.

### 2. Suppliers

#### 2.1 Primary: Tawfeer MAX Jbeil (Qartaboun)

- 5,500 SKUs, open since May 2026. Permanent PV1/PV2/PV3 tiers; PV3 is aimed at "small businesses, neighborhood shops", with no membership. **No thresholds or tier prices are published** ([Beirut.com](https://www.beirut.com/en/?p=775677); `suppliers.md` §1.3).
- Contact: 1626, customerservice@tawfeer.market, the branch manager. Pitch: `tawfeer-pitch.md`.

**Ask, and get every answer in writing (board C2):**
1. **B2B invoice account:** in whose name? This decides agent vs reseller (§6).
2. **PV2/PV3 thresholds and prices** for the top ~50 SKUs, and a weekly list.
3. Do **mixed cartons**, or several households' units of one item, count?
4. Any **per-customer cap** on tier prices? Does PV3 require a registered business?
5. **Pre-pick** an order sent by 08:00, ready at ~10:00?
6. **Settlement:** pay at collection (cash, card or Whish?), weekly after a trial?
7. Do app prices match the shelf? Does the app deliver to the hill villages, and at what fee?

Minimum order, lead time and terms: **QUOTE**.

#### 2.2 Backups for out-of-stocks

Used only after a customer says yes to an "ask me" line. Charged at that store's shelf price, with no saving split.

| store | where | price level |
|---|---|---|
| **Spinneys Jbeil** | Jbeil highway (Blat/Mastita), ~3–5 km | ~10% dearer on shared staples (`suppliers.md` §4.2). [Online prices](https://www.spinneyslebanon.com/). The loyalty card is personal use only |
| **Le Charcutier Aoun** | Qartaboun per OSM; branch **not re-verified** | 12-item basket $78.94 vs Tawfeer $77.04 ([shop](https://lecharcutier.suppy.app/)) |

#### 2.3 Packaging and equipment

| item | supplier | price |
|---|---|---|
| Bags | **Poly Bags**, Batroun ([Kompass](https://us.kompass.com/c/poly-bags/lb005694/)); **INDEVCO**, Ajaltoun; **Bag-It SAL**, paper ([Kompass](https://ae.kompass.com/c/bag-it-sal/lb014054/)) | **QUOTE** for 1,000: minimum and lead time |
| Label printer | **NIIMBOT B21S**, 20–50 mm ([961souq](https://www.961souq.com/products/niimbot-b21s-bluetooth-thermal-label-printer)) | **$65** ex VAT, in stock 17 Nov; labels QUOTE |
| Slip printer | **Xprinter XP-TP4**, 4-inch thermal ([Ayoub Computers](https://ayoubcomputers.com/xprinter-xp-tp4-4-inch-portable-thermal-receipt-printer-usb-bluetooth/)) | **$20** (sale); paper QUOTE |
| Cool boxes, ice packs | **Azadea Lebanon** ([coolers](https://www.azadea.com/lb/en/sports/hike-and-camp/camp-kitchen/coolers)) | **QUOTE** |
| Folding crates | none found online | **QUOTE** (hardware shop) |

### 3. People

#### 3.1 Founder's hours [EST]

| per run | slow month (6 bags) | plan (20 bags) |
|---|---:|---:|
| Intake, read-backs, confirmations | 0.8 h | 1.7 h |
| Cut-off, batch, order | 0.5 | 0.75 |
| Store, pre-picked (self-shopped) | 1.0 (1.5) | 1.5 (3.0) |
| Pack and label | 0.6 | 1.75 |
| Loop (61 min × 1.3 + 5 hosts + doorsteps) | 2.0 | 2.75 |
| Close | 0.5 | 0.75 |
| **Per run** | **5.4** | **9.2** |
| Weekly: tier log, complaints, settlement, recruiting | 4.25 | 4.0 |
| **Per week** | **~15 h** (16 self-shopped) | **~22.5 h** (25.5 self-shopped) |

A run day lasts 07:30–15:45, plus the evening close, and has to fit around any day job.

#### 3.2 Pickup host (5: one per hill village, one in Amchit)

One-page agreement, signed before the first run (C8):
- **Hours:** receives the bags by ~15:45 Tue/Fri. Hands them out 17:00–21:00 and the next morning until 12:00.
- **Fridge:** one shelf of dairy, ~30–40 L [EST], kept apart and labelled.
- **Commission:** $0.25 a bag, paid weekly. That is about $9 a month at plan, so the real draw is footfall.
- **Cash:**
  - collects the label amount and logs it on the run sheet;
  - sends the total by Whish (free) by noon the next day, or in cash on the next loop;
  - repeated unexplained gaps end the agreement.
- **Refusals:** taken back with no argument; the founder carries the cost.
- **Also:** may photograph paper lists for the founder; never opens sealed bags; two weeks' notice either side.

#### 3.3 When paid help pays

The `cfo.md` what-ifs:
- A half-day driver (~$22 a run) moves break-even to **22 bags, more than a car carries**. Year 1 falls to **−$959**.
- A ~40-bag van with a driver gives **+$1,946**.
- A packer at the legal day rate (~$14.5 plus $5–9 allowance, `market-lebanon.md` §4) costs about as much as the driver.

**Rule:** hire only once runs hold above ~22 bags for 4 weeks, which is when a van is needed (QUOTE). Until then, rely on pre-picking, Whish prepayment and an unpaid standby. A hire brings NSSF at 22.5% for the employer; check with the accountant.

### 4. SOPs

**SOP-1 Order intake and confirmation**
1. New household: send the welcome message with the line rules and the privacy line: *"Your list and number are used only for your order. Reply DELETE to remove them."*
2. Record each line: item, **brand, size**, quantity and rule: **S** similar OK / **X** skip / **A** ask me. A missing brand or size is taken from their last order, or asked once. No rule = **A**.
3. **Voice notes and photos:** type the lines, reply "Here is what I understood…", and buy only what was read back. Speech-to-text misses ~1 Lebanese word in 4 (`business-model.md` §4.4).
4. "Same as last time": copy the last order and its rules, then read it back. For produce, meat or bread, point to the host shop.
5. **Estimate:** PV1 prices + $1.25 (+ $1.50 doorstep; first bag free). "Savings only lower it; never more than 10% over without your OK; changes until 07:30." Invite Whish prepayment.
6. **At the store:**
   - **S:** same size and type, never dearer than the original's PV1.
   - **X:** left out, no charge.
   - **A:** WhatsApp the option and its price; no answer in 10 min means skip.

**SOP-2 The store run**
1. Send the batch (SKU and quantity) by 08:00.
2. Take the list, cool boxes with frozen ice packs, crates, the float and a charged phone.
3. Check the pick line by line, or shop by aisle. Reject short-dated dairy.
4. Out-of-stocks follow SOP-1 step 6. Use a backup store only on a "yes".
5. **Photograph every shelf tag bought** (PV1/2/3 and thresholds), then **the full receipt at the till**. Keep the paper.
6. Load heavy items first, dairy last.

**SOP-3 Packing and labelling**
1. One crate per village, in loop order. Heavy goods first; dairy in a labelled cool bag.
2. **Label:** name, host, bag code, number of parcels, "TO PAY $x" or "PAID".
3. **Slip:** per line, the receipt line number, shelf price, what we paid and what you paid. Then the fee, the total and "you saved $x".
4. Count the lines against the order, tick them off, seal the bag.
5. Print a **run sheet for each host** with columns: bag code, name, due, method, collected, refused, received, initials.

**SOP-4 Pickup handover and refuse-at-pickup** (printed copy at each host)
1. Count the bags against the run sheet; put the dairy straight into the fridge.
2. The customer checks the bag against the slip at the counter.
3. **Anything wrong, damaged or missing:** take it back, cross it off, deduct its price, note it. No argument.
4. **Payment:** USD, LBP at the rate on the sheet, or a Whish screenshot (checked at close). The customer initials.
5. **Uncollected by noon the next day:** the bag goes back on the next loop and the customer pays the fee only. Shelf-stable goods go back to stock; dairy is offered to the host at cost or written off.
6. **Doorstep:** hand it to a person or leave it at an agreed spot, and send a photo. Problems reported within 24 h are credited on the next bag.

**SOP-5 Complaint handling**
1. Reply within 1 h (08:00–21:00): thank, apologise, ask for a photo.
2. Check the line rule, the slip, the receipt photo and the shelf-tag photo.
3. **Our mistake:** refund by Whish or credit the next bag the same day, whichever the customer prefers. A whole bag wrong means no fee on the next one.
4. **A misread slip:** go through the three columns with the receipt. Never argue.
5. **Village-group complaint:** one calm public line ("Sorry, I've messaged you, fixing it today"), then continue in private. Never post names or receipts.
6. **Log** every complaint. The same cause twice means the SOP changes.

**SOP-6 Tier-price log and reorder check** (Wed and Sat)
1. From the shelf photos, log for each SKU: date, PV1, PV2/PV3 with thresholds, quantity, and whether the tier was hit.
2. **Per run:** the share of bag value bought at a tier price, the average gap below PV1, and the half-saving per bag. Compare with the CFO's **50% / 8% / $1.10** (`cfo-sources.md`). Kill line: under 25% or under 6% (`launch.md` T1).
3. **Near-misses** (1–3 units short of a tier) go into the next broadcast.
4. Prune the ~50-SKU list. Restock labels, paper, bags and ice packs to two weeks' cover. Offer returned stock first, at cost.

**SOP-7 Cash and Whish reconciliation**
1. **Before:** count the float (USD and LBP) and note the Whish balance.
2. **Out:** till totals, with the receipt photos.
3. **In, per host:** expected (labels minus refusals) against received. Match each Whish prepayment to its bag code. Explain any gap over $1 [EST] within the week.
4. **Weekly-settlement households** pay at Friday pickup. Anyone a week behind pays at every pickup until they catch up.
5. **Sunday:**
   - pay host commissions;
   - match the Whish statement to the ledger;
   - keep the personal balance well under the **$3,000 cap** (USD cash-out costs 1%, [Whish fees](https://whish.money/fees-commissions)).
6. Rebuild the float before taking any profit.

### 5. Tools

| need | tool | price |
|---|---|---|
| Orders | **WhatsApp Business app**: broadcast lists of up to 256, a catalogue of 500 items, 4 devices. **No bots on the free app** (ban risk, `business-model.md` §4.1) | free |
| Order book | **Google Sheet**, tabs: Customers, Orders (one row per line), Batch (per SKU), Tier log, Run sheets, Ledger, Complaints | free |
| Payments | **Whish** (OMT Pay as backup). Balance caps: personal $3,000, corporate $30,000 (`market-lebanon.md` §5) | wallet-to-wallet free; merchant 1% |
| Receipt photos | phone camera, one Drive folder per run date; these are the price database (`product-tech.md`) | free |
| Own software, after 2–3 hand runs | Dashboard, parser and driver PWA (`product-tech.md`) on a Hetzner VPS | ~$10/month at 180 orders: VPS €5.49, API $0.0091 a message after 1,000 free, parsing $0.008 an order |

### 6. Licences, permits and insurance

**Rules differ and change. Confirm each one with a Lebanese lawyer or accountant. Not legal advice.** Source: `market-lebanon.md` §6.

| item | what to confirm | link |
|---|---|---|
| **Agent vs reseller** (decide first) | Reseller: the goods (~$94,500 in year 1 [EST]) are turnover, past the **VAT threshold of LBP 5bn (~$55,900)**. Agent: perhaps only the ~$4,800 in fees counts. Ask also: whose name is on the pooled invoice, who is liable for dairy, whether PV3 needs registration, whether foods are VAT-exempt | [PwC](https://taxsummaries.pwc.com/lebanon/corporate/other-taxes) |
| **Commercial register** | Structure; Jbeil court registry, ~10–15 days | [IDAL](https://investinlebanon.gov.lb/en/doing_business/starting_a_business) |
| **MoF tax number** | Invoicing; monthly stamp duty | [MoF](https://www.finance.gov.lb/) |
| **Law 81/2018 data notice** | The privacy line; whether a declaration to MoET is needed | [DLA Piper](https://www.dlapiperdataprotection.com/index.html?t=law&c=LB) |
| **Municipal permission for hosts** | Ask each of the 5 municipalities whether hosting changes the shop's permit (aamchit.com is **not** Amchit's municipality) | in person |
| **Goods in a private car** ⚠ | **Check** whether paid goods runs are allowed on private plates and whether the insurance covers commercial use | lawyer, insurer |
| Food safety (Law 35/2015); consumer protection (Law 659/2005) | Duties for holding dairy; prices, invoices, complaints | [MoPH](https://www.moph.gov.lb/), [MoET](https://www.economy.gov.lb/) |
| Whish/OMT business account; later, employees (NSSF) | Requirements | [NSSF](https://www.cnss.gov.lb/) |

### 7. Risk register

L = likelihood, I = impact; all **[EST]**.

| # | risk | L | I | plan |
|---|---|---|---|---|
| 1 | **Tiers not hit** | H | H | Measure first (T1); nudge near-misses; keep the SKU list narrow. If the half-saving stays below $0.50 a bag for 4 weeks: a $1.50–2 flat fee for car-less households, or stop |
| 2 | **Tawfeer caps tier prices per customer, or refuses** | M | H | Ask in writing first, as a PV3 business customer. If refused: charge shelf price, waive the fee and say so on the slip; then re-price |
| 3 | **Host shop quits** | M | M | Two weeks' notice; a backup host per village; meanwhile hand out bags from the car, 17:00–19:00 |
| 4 | **Founder sick** | M | H | A trained standby. If none: cancel by 07:00, refund prepayments |
| 5 | **Car breakdown** | L–M | H | Service before launch; a borrowed car or a taxi; new time sent out; bags kept cold |
| 6 | **Cash shortfall / float** | M | M–H | Whish prepayment; weekly settlement capped at 40 households and 1 week; SOP-7 after every run; a two-run float |
| 7 | **Spoiled dairy** | M | M | Ice packs; dairy loaded last and into the host fridge; reject short-dated stock; never held past noon the next day |
| 8 | **Security escalation / road closure** (war since 2 Mar 2026, fragile ceasefire, UNIFIL mandate ends 31 Dec) | L–M | H | Suspend and refund; no stock held; fixed costs ~$124/month; Spinneys as a stopgap; fuel budgeted at ±20% |
| 9 | **Viral bad review in the village WhatsApp group** | M | H | SOP-5 within the hour; receipt photos as proof; the host vouches; post the fix |
| 10 | **Tawfeer launches its own village pickup** | L–M | H | Own the list, the hosts and the WhatsApp relationship; keep 2 suppliers; offer Tawfeer the channel (`tawfeer-pitch.md`) |

### 8. Changes for the CFO

`numbers.json` was **not** edited. Re-run with:

| line | now | suggested | source / reason |
|---|---:|---:|---|
| Cash float | $1,100 | **$2,200** | Under weekly settlement (`offer.md`), Tue and Fri goods are both paid for before Friday's pay-in: 2 × 20 × $55. **Cash needed: ~$1,900 → ~$3,000.** Whish prepayment reduces it |
| Fuel | $7/run | **$8/run** [EST] | Amchit ↔ Qartaboun (~10 km), then the hill loop from home (~45–50 km; OSRM 49.5 km). 60 km × 10 L/100 km × $1.31 = $7.86. At the 29 Sep peak ($1.59/L): ~$9.50 |
| Software | $16 | **$10** ($0 in months 1–2) | v2 dropped the $6 price agent: $1.64 + $1.44 + $0.24 + $6.11 = $9.43 at 180 orders (`business-model.md` §4.6) |
| *(missing)* Vehicle wear, commercial insurance | $0 | **add, QUOTE**; placeholder $20/month [EST] | ~540 km a month on hill roads |
| *(missing)* Ongoing accountant, stamp duty | $0 | **add, QUOTE** | Only the setup is budgeted |
| Host commission | $0.25 | keep; **run a $0.50 what-if** | ~$9 a month per host is thin |
| Payment fees | 0.6% | keep; flag | Holds only if Tawfeer accepts Whish (USD cash-out costs 1%) |
| Capacity | 20 bags | **test in week 1** | Unmeasured |

**Effect** (the CFO's tool on a scratch copy: fuel $72, software $10, $20 placeholder): fixed costs **$147 a month**, break-even **10 bags a run** (was 9), year 1 **$1,141** (was $1,417). Adding a $0.50 host commission: break-even **12**, year 1 **$711**.

**Open quotes:** Tawfeer terms, bags, labels, paper, cool boxes, crates, insurance, accountant, a Whish corporate account. **Next:** `/founder-launch`.

## Launch plan

Today is Tue 17 Nov 2026. **Launch day: Tue 12 Jan 2027**, the first public run, after the Christmas, New Year and 6 January holidays. **Soft open: Fri 8 Jan 2027**, founding households only. The marketing calendar in `marketing.md` runs from 29 Dec 2026.

### Step 1: test before you spend (17 Nov – 18 Dec)

Nothing in this plan is expensive (`cfo.md`: $775 sunk plus a $2,200 float that comes back), but every number in it is an estimate. Three cheap real-world tests replace the three estimates that decide everything:

| test | how | success line (written before running it) | if it fails |
| --- | --- | --- | --- |
| **T1. The tier gap** (the CFO's "line to watch") | Shelf survey at Tawfeer MAX Jbeil: photograph the PV1/PV2/PV3 tags for the 40 staples villagers buy most. Ask staff for the thresholds and whether mixed cartons count. | **≥25% of a typical bag's value** can reach PV2/PV3 when 10 households pool, at an **average gap ≥6%** | Below that, the savings share can't pay for itself. Switch to a flat fee of $1.50–$2.00 aimed only at car-less households, or stop. |
| **T2. Real sign-ups at a real price** | The founder and two host-shop owners personally ask car-less and hill-village households to become founding households: the v2 offer, a real date, $1.25 a bag. | **25 founding households** across the 4 hill villages and car-less Amchit by Fri 18 Dec. The panel's 25% buy rate implies ~25 yes from ~100 asked. | Fewer than 10 yes from 100 asked means the panel was far too optimistic. Go back to `/founder-offer` with the real objections. |
| **T3. Two hand-run friends-and-family runs** | Fri 11 Dec and Tue 15 Dec, with 8–10 households, no software: WhatsApp Business app, a Google Sheet, printed slips. | Each run: **≥10 bags, zero wrong bags**, **average slip saving ≥ $1.25** (it at least covers the fee, so the household pays no more than shelf price; the CFO base assumes only $1.10), ≤45 min packing | Fix the routine (`ops.md` SOPs) and run a third time before any public launch. |

**Go / no-go: Fri 18 Dec.** Go only if T1 and T3 pass and T2 reaches at least 15. If real buyers fall well short of the panel, trust the real buyers.

### Step 2: the countdown

| week of | task | owner | deadline | critical path |
| --- | --- | --- | --- | --- |
| **17 Nov** | T1 shelf survey at Tawfeer MAX Jbeil (40 SKUs, 3 tiers) | founder | Sat 21 Nov | **yes** |
| | Ask Tawfeer for a meeting: 1626 / customerservice@tawfeer.market, using `tawfeer-pitch.md` | founder | Fri 20 Nov | **yes** |
| | Count car-less and winter-resident households with each mukhtar or the parish (Bejjeh, Ghalboun, Aabaydat, Kfoun) | founder | Sat 21 Nov | |
| | Visit 4–6 village mini-markets; shortlist 2 pickup hosts; note their prices on 10 staples (the missing dekkene price) | founder | Sat 21 Nov | **yes** |
| **24 Nov** | Tawfeer meeting: tiers, invoice account, pre-picking, settlement | founder | Fri 27 Nov | **yes** |
| | Accountant: agent vs reseller, commercial register, MoF number, VAT position (`ops.md` licences) | founder + accountant | Fri 27 Nov | |
| | Sign 2 host-shop agreements: hours 5–9 p.m. + morning, fridge shelf, $0.25 a bag, cash rules | founder + hosts | Sat 28 Nov | **yes** |
| **1 Dec** | Business WhatsApp number, 40-SKU catalogue, order-book sheet, bag label + 3-column slip template (`brand.md`) | founder | Fri 4 Dec | |
| | Recruit 8–10 friends-and-family households for T3; start T2 sign-ups | founder + hosts | Sat 5 Dec | |
| | Buy crates, cool boxes, label printer ($250 budget) | founder | Sat 5 Dec | |
| **8 Dec** | **T3 run #1, Fri 11 Dec**; log every number | founder | Fri 11 Dec | **yes** |
| **15 Dec** | **T3 run #2, Tue 15 Dec**; **go/no-go Fri 18 Dec** | founder | Fri 18 Dec | **yes** |
| | File registration if go (accountant) | accountant | Fri 18 Dec | |
| **22 Dec – 3 Jan** | Holidays: no runs. Founding-household sign-ups continue; marketing pre-launch posts from 29 Dec (`marketing.md`) | founder | | |
| | Start building the dashboard + parser (`product-tech.md` week 1–3) on what T3 taught | founder | ongoing | |
| **5 Jan** | Confirm Tawfeer pre-pick for Fri 8 and Tue 12; brief the hosts; print labels | founder | Wed 6 Jan | |
| | **Soft open Fri 8 Jan**: founding households only | founder + hosts | Fri 8 Jan | **yes** |
| **12 Jan** | **Launch: first public run, Tue 12 Jan** | founder | Tue 12 Jan | |

The **critical path** is T1, then the Tawfeer meeting, the host shops, the two T3 runs and the go/no-go. A slip in any one moves the launch date.

### Step 3: launch-day run sheet (Mon 11 – Tue 12 Jan 2027)

| time | what | who | channel |
| --- | --- | --- | --- |
| Mon 18:00 | Reminder to founding + new households: "List by 9 p.m. for tomorrow's run" | founder | WhatsApp broadcast + village groups (`marketing.md`) |
| Mon 21:00 | **Cut-off.** Late lists roll to Friday | | |
| Mon 21:00–22:30 | Read every list back with its line rules (similar OK / skip / ask me) and an estimated total; wait for "OK" | founder | WhatsApp |
| Tue 07:30 | Send the consolidated order to Tawfeer MAX for pre-picking (if agreed) | founder | as agreed |
| Tue 09:00–10:30 | At Tawfeer MAX: check the pick, settle out-of-stocks by the line rules, pay, **photograph every receipt** | founder | |
| Tue 10:30–12:30 | Pack by village and household; bag label; print slips (shelf / paid / your price) | founder | |
| Tue 12:30–14:30 | Loop: Kfoun → Ghalboun → Bejjeh → Aabaydat (hosts) + doorstep drops; Amchit host | founder | |
| Tue 14:30 | "Your bag is ready at [host], 5–9 p.m. or tomorrow morning" + photo of the slip | founder | WhatsApp |
| Tue 17:00–19:00 | Founder at the busiest host for the first pickups: answer questions, take refusals (refuse-at-pickup) | founder | in person |
| Tue 21:30 | Close: cash and Whish vs ledger, refusals logged, tier-capture logged, uncollected bags noted | founder | sheet |

**If something breaks** (from `ops.md` risk register):
- **Item out of stock:** apply the line rule; "ask me" lines get one message, and with no answer by 10:15 they are skipped.
- **Tawfeer won't apply tiers to the pooled order:** buy at shelf price, waive the fee for that run, and say so on the slip. Never hide it.
- **Car breaks down:** a borrowed car or a taxi for the loop; message every household with a new time.
- **Host shop closed:** the founder hands out bags from the car at a named spot in the village, 17:00–19:00.
- **A complaint in a village group:** reply within the hour, in public and politely, then fix it in private (`brand.md` complaint reply).

### Step 4: the first 30 days

**The weekly numbers** (CFO break-even: 12 bags a run; plan: 20):

| number | target by day 30 | change something if |
| --- | --- | --- |
| Bags per run | ≥15 | below 12 (break-even) for 2 weeks in a row |
| Bags where the slip saving ≥ the fee | ≥50% | below 30%: the tier gap is too thin; move to a flat fee aimed only at car-less households |
| Households ordering a 2nd bag within 14 days | ≥60% | below 40% |
| Wrong or damaged lines per 100 lines | ≤2 | above 4 |
| Share of bag value bought at PV2/PV3 | ≥25% | below 15% |

**Reviews**
- **Day 7 (Tue 19 Jan):** Does the routine fit in the hours `ops.md` estimates? Any wrong bags? Which items keep going out of stock?
- **Day 14 (Tue 26 Jan):** Fee test: compare $1.25 and $1.50 conversion across the two village pairs (`pricing.md`). Tier-capture trend. Is a "same as last time" standing order used?
- **Day 30 (Thu 11 Feb):** Bags per run vs break-even. Decide whether to add a third host village, raise the fee, or stop. Share the 4-week numbers with Tawfeer (`tawfeer-pitch.md`). Only now consider Basket Club pricing.

_The panel is simulated buyers and the numbers are projections from your inputs. Confirm demand with real customers and costs with real quotes before you spend. Not financial, legal or tax advice._
