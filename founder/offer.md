# The offer: Village Basket

Method: the Offers lens in `.claude/skills/founder-board/lenses.md`, a summary of a published framework, not anyone's words. Inputs: `panel/results.md` (v1 panel, 3 buy · 47 pass), `competitors.md`, `numbers.json`, `board.md`.

## 1. The problem list (in the buyers' words; counts are from the 50 v1 answers)

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

## 2. Solutions, scored (value to buyer 1–5 / cost to deliver 1–5)

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

## 3. The stack

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

## 4. Value-equation scores (1–10)

| element | v1 pitch | v2 offer | what moved it |
| --- | ---: | ---: | --- |
| Dream outcome | 4 ("cheaper, maybe") | 6 | outcome stated as "your stock-up done, never above shelf price" |
| Perceived likelihood | 2 (strangers, no proof) | 6 | receipt + slip, a named neighbour, the village shop as host, refuse-at-pickup |
| Time delay | 6 (same day) | 5 | twice-weekly instead of daily; fine for stock-ups, worse for urgent items |
| Effort and sacrifice (higher = less effort) | 3 | 6 | standing order, list the night before, a 16-hour pickup window or the doorstep, keep choosing your own produce, keep the dekkene |

## 5. Re-test

The new offer is in `pitch.md` (the old one is `pitch-v1.md`; the v1 panel is kept in `panel-v1/`). It was re-run on `/founder-consumer --quick` (20 buyers, same customer, same seed 2026). Result: see section 6, added after the run.

## 6. Re-test result (20 simulated buyers, same customer profile, seed 2026)

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
