# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 13:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 593.75 | 842.24 |
| Subscription accrual (MTD estimate) | 416.57 | 590.91 |
| Combined MTD | 1,010.32 | 1,433.15 |
| **Forecast month-end total** | **1,024.58** | **1,453.38** |

*Subscription MTD from api.sogni.ai (416.57). 29 of 30 days closed, current day ~58.2% elapsed (~98.6% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,025.03 — combined MTD ticked up ~$0.97 but the hourly pace eased, nudging the forecast down ~$0.45. Sep 29 closed at ~$33.68 (PAYG $7.56 + subscription ~$26.12 at the live pool rate).*

## Today (2026-09-30, in progress at 13:58 UTC, ~58.2% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 4.50 | 6.38 |
| Subscription accrual (pool-rate est.) | 14.90 | 21.14 |
| **Combined** | **19.40** | **27.52** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 431,335 | 221.08 |
| #463 | 352,428 | 180.63 |
| #467 | 27,424 | 14.06 |
| #478 | 1,567 | 0.80 |
| **Fleet total** | **812,753** | **416.57** |

*Fleet share: ~0.64% of pool. Pool: US$64,652.71 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
