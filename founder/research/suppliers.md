# Suppliers, price data and basket spread: Amchit group-buying service

Research date: 2026-11-17. Public sources only. Every price was read on 2026-11-17 unless a row says otherwise. Anything marked **estimate** was not measured.

---

## 0. Bottom line

1. **"Tawfir Shop" is almost certainly Tawfeer (توفير).** It is Lebanon's largest discount grocery chain: 40+ stores, run by Tawfeer International SAL (Capital Partners Holding, CEO Rami Bitar). Its online store is **"Tawfeer Online"** at shop.tawfeer.market, which fits the name "Tawfir Shop". I found no other store called Tawfir, Tawfir Shop or Tawfir Market in Lebanon. Confidence is high but not certain, so the founder should confirm the Instagram handle he saw. It should be **@tawfeerlebanon**.
2. **The branch that matters is Tawfeer MAX Jbeil (Qartaboun, Beirut–Jbeil highway).** It opened on 21–22 May 2026, roughly 5–8 km from Amchit (estimate). MAX is built around "Buy More, Pay Less": a single-item price, a lower price for a larger quantity, and a carton price **explicitly for "small businesses, neighborhood shops, restaurants, and cafés"**, with no membership. The founder can get carton (wholesale-level) prices **without any special deal**. What he should ask the owner for is the service around them: an invoice or B2B account, picking his order in advance, and maybe credit or delivery.
3. **The measured basket spread is small among discount chains and larger against Spinneys.** On 12 staples at the three stores that list all of them online (Tawfeer, Le Charcutier Aoun, Faddoul):
   - buying each item where it is cheapest saves **3.4%** against the cheapest single store, **4.4%** against the average store and **5.7%** against the dearest;
   - on the 6–7 items Spinneys also lists, the cheapest single store is **~10% below Spinneys** and cherry-picking is **~11% below Spinneys**.
   - Adding the two Tawfeer bundle/promo deals I found raises the saving to **~6–8%**. Shopping **only at Tawfeer, using its bundles,** costs about the same as cherry-picking three stores ($74.77 vs $74.42).
4. **Get price data by partnership, not scraping.** Spinneys' terms allow only "personal, non-commercial transitory viewing". Carrefour Lebanon blocks automated fetches. Seven of the candidate stores (Tawfeer, Faddoul, Metro Market, Le Charcutier, Hachem, La Valeur, Khoury Shopping Center Batroun) run on one white-label platform, **Suppy**. A third-party aggregator, **SoukCompare**, already publishes daily prices for 41 grocery shops. The compliant route is described in §3.4.

---

## 1. Identifying "Tawfir Shop" → Tawfeer / Tawfeer Online / Tawfeer MAX

### 1.1 Identity

