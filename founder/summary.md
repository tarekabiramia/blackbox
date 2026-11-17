# Summary

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
