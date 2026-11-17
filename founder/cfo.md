# CFO: Village Basket

## The CFO's note (read this first)

**The original pitch does not work.** Daily runs at a $2 fee, with the till price passed straight through (`numbers-v1.json`), need **30 bags a day** to break even against a car that carries about 20. They lose **$7,498 in year 1**. Run it with `python3 .claude/skills/founder-cfo/unit_economics.py founder/numbers-v1.json`.

**The redesigned version (v2, below) works only as a small, founder-run operation.**
- **The margin.** Each bag brings in $2.80: a $1.25 fee, plus half of the bulk saving (~$1.10), plus $0.45 average doorstep fees. Its own costs are $1.11, so each bag leaves **$1.69 (60%)**. At the plan of 20 bags a run, twice a week, the profit margin is **36%** and year 1 makes **$1,417** on operations.
- **That $1,417 is the founder's pay.** It assumes he drives the runs himself (no driver in the fixed costs). Add a half-day driver at ~$22 a run and v2 breaks even at **22 bags a run, above what one car can carry**. Year 1 is then **−$959**. A paid driver only makes sense with a van carrying ~40 bags, which gives +$1,946 in year 1 on a 22-bag break-even.
- **The line to watch: the bulk saving.** $1.10 of the $2.80 per bag is the business's half of the gap between Tawfeer MAX's single-item price and its quantity/carton price. Neither the thresholds nor the gaps are published anywhere (`research/suppliers.md`). If pooled orders never reach the tiers, revenue falls to $1.70 a bag. Break-even jumps to **24 bags a run** and year 1 becomes **−$474**. Measure this on the shelf before anything else.
- **Cash.** $1,875 to start. $1,100 of that is a float to pay the till for one run before customers pay at pickup, and it comes back the same evening. The sunk startup spend is **$775**, earned back in **month 9**. Counting the float, the founder needs about **$1,900** in hand. With members paying by Whish when they confirm, the float shrinks.

**Three ways to improve the margin (tool what-ifs, not guesses):**
1. **Fee $1.50 instead of $1.25:** year 1 goes from $1,417 to **$1,847** and break-even drops to 8 bags a run. The panel's indifference price was $1.01 and the median "getting expensive" was $2.00, so $1.50 is testable. Test $1.25 against $1.50 in two villages.
2. **Bigger bags.** The savings share and the payment and write-off costs all scale with bag value, but the fee and fuel do not. A $55 stock-up bag is the assumption; push "weekly stock-up" over "top-up" in the offer.
3. **More bags per run, not more runs.** Fuel is the only real fixed cost per run. Moving from 20 to 40 bags a run needs a bigger vehicle, which is when a paid driver starts to pay for itself.

**Sensitivity.** Volume −20% leaves year 1 at $836, and volume −40% leaves $255: still positive, because fixed costs are only $124 a month. Price −10% gives $936.

**Board conditions about money (`board.md`):** C1 (prove the gap) is **not met**: it depends on the tier gap, which is unmeasured. C8 (who fronts the cash) is answered with a $1,100 float, or Whish prepayment. C9 (density) is defined: **9 bags a run, twice a week, about 6 regular households per run, is break-even**. 20 bags a run is the plan.

**What this is, honestly:** a low-risk, ~$1,900 experiment that pays the founder roughly $100–150 a month once it is running. It is not a living. Its value is as a live proof of a pooled village channel, which is the asset the plan (`business-plan.md`) builds on.

Revenue is before tax. Lebanon charges 11% VAT once turnover passes LBP 5bn (~$55,900); this business stays far below that if it acts as a fee-paid buying agent, not a reseller (confirm). An accountant should check the structure (agent vs reseller), any payroll, and tax before money moves. Not financial, tax or legal advice.

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

Fixed costs: $124 a month (Fuel, ~54 km loop at $7 a run x 9 runs $63, Software, lean stack $16, Business phone line and data (est.) $10, Crates, cool boxes, wear (est.) $15, Printed flyers and village posters (est.) $20).

- **Break-even: 9 bags a day.** Below that you lose money every month.
- **Profit margin at your plan** (20 a day): **36%** of every sale, after every cost.
- Capacity: 20 a day.

## Year 1, month by month

| month | bags a day | revenue | profit | cumulative (after $1,875 startup) |
| ---: | ---: | ---: | ---: | ---: |
| 1 | 6 | $151 | -$33 | -$1,908 |
| 2 | 9 | $227 | $13 | -$1,895 |
| 3 | 12 | $302 | $59 | -$1,836 |
| 4 | 14 | $353 | $89 | -$1,747 |
| 5 | 16 | $403 | $119 | -$1,628 |
| 6 | 17 | $428 | $135 | -$1,493 |
| 7 | 18 | $454 | $150 | -$1,344 |
| 8 | 19 | $479 | $165 | -$1,179 |
| 9 | 20 | $504 | $180 | -$998 |
| 10 | 20 | $504 | $180 | -$818 |
| 11 | 20 | $504 | $180 | -$638 |
| 12 | 20 | $504 | $180 | -$458 |

- **Year 1 operating profit: $1,417** on $4,813 of revenue.
- After the $1,875 startup spend: -$458.
- Startup money earned back: not within year 1.
- Cash you need before it pays for itself: **$1,908**.

## What if

| scenario | margin at plan | break-even a day | year 1 profit |
| --- | ---: | ---: | ---: |
| Base plan | 36% | 9 | $1,417 |
| Price -10% | 29% | 10 | $936 |
| Volume -20% | 30% | 9 | $836 |
| Unit costs +15% | 30% | 10 | $1,131 |

## Red flags

- The startup spend is not earned back within year 1.
