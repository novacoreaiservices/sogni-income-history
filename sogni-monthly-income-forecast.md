# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 14:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 594.13 | 842.78 |
| Subscription accrual (MTD estimate) | 417.25 | 591.87 |
| Combined MTD | 1,011.38 | 1,434.66 |
| **Forecast month-end total** | **1,024.21** | **1,452.86** |

*Subscription MTD from api.sogni.ai (417.25). 29 of 30 days closed, current day ~62.4% elapsed (~98.7% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,024.58 — combined MTD ticked up ~$1.06 but the hourly pace eased, nudging the forecast down ~$0.37. Sep 29 closed at ~$33.68 (PAYG $7.56 + subscription ~$26.12 at the live pool rate).*

## Today (2026-09-30, in progress at 14:58 UTC, ~62.4% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 4.88 | 6.92 |
| Subscription accrual (pool-rate est.) | 16.35 | 23.19 |
| **Combined** | **21.22** | **30.11** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 432,995 | 221.50 |
| #463 | 353,658 | 180.92 |
| #467 | 27,424 | 14.03 |
| #478 | 1,567 | 0.80 |
| **Fleet total** | **815,643** | **417.25** |

*Fleet share: ~0.63% of pool. Pool: US$64,655.48 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
