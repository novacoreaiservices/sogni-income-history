# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 16:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 594.73 | 843.63 |
| Subscription accrual (MTD estimate) | 418.23 | 593.26 |
| Combined MTD | 1,012.96 | 1,436.90 |
| **Forecast month-end total** | **1,022.94** | **1,451.05** |

*Subscription MTD from api.sogni.ai (418.23). 29 of 30 days closed, current day ~70.7% elapsed (~99.0% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,023.31 — PAYG MTD +$0.15 and subscription +$0.90, but the combined pace eased slightly, nudging the forecast down ~$0.37. Sep 29 closed at ~$33.48 (PAYG $7.56 + subscription ~$25.92 at the live pool rate).* PAYG MTD carried forward from the 15:58 UTC update plus today's incremental PAYG ($5.48 − $5.33); the API read this run returns subscription MTD only.*

## Today (2026-09-30, in progress at 16:58 UTC, ~70.7% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 5.48 | 7.77 |
| Subscription accrual (pool-rate est.) | 18.98 | 26.92 |
| **Combined** | **24.47** | **34.70** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 435,613 | 221.92 |
| #463 | 356,343 | 181.54 |
| #467 | 27,424 | 13.97 |
| #478 | 1,567 | 0.80 |
| **Fleet total** | **820,946** | **418.23** |

*Fleet share: ~0.65% of pool. Pool: US$64,658.61 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

## Prior month

| | USD |
|---|---|
| August 2026 (est.) | 139.95 |

*August 2026 full detail from Month view: total US$455.92 (PAYG 315.98 + Unlimited 139.94).*

## Payout schedule

- **August 2026** → ~US$139.95, USDC on Base, **Oct 16, 2026**
- **September 2026** → forecast TBD, USDC on Base, **Nov 15, 2026**
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
- Pool-rate method: today's Unlimited Spark units × (September pool USD ÷
  total render units MTD). Assumes Unlimited Spark units map 1:1 to pool
  render units.
- CAD conversions use the mid-market rate noted above, refreshed each run.
- Forecasts are projections, not settled payouts.
