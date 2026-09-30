# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 06:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 591.82 | 839.50 |
| Subscription accrual (MTD estimate) | 413.41 | 586.43 |
| Combined MTD | 1,005.23 | 1,425.93 |
| **Forecast month-end total** | **1,029.57** | **1,460.46** |

*Subscription MTD from api.sogni.ai (413.41). 29 of 30 days closed, current day ~29.1% elapsed (~97.6% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,030.63 — combined MTD ticked up but pool-rate drift nudged the sub estimate down. Sep 29 closed at $33.89 (PAYG $7.56 + subscription ~$26.33 at the live pool rate).*

## Today (2026-09-30, in progress at 06:58 UTC, ~29.1% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 2.57 | 3.64 |
| Subscription accrual (pool-rate est.) | 6.99 | 9.91 |
| **Combined** | **9.56** | **13.56** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 421,666 | 218.68 |
| #463 | 346,504 | 179.70 |
| #467 | 27,424 | 14.22 |
| #478 | 1,567 | 0.81 |
| **Fleet total** | **797,160** | **413.41** |

*Fleet share: ~0.63% of pool. Pool: US$64,626.69 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
