# CFO: Village Basket

## The CFO's note (read this first)

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

# Unit economics: Village Basket v2: twice-weekly staples run, founder drives, receipt-backed savings split

Every number below comes from the input file. Nothing is looked up or guessed.

## One bag

| line | per bag |
| --- | ---: |
| Price | $2.80 |
| Bags, labels, printed receipt and savings slip (est.) | -$0.15 |
| Pickup-host commission to the partner mini-market (proposed) | -$0.25 |
| Payment fees and cash shortfalls, ~0.6% of a $55 bag (est.) | -$0.33 |
| Refused or damaged items written off, ~0.5% of a $55 bag (est.) | -$0.28 |
| Doorstep drops: extra fuel and time, averaged over all bags (est.) | -$0.10 |
| **Contribution** (what each bag leaves to pay the fixed costs) | **$1.69** (60%) |

## The margin that matters

Fixed costs: $178 a month (Fuel, ~60 km run day at $8 a run x 9 runs (ops.md estimate) $72, Software, lean stack $16, Business phone line and data (est.) $10, Crates, cool boxes, wear (est.) $15, Printed flyers and village posters (est.) $20, Vehicle wear and commercial-use insurance, placeholder until quoted (ops.md) $20, Accountant, ongoing bookkeeping, placeholder until quoted (est.) $25).

- **Break-even: 12 bags a day.** Below that you lose money every month.
- **Profit margin at your plan** (20 a day): **25%** of every sale, after every cost.
- Capacity: 20 a day.

## Year 1, month by month

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

## What if

| scenario | margin at plan | break-even a day | year 1 profit |
| --- | ---: | ---: | ---: |
| Base plan | 25% | 12 | $769 |
| Price -10% | 17% | 15 | $288 |
| Volume -20% | 16% | 12 | $188 |
| Unit costs +15% | 19% | 13 | $483 |

## Red flags

- The startup spend is not earned back within year 1.
