# Pricing: Village Basket

## 1. The price

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

## 2. The ladder

| rung | what you get | price | why step up |
| --- | --- | --- | --- |
| **Pickup bag** | twice-weekly staples run, collect at the partner shop 5–9 p.m. or next morning | $1.25 + half the saving | the default |
| **Doorstep** | same, left at your door on the driver's loop | +$1.50 | for car-less, older or late-working households: the only group that bought |
| **Basket Club** (only after 3 months of data) | unlimited pickup bags + weekly settlement + "same as last time" standing order | ~$4 a month (to test) | once a household orders ~3 bags a month, the club is cheaper than 3 fees |

Don't launch the club on day one. Memberships only work once the weekly habit exists (`research/business-model.md` §1.4, §1.9).

## 3. The opening offer

- **First bag: no fee.** It costs about $1.25 × ~60 households, $75–175 in total, budgeted in `numbers.json` startup. It answers "the fee is a sure cost and the saving is a maybe" (P025) by showing the saving on the slip before asking for a fee.
- **Founding households (the first 40):** weekly settlement from their 3rd bag instead of paying at each pickup. This partly answers the dekkene-tab objection (24 of 50) without open-ended credit. The cap is real: the cash float only covers about 40 households.
- It ends when the 40 places fill, or at the end of the pilot month, whichever comes first. No fake countdown.

## 4. What to test with real buyers

1. **$1.25 vs $1.50**, one per village cluster (e.g. Kfoun + Ghalboun at $1.25, Bejjeh + Aabaydat at $1.50) for 4 weeks. Measure first-bag → second-bag conversion. The CFO shows $1.50 adds ~$430 to year 1 if conversion holds ($769 → $1,199).
2. **Flat fee vs 3% of bag value** (min $1, max $2.50) on half the founding households, if baskets vary a lot in size.
3. **Real tier capture:** for every run, log the share of bag value that hit a PV2/PV3 price and the average gap. This decides whether the model works at all.

## 5. The panel's own words on price (top three)

- "The $2 is a sure cost while the savings are only a maybe." (P025)
- "A $2 fee on a small daily bag eats whatever I would save, and I lose the tab and the fresh bread I pick up when I need it." (P010)
- "Another fee on top of my groceries. I pass Spinneys and Tawfeer MAX anyway, so I would be paying $2 just to have someone else do what I already do, and I have no proof the bulk prices come out lower than the fee." (P006)

Simulated buyers. These pick what to test; they are not proof.
