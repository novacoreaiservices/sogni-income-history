# Sogni Worker Monthly Income Statement — September 2026 (final) & October 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-10-05 21:44 UTC · FX: 1 USD = 1.42482 CAD*

## October 2026 — month to date + forecast (in progress)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 2.03 | 2.89 |
| Subscription accrual (Oct projected rate) | 21.70 | 30.92 |
| Combined MTD | 23.73 | 33.81 |
| **Forecast month-end total (pace)** | **~150** | **~214** |

*The October pool rate switched on Oct 5 ~12:44 UTC from the inflated dashboard-display raw rate (~$0.0023475/unit, ~6.9× too high early in the month because the leaderboard pairs full-month revenue with month-to-date spark) to the projected rate ~$0.0003437/unit (pool $63,719 ÷ projected 185.4M spark — auditor-validated, TypeSafe Jev 0.92/0.99, user-approved switch). October MTD before Oct 5 was overstated on the dashboard-display basis. Pace projection at ~4.91 of 31 days elapsed ($23.73 earned → ~$150/mo) is noisy and includes the 3 idle days (Oct 2, 3, and most of Oct 4 — workers back online ~6:40 PM EDT Oct 4); the independent October outlook from the 2026-09-30 earnings audit is base case ~$945 (PAYG ~$177 + subscription ~$765). Season 12 started Oct 5 00:00 UTC — worker rewards increasingly funded by market-bought SOGNI; watch for rate drift through the month.*

***October gap (user instruction 2026-10-04): workers #462/#463 were idle ~3 days (last jobs Oct 1 09:35–09:37 UTC, back online ~6:40 PM EDT Oct 4). Oct 2, 3, and most of Oct 4 earned ~$0 — 3 days of October will be missing from the month's totals.***

## October 2026 — subscription per worker (MTD, 21:44 UTC)

| Worker | Render units | USD |
|---|---|---|
| #462 | 41,904 | 14.40 |
| #463 | 27,142 | 9.33 |
| #467 | 0 | 0.00 |
| #478 | 0 | 0.00 |
| **Fleet total** | **69,047** | **23.73** |

*Fleet share: ~0.24% of pool. Pool: US$63,718.84 live estimate (21:44 UTC read). Per-worker USD = pro-rata of fleet USD by units. Oct 2–4 units are near-zero because of the idle gap; Oct 5 is the first full day back.*

## Today (2026-10-05, in progress at 21:44 UTC, ~21.7h into the 8pm–8pm Toronto day)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 1.07 | 1.52 |
| Subscription accrual (Oct projected rate $0.0003437/unit) | 16.02 | 22.83 |
| **Combined** | **17.09** | **24.35** |

*Workers #462/#463 online; 855 unlimited jobs and 46,621.18 unlimited spark units plus 49 PAYG jobs (3,987.01 SOGNI tokens) since the accounting day rolled over.*

## September 2026 — final (month closed)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 596.59 | 849.55 |
| Subscription accrual (final estimate) | 421.34 | 599.89 |
| **Combined final** | **1,017.93** | **1,449.39** |

*Subscription is api.sogni.ai's estimatedPayoutUsd — still an estimate until revenue reconciles (~Nov 15 payout window). Closed-day Sep 30: PAYG $7.33 + subscription $27.64 = $34.98 (CA$49.81). Closed-day Oct 1: PAYG $0.96 + subscription $9.36 = $10.33 (CA$14.71). Closed-day Oct 2: $0.00 — workers idle all day. Closed-day Oct 3: $0.00 — workers still idle. Closed-day Oct 4: PAYG $0.00 + subscription $1.90 = $1.90 (CA$2.71) — workers back online ~22:40 UTC. Oct 5 in progress (21:44 UTC sample): PAYG $1.07 + subscription $16.02 = $17.09 (CA$24.35) — on the new projected pool-rate basis; Oct 1–4 accrual figures above are on the prior inflated dashboard-display basis.*

## Subscription — per worker (September final)

| Worker | Render units | USD |
|---|---|---|
| #462 | 445,836 | 223.97 |
| #463 | 363,898 | 182.80 |
| #467 | 27,424 | 13.78 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **838,724** | **421.34** |

*Fleet share: ~0.09% of pool. Pool: US$64,687.55 live estimate (23:50 UTC read). Per-worker USD = pro-rata of fleet USD by units.*

## Prior month

| | USD |
|---|---|
| August 2026 (est.) | 139.95 |

*August 2026 full detail from Month view: total US$455.92 (PAYG 315.98 + Unlimited 139.94).*

## Payout schedule

- **August 2026** → ~US$139.95, USDC on Base, **Oct 16, 2026**
- **September 2026** → ~US$1,017.93 (subscription ~$421.34 est. until reconciliation), USDC on Base, **Nov 15, 2026**
- **October 2026** → USDC on Base, **Dec 16, 2026** (confirmed on dashboard subscription tab 2026-10-05)
- Destination: `0x0328...1f91`

## October 15 reconciliation (planned)

When the August payout lands (USDC on Base, expected ~Oct 15, 2026), a
one-time scheduled task will compare the August estimate (~US$139.95) against
the actual finalized payout: estimate vs actual, variance in USD and %.
Results will be recorded here.

## November 15 reconciliation (planned)

When the September payout lands (USDC on Base, expected Nov 15, 2026), a
one-time scheduled task will compare the final September forecast above
against the actual finalized payout: forecast vs actual totals and per-worker
variance in USD and %. Results will be recorded here.

## Assumptions & caveats

- Subscription figures are live estimates until month close; the pool $/unit
  drifts as the month progresses.
- PAYG "Est. Earnings USD (51%)" is the dashboard's estimate until finalized.
- Pool-rate method: today's Unlimited Spark units × (October pool USD ÷
  total render units MTD). Assumes Unlimited Spark units map 1:1 to pool
  render units. Early in a month the leaderboard's raw rate is inflated
  (it pairs full-month revenue with month-to-date spark), so since
  Oct 5 ~12:44 UTC the pipeline uses the projected rate = pool USD ÷
  (total render spark ÷ elapsed fraction of the UTC month), with the 5×
  guard applied to the projected rate. Figures before Oct 5 12:44 UTC
  were on the inflated dashboard-display basis (~6.9× too high).
- CAD conversions use the mid-market rate noted above, refreshed each run.
- Forecasts are projections, not settled payouts.
