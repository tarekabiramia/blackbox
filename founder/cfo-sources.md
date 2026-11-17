# Where each number comes from

| input | value | source / status |
| --- | --- | --- |
| Fee per bag | $1.25 | Panel price answers: indifference $1.01, median "getting expensive" $2.00, acceptable range $0.51–$2.50 (`pricing-curve.md`). Decision in `pricing.md`. |
| Half of the bulk saving per bag | $1.10 | **ESTIMATE.** Assumes a $55 bag, 50% of its value hitting Tawfeer MAX PV2/PV3 tiers, an average tier gap of 8% below PV1, split 50/50. The thresholds and gaps are **not public** (`research/suppliers.md` §A). Measure them on the shelf. |
| Doorstep add-on, averaged | $0.45 | ESTIMATE: 30% of bags take the $1.50 doorstep option. |
| Bag value | $55 | ESTIMATE. Late-2026 household food spend is estimated at $210–300 a month (`research/market-lebanon.md` §2). A stock-up bag of staples is about a quarter of that. |
| Bags, labels, receipt | $0.15 | ESTIMATE; get a quote from a Jbeil packaging supplier. |
| Pickup-host commission | $0.25 | PROPOSAL to the partner mini-market; to negotiate. |
| Payment and cash shortfalls | 0.6% of bag | Whish Pay merchant fee 1%; wallet-to-wallet transfers free (`research/market-lebanon.md` §5). Mixed with cash. ESTIMATE. |
| Write-offs | 0.5% of bag | ESTIMATE for shelf-stable goods. Refused items mostly go back to stock. No fresh produce at the start. |
| Fuel | $8 a run | ~60 km run day (Amchit, Tawfeer MAX Qartaboun, Kfoun/Ghalboun/Bejjeh/Aabaydat, doorstep drops, back) at ~10 L/100 km loaded, with 95 octane at LBP 2,343,000 / 20 L ≈ $1.31/L on 17 Nov 2026 (`research/market-lebanon.md` §3–4; corrected per `ops.md`). |
| Driver (what-if only) | $22 a run | ESTIMATE: legal daily minimum LBP 1.3M (~$14.5) plus transport allowance ~$5–9 (`research/market-lebanon.md` §4). |
| Software | $16 a month | Lean stack at ~200 orders/month: WhatsApp Cloud API, LLM parsing, small VPS (`research/business-model.md` §4.6). |
| Runs a month | 9 | Twice a week (Tue/Fri), ~4.3 weeks. |
| Capacity | 20 bags a run | ESTIMATE for a private car with ~$55 staple bags. Test it with real bags. |
| Ramp 6 → 20 bags a run | | The panel's buyers say 3 purchases a month, so 20 bags a run × 9 runs ≈ 60 regular households. All 3 panel buyers were car-less households. The ramp is a judgement, to be replaced by pilot data. |
| Registration and accountant | $300 | ESTIMATE; get a quote. |
| Cash float | $2,200 | Two runs of 20 bags × $55, fronted before weekly settlement, recovered (`ops.md`). Whish prepayment at confirmation would shrink it. |
| Vehicle wear and commercial-use insurance | $20 a month | PLACEHOLDER until quoted (`ops.md`). |
| Accountant, ongoing | $25 a month | PLACEHOLDER ESTIMATE; get a quote. |