| Fact | Detail | Source (date) |
|---|---|---|
| Brand | Tawfeer (توفير, "savings"). Its own spelling is *Tawfeer*, never *Tawfir*. Online store title: "Tawfeer Online". | [tawfeer.market](https://tawfeer.market/) (read 2026-11-17); page title of [shop.tawfeer.market](https://shop.tawfeer.market/) (read 2026-11-17) |
| Operator | "Tawfeer International", a subsidiary of Capital Partners Holding, described as "Lebanon's leading discount retail operator". A D&B profile is titled "TAWFEER INTERNATIONAL SAL" (I could not read its body). | [Beirut.com, 22 May 2026](https://www.beirut.com/en/775677/tawfeer-max-opens-in-jbeil-bringing-transparent-three-tier-pricing-to-families-and-small-businesses/); [D&B listing](https://www.dnb.com/business-directory/company-profiles.tawfeer_international_sal.652b58f59f3bc6a8c8bc3d22fcd883d4.html) |
| CEO | Rami Bitar, CEO of Tawfeer International and Capital Partners Holding | [Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677) |
| Size | "41 Branches As of April 2026"; 850+ employees (website). Press: 40+ stores, 30,000+ shoppers a day, 1,000+ staff, target of 500 stores by 2030 | [tawfeer.market](https://tawfeer.market/); [Annahar, 14 May 2026](https://www.annahar.com/economy/309955/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%85%D9%81%D9%87%D9%88%D9%85-%D8%AC%D8%AF%D9%8A%D8%AF-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D8%A7%D9%84%D8%B0%D9%83%D9%8A-%D9%88%D8%A7%D9%84%D8%A3%D8%B3%D8%B9%D8%A7%D8%B1-%D8%A7%D9%84%D9%85%D9%86%D8%AE%D9%81%D8%B6%D8%A9-%D9%81%D9%8A-%D9%84%D8%A8%D9%86%D8%A7%D9%86) |
| Format | Self-described "hyperdiscounter". 500+ brands, 30 exclusive lines, 6 private labels; claims savings of "up to 20%" on grocery bills (company claim, not verified) | [Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677); [Annahar, 14 May 2026](https://www.annahar.com/economy/309955/%D8%AA%D9%88%D9%81%D9%8A%D8%B1-%D9%85%D8%A7%D9%83%D8%B3-%D9%85%D9%81%D9%87%D9%88%D9%85-%D8%AC%D8%AF%D9%8A%D8%AF-%D9%84%D9%84%D8%AA%D8%B3%D9%88%D9%82-%D8%A7%D9%84%D8%B0%D9%83%D9%8A-%D9%88%D8%A7%D9%84%D8%A3%D8%B3%D8%B9%D8%A7%D8%B1-%D8%A7%D9%84%D9%85%D9%86%D8%AE%D9%81%D8%B6%D8%A9-%D9%81%D9%8A-%D9%84%D8%A8%D9%86%D8%A7%D9%86) |
| What it sells | A full grocery range (fresh, dairy, pantry, frozen, household, personal care, baby). SoukCompare tracks 9,289 Tawfeer products. Largest categories: sweets & snacks 1,831, personal care 1,806, pantry 1,221, home & kitchen 1,118, drinks 901, dairy 762 | [SoukCompare Tawfeer page](https://soukcompare.com/stores/tawfeer) (17 Nov 2026) |
| Website / app | Corporate site [tawfeer.market](https://tawfeer.market/). Online shop [shop.tawfeer.market](https://shop.tawfeer.market/), whose page metadata names "Suppy Technologies" as author. App "Tawfeer LB" on iOS and Android, "over 2500 items" | [App Store](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055); [Google Play developer page (Suppy)](https://play.google.com/store/apps/developer?id=Suppy) |
| Social | Instagram @tawfeerlebanon | [Beirut.com, 15 May 2026](https://www.beirut.com/en/775151/meet-tawfeer-max-lebanons-new-super-saver-supermarket/) |

**Closest non-matches checked:** "Tawfeer Market" Egypt (Alexandria app), "Tawfeer EU" (Netherlands), "Al Tawfeer" (Ajman, UAE). None of these is in Lebanon ([App Store search results](https://apps.apple.com/fi/app/tawfeer-market/id1513485186), [2GIS Ajman](https://2gis.ae/ajman/branches/70000001019194159)). Searches for "Tawfir shop", "tawfirshop", "توفير شوب" and "Tawfir Jbeil/Amchit" found no other Lebanese store.

**Caution on sources:** many search results about "Tawfeer Market" are self-published SEO pages on Payhip, Hashnode, Google Sites, Notion and Blogspot that call it "the best/cheapest supermarket". I did not use them as evidence.

### 1.2 Branches near Amchit

The full branch list is not published on tawfeer.market. Its sitemap has 8 pages and none of them lists branches ([sitemap](https://tawfeer.market/sitemap.xml)).

| Branch | Location | Distance from Amchit (**estimate**) | Evidence |
|---|---|---|---|
| **Tawfeer MAX Jbeil** | Qartaboun, Jbeil, on the Beirut–Jbeil (also called Beirut–Tripoli) highway. 2,000 m², 5,500 SKUs. Opened 21 May 2026, 5 pm (official opening announced 22 May) | ~5–8 km, 10–15 min | [Beirut.com, 15 May 2026](https://www.beirut.com/en/?p=775151); [Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677); [Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/توفير-ماكس-يفتتح-فرعه-الجديد-في-جبيل-ويطلق-نموذج-التسعير-الثلاثي-للتسوق-منخفض-الكلفة); [Executive Bulletin, 8 Sep 2026](https://executive-bulletin.com/retail/tawfeer-expands-hyperdiscounter-model-in-lebanon-to-advance-consumer-protection-amid-soaring-inflation-and-rising-shelf-prices) |
| Tawfeer "Tabarja" | The online shop has a storefront named *Tabarja* (store id 390); the address is not published | ~13–15 km, 15–20 min | Product URL `shop.tawfeer.market/shop/stores/390/Tabarja/...` linked from [SoukCompare](https://soukcompare.com/p/42779-persil-universal-gel-2-5l-liquid-laundry-detergent) |
| Tawfeer "Zouk" | Online storefront *Zouk* (store id 34); the address is not published | ~20–22 km, 25–35 min | [SoukCompare tuna page](https://soukcompare.com/p/7159-siblou-white-tuna-in-vegetable-oil-185g) |
| Other storefronts seen | Raouche (24), Baabda (46), Kfaraakka (172), Balamand (476). All are far from Amchit. | — | SoukCompare product pages (see CSV) |
| Other Tawfeer MAX | Cascada Mall, Taanayel (Bekaa), opened Oct 2025; Abbassieh (converted, Sep 2026). Two more conversions are planned. | far | [Beiruting, 3 Oct 2025](https://www.beiruting.com/news/141291/tawfeer-max-launches-in-lebanon-efficiency-as-the-new-lifeline-against-inflation); [Executive Bulletin, 8 Sep 2026](https://executive-bulletin.com/retail/tawfeer-expands-hyperdiscounter-model-in-lebanon-to-advance-consumer-protection-amid-soaring-inflation-and-rising-shelf-prices) |

Distances are straight-line estimates from approximate town positions. Amchit is "about 40 km north of Beirut" ([Wikipedia](https://en.wikipedia.org/wiki/Amchit)). They were **not measured on a map service**.

### 1.3 Promotion mechanics, with real examples

**A. Tawfeer MAX three-tier "Price Value" system (PV1, PV2, PV3).** This matches the founder's "buy 3, get a big discount" most closely.
- "cheap by the piece, cheaper by quantity, and cheapest by the carton". The tiers are permanent: "without temporary promotions, membership fees, loyalty cards, or limited-time discounts" ([Beirut.com, 15 May 2026](https://www.beirut.com/en/?p=775151); [Beiruting, 15 May 2026](https://www.beiruting.com/news/141422/tawfeer-max-a-new-era-of-value-retail-in-lebanon)).
- Tier 1 is "the cheapest single-unit price on the Lebanese market". Tier 2 is for larger family quantities. Tier 3 gives "wholesale-level discounts for small businesses, neighborhood shops, restaurants, and cafés" ([Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677)). Annahar quotes "أسعارًا مخصّصة للشراء بالجملة" ("prices specifically for wholesale purchases") ([Annahar, 22 May 2026](https://www.annahar.com/lebanon/312468/توفير-ماكس-يفتتح-فرعه-الجديد-في-جبيل-ويطلق-نموذج-التسعير-الثلاثي-للتسوق-منخفض-الكلفة)).
- CEO: "The MAX model changes the relationship between price and quantity" ([Executive Bulletin, 8 Sep 2026](https://executive-bulletin.com/retail/tawfeer-expands-hyperdiscounter-model-in-lebanon-to-advance-consumer-protection-amid-soaring-inflation-and-rising-shelf-prices)).
- **Not public anywhere I could find:** the quantity thresholds for PV2 and PV3, and any PV1/PV2/PV3 price for any product. The founder must collect these on the shelf at Tawfeer MAX Jbeil.

**B. Bundle packs and percentage-off offers in Tawfeer's online catalogue.** SoukCompare showed 156 Tawfeer products on offer on 17 Nov 2026 ([store page](https://soukcompare.com/stores/tawfeer)). Real examples:

| Offer | Price | Was | Saving | Link |
|---|---|---|---|---|
| Barilla Ditalini Rigati 400 g **x3** | $2.99 | $4.47 | −33% (pay for 2, get 3) | [link](https://soukcompare.com/p/441660-barilla-shortcuts-ditalini-rigati-cello-n-47-400g-x3) |
| Barilla Filini Vermicelli 400 g **x3** | $2.99 | $4.47 | −33% | [link](https://soukcompare.com/p/443978-barilla-filini-vermicelli-no-30-400g-x3) |
| Divella Filini 79 500 g **x2** | $1.59 | $2.12 | −25%. Per pack $0.80, against $1.19 for a single pack at Tawfeer (−33%) | [link](https://soukcompare.com/p/55178-divella-pasta-filini-79-500g-x2-25-off) |
| H&H Sardines 125 g **x3** | $1.39 | $2.07 | −33% | via [store page](https://soukcompare.com/stores/tawfeer) |
| Palmolive soap 90 g **x4** | $2.74 | $3.43 | −20% | [link](https://soukcompare.com/p/4757-palmolive-bar-soap-olive-90g-x4-20-off) |
| Nido milk powder bag 2.25 kg −10% | $16.99 | $18.88 | −10% | [link](https://soukcompare.com/p/49712-nido-milk-powder-bag-2-25kg-10-off) |
| Mazola sunflower oil 8.1 L | $27.99 | $39.99 | −30% | [link](https://soukcompare.com/p/34710-mazola-sunflower-oil-8-1l-30-discount) |
| Elegance adult diaper pants M 14 pcs | $7.04 | $10.51 | −33% | via [store page](https://soukcompare.com/stores/tawfeer) |

The corporate homepage also shows a "Hot Deals This Week" block, for example "Barilla Pasta $1.99 (was $2.79)" and "Joud Water $8.99 (was $12.99)". It gives no sizes or dates and may be static ([tawfeer.market](https://tawfeer.market/), read 2026-11-17).

**Flyers:** the online shop loads a "flipbook" viewer library (seen in the page source of shop.tawfeer.market), which suggests digital flyers inside the app. I could not view them without the app, so this is **not confirmed**.

### 1.4 Delivery, minimum order, payment, B2B

| Topic | Finding | Source |
|---|---|---|
| Delivery | "Delivery 7 Days a week", chosen time slot, "delivered in refrigerated cabinets" | [App Store](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055) (read 2026-11-17) |
| Delivery fee / minimum order | **Not published** on the website, the app listing or press. The founder will see them at checkout in the app. | — |
| Payment | "cash on delivery or credit card on delivery" | [App Store](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055) |
| Wholesale / B2B | MAX tier 3 is public wholesale-level pricing for small businesses, with no membership. No separate B2B account programme is described anywhere. Tawfeer says it relies on "direct supplier relationships" and "centralized logistics". | [Beirut.com, 22 May 2026](https://www.beirut.com/en/?p=775677) |
| Partnership channels | Phone 1626 / 01 490 290; customerservice@tawfeer.market; hours 8:00–22:00; contact form (inquiry types include "Franchise"); LinkedIn. Investment models: "Franchise" and "Manchise". | [tawfeer.market](https://tawfeer.market/) |
| Reviews | iOS (Lebanon store): **4.8/5 from 301 ratings**. One review (25/05/2024) says "Always the delivery is late… takes more than 2 hours" and an order went to the wrong address; others praise prices and staff ([App Store](https://apps.apple.com/lb/app/tawfeer-lb/id1574152055)). Android: **4.07/5 from 392 ratings, ~70.8K installs** per a third-party tracker ([AppGoblin](https://appgoblin.info/apps/ma.osp.shopping_app.twds.android)). I could not read Google Maps reviews for Tawfeer MAX Jbeil. | read 2026-11-17 |

**What to ask Tawfeer MAX Jbeil (suggested):**
1. The PV2 and PV3 thresholds for the 12 staples below.
2. Whether a mixed-SKU carton counts towards PV3.
3. A business account with an invoice (VAT).
4. Pre-picking of a daily order sent by 15:00, ready for collection.
5. Credit terms or a weekly settlement.
6. Whether the app's prices equal the Jbeil shelf prices.

---

## 2. Other candidate suppliers reachable in one driver run

Drive times are **estimates** (see §1.2 note). The prices column shows whether public online prices exist.

| # | Supplier | Location | Drive from Amchit (est.) | Online prices | Delivery / fees | Promo style | B2B / wholesale |
|---|---|---|---|---|---|---|---|
| 1 | **Spinneys Jbeil** (Gray Mackenzie Retail Lebanon SAL) | Jbeil highway, Blat exit ([Foursquare](https://foursquare.com/v/spinneys/505c94a3e4b06ee0cb826202); branch listed by [Daleeeel](https://www.daleeeel.com/en-lb/chain/2841/spinneys/locations/)) | ~3–5 km, 5–10 min | **Yes.** [spinneyslebanon.com](https://www.spinneyslebanon.com/) shows USD prices and a "1.00 USD = 89,700 LBP" banner | The site lists delivery areas Beirut, Greater Beirut, Mount Lebanon, Jeita/Ajaltoun/Faraya; Jbeil was not visible. There is a click-and-collect option. Fee and minimum not found. | 1,494–1,495 items on promotion. Mostly %-off, a few multi-buys, e.g. "DIVELLA SPAGHETTI 8 2+1 FREE" $2.39 (was $2.55), "DURACELL AAA 6+2FREE" ([promotions](https://www.spinneyslebanon.com/default/promotions.html)) | None public. The loyalty card is "for personal use only… cannot be used for business purposes" ([search summary of loyalty T&Cs](https://www.spinneyslebanon.com/m-loyalty-points-terms-conditions)) |
| 2 | **Le Charcutier Aoun** (Le Charcutier Aoun Group SAL) | A Jbeil branch ("Jbeil Mastita") is listed in a directory last updated 30 Jul 2021 ([Daleeeel](https://www.daleeeel.com/en-lb/chain/2900/le-charcutier-aoun)). The app says 19 branches ([App Store](https://apps.apple.com/app/id6760022832)). **Current Jbeil branch not re-verified.** | ~6–8 km, 10–15 min | **Yes.** [lecharcutier.suppy.app](https://lecharcutier.suppy.app/) (Suppy). Prices read via SoukCompare come from the *Dekwaneh* storefront. | "scheduled or express options to your door"; cash or card. Fee not found. | Weekly in-app promotions; x2 bundles, e.g. Harpic 750 ml x2 −30%, WC Net x2 −25% ([SoukCompare](https://soukcompare.com/stores/le-charcutier)) | None public |
| 3 | **Bou Khalil Jbeil** | Branch listed ([Daleeeel](https://www.daleeeel.com/en-lb/chain/3210/bou-khalil-supermarket/locations/)); address not found | ~4–6 km (est.) | **No online prices found.** boukhalil.com returned HTTP 503 | Unknown | Unknown | Unknown |
| 4 | **Metro Market Ghazir** (Partenaire Intermarché, Athos network) | Ghazir, Keserwan ([Annahar, 2 Jan 2026, sponsored](https://www.annahar.com/economy/266288/بالشراكة-مع-intermarch-تعزز-athos-حضورها-في-لبنان-بافتتاح-متجرين-في-البترون-وأميون)) | ~14–16 km, 15–20 min | **Yes.** [metromarketlebanon.com](https://metromarketlebanon.com/) (Suppy-built; "Delivery, Pickup") | Fee not found | "Weekend offers" category (e.g. Candia labneh 900 g $5.54, was $6.15) | None public |
| 5 | **Faddoul Supermarket, Sarba** (Jounieh) | Sarba (Jounieh): its Suppy shop serves a storefront named "Sarba" (store id 39), e.g. [this product URL](https://faddoul.suppy.app/shop/stores/39/Sarba/products/16366/Plein%20Soleil%20Sunflower%20Oil%201.8L); street address not verified | ~19–20 km, 25–30 min | **Yes.** [faddoul.suppy.app](https://faddoul.suppy.app/) | Fee not found | %-off bundles (e.g. Nido 2.25 kg "+10% Off" pack) | None public |
| 6 | **Khoury Shopping Center (KSC) Batroun** (Partenaire Intermarché) | Batroun, renovated under the KSC banner ([Annahar, 2 Jan 2026](https://www.annahar.com/economy/266288/بالشراكة-مع-intermarch-تعزز-athos-حضورها-في-لبنان-بافتتاح-متجرين-في-البترون-وأميون)) | ~11–13 km north, 15–20 min | App "KSC Partenaire Intermarché" exists on Suppy ([Google Play](https://play.google.com/store/apps/developer?id=Suppy)); I did not check its prices | Unknown | Unknown | Unknown |
| 7 | **Carrefour Zouk Mosbeh** (Majid Al Futtaim) | Zouk Mosbeh ([Asharq Al-Awsat](https://english.aawsat.com/node/1322746), undated) | ~22 km, 25–40 min | Has an online shop with **LBP** prices, but carrefourlebanon.com returned HTTP 503 to every fetch (bot protection). A search snippet showed Plein Soleil 1.8 L at "LBP 573,340" (≈ $6.41 at 89,500; **unverified, date unknown**) | Unknown | Unknown | Unknown |

**Checked and set aside** (not near Amchit, or no evidence of a branch there):
- *Happy* (Spinneys discount brand): stores in Hazmieh, Zouk Mosbeh and Choueifat ([BusinessNews](https://www.businessnews.com.lb/cms/Story/StoryDetails/4353/Spinneys-is-‘Happy’)).
- *Hachem Superstore*: Rifoun, Keserwan mountains ([Annahar](https://www.annahar.com/economy/266288/بالشراكة-مع-intermarch-تعزز-athos-حضورها-في-لبنان-بافتتاح-متجرين-في-البترون-وأميون)). Often cheapest online, but far.
- *La Valeur*: Achrafieh and Ajaltoun storefronts.
- *Promarché*: Antelias and further south.
- *Fahed*: "Jounieh Fahd" ranked in the MoET InfoPrice of Feb 2019 ([MoET PDF](https://www.economy.gov.lb/media/12058/summaryinfopricefeb2019en-rank.pdf)); current branch not verified.
- *The Sultan Center*, *Rammal*: no Jbeil or Keserwan branch found.
- *Monoprix*: being relaunched by Gray Mackenzie ([FoodBusinessMEA](https://www.foodbusinessmea.com/?p=2154642)); no branch near Amchit found.
- *Al Makhazen*: online via minim.weevi.com; no nearby branch found.

**Cash-and-carry and produce/meat wholesale.** I found no named cash-and-carry or wholesale vegetable market (حسبة) in Jbeil, Amchit or Jounieh in public sources. Directory hits ([Kompass Jbeil](https://lb.kompass.com/d/jbeil/lb_lbjl_13/), [D&B Mount Lebanon wholesalers](https://www.dnb.com/business-directory/company-information.grocery_and_related_product_merchant_wholesalers.lb.mount_lebanon.html)) are importers and distributors with no public terms. **The de facto local cash-and-carry is Tawfeer MAX tier 3.** For produce and meat, ask local farmers, butchers and the village shop. This was not researched further.

---

## 3. Price-comparison feasibility

### 3.1 Machine-readable prices, robots.txt and terms per store

| Store | Public prices? | robots.txt (read 2026-11-17) | Terms on automated access / reuse |
|---|---|---|---|
| Tawfeer | Yes, in the JS web app shop.tawfeer.market (Suppy); prices render client-side | [shop.tawfeer.market/robots.txt](https://shop.tawfeer.market/robots.txt): `User-agent: * Allow: /`, disallows `/user`, `/orders`, `/support`. [tawfeer.market/robots.txt](https://tawfeer.market/robots.txt): `Allow: /`, `Disallow: /thank-you` | The storefront terms could not be read (they need JavaScript). Suppy's own site terms say users may not "use automated means to copy or extract content in a way that harms the website" and "may not reproduce or reuse content commercially without our written permission". Those terms state that they apply to suppy.app itself ([Suppy ToS, updated 6 Oct 2026](https://suppy.app/legal/terms-of-service)). |
| Spinneys | Yes, server-rendered product pages with USD prices | [robots.txt](https://www.spinneyslebanon.com/robots.txt) disallows `/catalog/`, `/checkout/`, `/customer/`, any URL with a query string (`/*?*`), `*.php` | [Terms of Use](https://www.spinneyslebanon.com/terms-of-use) §2.1: licence "for personal, non-commercial transitory viewing only"; you may not "modify or copy the materials", "use the materials for any commercial purpose, or for any public display", or "'mirror' the materials on any other server". §5: does "not warrant that any of the materials… are accurate, complete or current". **A commercial price-scraping agent conflicts with these terms.** |
| Le Charcutier, Faddoul, Metro Market, Hachem, La Valeur, Storiom, KSC | Yes, Suppy-built JS storefronts | Not checked per store | Not readable (JS). All are Suppy clients ([Google Play developer list](https://play.google.com/store/apps/developer?id=Suppy)). |
| Carrefour Lebanon | Yes (LBP), but blocked | robots.txt returned an empty HTML page (HTTP 200 via curl) and HTTP 503 via WebFetch | The Lebanese terms could not be reached. The sister site Carrefour KSA (same Majid Al Futtaim platform) prohibits use of "any engine, software, tool, agent or other device, including browsers, spiders, robots, avatars or intelligent agents, to navigate or search the site" (from a search snippet of [carrefourksa.com help centre](https://www.carrefourksa.com/mafsau/en/helpcenter/topics/223?articleId=4385); the page itself returned 503) |
| Bou Khalil | None found | — | — |
| Toters (delivery app) | App only; I did not verify supermarket listings or fees for Jbeil | — | — |

### 3.2 Aggregators that already exist

- **SoukCompare** ([soukcompare.com](https://soukcompare.com/)). It compares 586,256 prices across 175 shops, including 41 grocery shops and 135,423 grocery products. It says "We copy every shop's prices from its own website every morning", is "not affiliated" with the shops, and states that shops "cannot pay to change the order". It converts LBP at 89,500 per USD. Covered nearby stores: Tawfeer (9,289 products), Spinneys (15,704), Le Charcutier (16,145), Faddoul (29,397), Metro Market (9,089). Not covered: Carrefour and Bou Khalil ([stores](https://soukcompare.com/stores)).
  - It publishes a **monthly 20-item Basket Index**. On 17 Nov 2026, Tawfeer was cheapest at **$85.29** and Le Charcutier dearest at **$92.41**, a gap of **$7.12 (8%)**. Hachem was $88.56, Faddoul $89.64 and La Valeur $91.04. Spinneys sells only 14 of the 20 items, so it is not ranked ([Basket Index](https://soukcompare.com/basket-index)).
  - There is no terms or licensing page. The contact page invites "Questions about our data… or working together" (hello@soukcompare.com) and lets stores "send your weekly flyer or a price list" ([contact](https://soukcompare.com/contact.html)). Its [robots.txt](https://soukcompare.com/robots.txt) disallows search URLs (`/?`), `/compare` and `/api/...`.
  - **Data-quality warning:** some La Valeur listings are clearly wrong, for example Fairy 1 L at $0.18 and Persil gel 3 L at $0.57 ([Fairy brand page](https://soukcompare.com/groceries/brand/fairy), [Persil brand page](https://soukcompare.com/groceries/brand/persil)). Treat aggregator data as a lead and confirm before buying.
- **Libnanews Consumer Price Index** ([price.libnanews.com](https://price.libnanews.com/en)): a "Local MVP version in progress" that names Metro Market and Carrefour, with "Auto + community" data. Last regional update was 05 Nov 2026. It states no reuse terms.

### 3.3 Official price data (Ministry of Economy and Trade, MoET)

- The MoET Center for Pricing Policies publishes a **weekly basket** report and analysis. An LCPS paper (21 Jul 2026) built on these reports finds the essential food basket rose "5%, 9%, and 13% a year between 2023 and 2026" ([LCPS](https://www.lcps-lebanon.org/en/articles/details/6050/lebanons-cost-of-living-crisis-beyond-monitoring-and-enforcement-of-essential-food-prices)).
- I downloaded the analysis for 19-01-2026 ([PDF](https://www.economy.gov.lb/media/15024/تحليل-التقرير-الاسبوعي-لأسعار-السل-ة-الغذائية-في-19-01-2026.pdf)). It is a PDF whose **Arabic text could not be extracted** (only numbers came out), so it is **not machine-readable** in practice. The index pages on economy.gov.lb returned HTTP 403 to my fetches.
- The PDF contains the figure "89700". Its position suggests it is the LBP/USD rate used, but **that is an inference**.
- The MoET **InfoPrice** monthly ranking of cheapest supermarkets: the latest edition I found is February 2020 ([PDF](https://www.economy.gov.lb/media/12778/summaryinfopricefeb2020en-rank.pdf)). It is outdated.
- During Ramadan 2026 the MoET's "Sawa bil Siyam" initiative had 27 supermarket chains commit to discounts of at least 15% on 21 staples. This comes from a search-result summary of [Lebanese Forces site, 20 Feb 2026](https://lebanese-forces.com/2026/02/20/%D9%88%D8%B2%D8%A7%D8%B1%D8%A9-%D8%A7%D9%84%D8%A7%D9%82%D8%AA%D8%B5%D8%A7%D8%AF-2); the page returned 403, so it is **unverified**.
- **Conclusion:** official data is useful for context and marketing ("basket up 13% a year"), but it cannot drive daily SKU-level buying.

### 3.4 Recommended compliant price-data route

1. **Tawfeer MAX first, by relationship.** Ask the Jbeil store for a weekly PV1/PV2/PV3 price list, or a PDF or WhatsApp flyer, for the ~50 SKUs the village actually buys. Tawfeer is cheapest or near-cheapest on most staples, so most of the basket will go there anyway.
2. **Ask SoukCompare for a data licence or feed** (hello@soukcompare.com). It already publishes daily, dated, SKU-matched prices for Tawfeer, Spinneys, Le Charcutier, Faddoul and Metro Market. One agreement covers five stores and removes the need to scrape at all.
3. **Approach Suppy** (hello@suppy.app; [reseller programme](https://suppy.app/reseller-program)). Tawfeer, Faddoul, Metro Market, Le Charcutier and KSC Batroun all run on Suppy. With each store's written consent, an integration or export could deliver prices, and possibly orders.
4. **Manual weekly check as the fallback.** The driver photographs the shelf tags and flyers for the top 50 SKUs once a week at Spinneys Jbeil and Bou Khalil Jbeil, the two with no feed. The software stores them with a date.
5. **Do not scrape** Spinneys (its ToU forbids commercial use) or Carrefour (blocked; its sister site's ToU bans robots). If the agent reads any storefront, it should do so only with the store's written permission.

---

## 4. Basket price sample: the key number

**Method.** I used 12 staples and picked SKUs that the stores list under the same brand and size, read on **SoukCompare product pages on 2026-11-17**. Each page links to the store's own product page; those links are in the CSV. I checked three Spinneys prices directly on spinneyslebanon.com (oil $6.05, tuna $2.15, Nido $20.39), and all three matched SoukCompare.

Data: [basket-prices.csv](basket-prices.csv).

**Currency.** All five stores price in **USD** online. SoukCompare shows LBP at **89,500 LBP/USD**. This is the BDL official rate, held since early 2024 ([BLOM Bank recap, Feb 2026](https://blog.blominvestbank.com/wp-content/uploads/2026/02/Reflecting-on-2025-The-Forex-and-Commodities-Markets-Recap.pdf); [Pulse, Jun 2026](https://www.pulse.bot/global-economy/news/lebanon-depletes-640-million-of-reserves-to-keep-pound-at-89500-per-dollar-c6dbacf7-b44d-4b85-9131-ee8196c18a76/)). Spinneys' site displays **89,700**. Carrefour prices in LBP. No conversion was needed for the basket.

**Caveats.**
- Online prices come from a specific storefront: Tawfeer Raouche, Zouk, Tabarja and others; Le Charcutier Dekwaneh. **They may differ from in-store prices at Tawfeer MAX Jbeil**, whose PV2 and PV3 prices are not online.
- Eggs are the **cheapest 30-egg tray at each store** (Hawa at Tawfeer, Wilco elsewhere), not the same SKU.
- Faddoul's Nido is a "+10% Off" pack, and Le Charcutier's Nido is a separate listing.
- Rice and sugar are left out of the 3-store basket because no common rice or white-sugar SKU was matched at Tawfeer. That is itself a warning about how hard SKU matching is.

### 4.1 Three stores with full coverage (Tawfeer, Le Charcutier Aoun, Faddoul Sarba), 12 items

| Item | Tawfeer | Le Charcutier | Faddoul | Cheapest vs avg | Cheapest vs dearest |
|---|---|---|---|---|---|
| Sunflower oil Plein Soleil 1.8 L | 5.59 | 5.89 | **5.18** | 6.7% | 12.1% |
| Tuna Siblou 185 g | **1.75** | 2.02 | 1.98 | 8.7% | 13.4% |
| Labneh Candia 900 g | 5.79 | 6.02 | **5.48** | 4.9% | 9.0% |
| Laban Candia 2 kg | 4.84 | 5.00 | **4.55** | 5.1% | 9.0% |
| Pasta Divella Filini 500 g | 1.19 | 1.24 | **1.09** | 7.1% | 12.1% |
| Nido 2.25 kg | 18.87 | 19.73 | **18.75** | 1.9% | 5.0% |
| Eggs 30 (cheapest tray) | 4.79 | 4.54 | **4.40** | 3.9% | 8.1% |
| Brio dish liquid 1.25 L | 2.44 | **2.19** | 2.25 | 4.5% | 10.2% |
| Persil gel 2.5 L | **6.99** | 7.31 | 7.30 | 2.9% | 4.4% |
| Pampers Giant s5 66 pcs | **18.49** | 19.45 | 19.90 | 4.1% | 7.1% |
| Sanita toilet paper 6 rolls | 5.24 | **4.49** | 5.60 | 12.1% | 19.8% |
| Wooden Bakery pita 800 g | 1.06 | 1.06 | 1.06 | 0% | 0% |
| **Basket total ($)** | **77.04** | 78.94 | 77.54 | | |

- Cherry-picked basket: **$74.42**. Average store: $77.84. Cheapest single store: Tawfeer, $77.04. Dearest: Le Charcutier, $78.94.
- **Cherry-picking vs average store: 4.4%.** Vs dearest: **5.7%.** Vs cheapest single store: **3.4%.**
- Between single stores the gap is only **2.4%** (cheapest vs dearest).

### 4.2 Including Spinneys and Metro Market (items all of them list)

| Basket | Tawfeer | Le Charcutier | Faddoul | Spinneys | Metro | Cherry-pick |
|---|---|---|---|---|---|---|
| 6 items (oil, tuna, labneh, pasta, Nido, Persil) | 40.18 | 42.21 | 39.78 | **44.02** | 40.93 | 39.24 |
| 7 items (+ Brio; Metro not listed) | 42.62 | 44.40 | 42.03 | **46.61** | — | 41.43 |

- In the 6-item basket, cherry-picking beats the average store by **5.3%** and Spinneys by **10.9%**. The cheapest single store (Faddoul) is **9.6% below Spinneys**.
- In the 7-item basket, cherry-picking beats Spinneys by **11.1%**, and the cheapest single store is **9.8%** below Spinneys.
- Spinneys is the dearest of the five on every one of these items.

### 4.3 Effect of multi-buy and promotions (Tawfeer)

These use the two deals in the CSV that apply to basket items: Divella Filini **x2** at $0.80 per pack, and Nido 2.25 kg **−10%** at $16.99.
- **Cherry-pick plus promos: $72.37.** That is **7.0%** below the average store, **8.3%** below the dearest and **6.1%** below the cheapest single store.
- **Tawfeer alone using its bundles: $74.77.** This is practically the same as cherry-picking three stores ($74.42), with one stop instead of three.
- On individual bundle SKUs, Tawfeer's deals are **20–33% off**, e.g. "x3" Barilla at −33%. Spinneys' multi-buy found, "2+1 FREE" spaghetti, is only **−7%**.
- PV2 and PV3 at Tawfeer MAX are **unmeasured**. They are the biggest unknown and possibly the biggest saving.

### 4.4 Wider context

Across all 9–10 online shops SoukCompare lists, single-item gaps from cheapest to dearest were larger:

| Item | Range | Gap |
|---|---|---|
| Sunflower oil 1.8 L | $4.38–$6.23 | 30% |
| Siblou tuna | $1.75–$2.15 | 19% |
| Nido pouch 2.25 kg | $17.17–$20.39 | 16% |
| Divella pasta | $1.09–$1.29 | 16% |
| Candia labneh | $5.48–$6.25 | 12% |
| Persil gel 2.5 L | $6.99–$7.89 | 11% |

Source: SoukCompare product pages linked in the CSV. The cheapest is often a store far from Amchit (Hachem in Rifoun, La Valeur in Achrafieh or Ajaltoun).

### 4.5 What this means for the model

- The realistic saving from **cherry-picking across stores near Amchit is ~3–6%** of basket value. That is roughly **$2.50–$4.50 on a ~$78 basket**, before the driver's time and fuel for extra stops.
- The saving from **sending residents' Spinneys-type shopping to Tawfeer or Faddoul is ~10%**.
- The saving from **multi-buy and bundles is ~2–3 extra points** on this basket. On the bundled SKUs alone it is 20–33%.
- **Estimate:** a two-stop run (Tawfeer MAX Jbeil plus one other) captures nearly all of it. Five or six stores do not pay.
- The saving against the **village mini-market** (the real alternative for many residents) was not measured, because those shops publish no prices. A manual shelf check in Amchit is the most important missing number.

---

## 5. Open items for the founder

1. Confirm that "Tawfir Shop" = Tawfeer, using the Instagram handle he saw (expected @tawfeerlebanon).
2. Visit Tawfeer MAX Jbeil and record the PV1/PV2/PV3 prices and thresholds for the 12 basket SKUs. Ask the six questions in §1.4.
3. Record Amchit mini-market prices for the same 12 SKUs. This is the residents' real comparison.
4. Check the delivery fee and minimum order at checkout in the Tawfeer, Spinneys and Le Charcutier apps. They are not published.
5. Email SoukCompare and Suppy about a data feed or licence before building any scraper.
