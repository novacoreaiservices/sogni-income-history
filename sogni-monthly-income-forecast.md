# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 22:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 595.67 | 844.97 |
| Subscription accrual (MTD estimate) | 420.82 | 596.94 |
| Combined MTD | 1,016.49 | 1,441.91 |
| **Forecast month-end total** | **1,017.95** | **1,443.98** |

*Subscription MTD from api.sogni.ai (420.82). 29 of 30 days closed, current day ~95.7% elapsed (~99.86% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,018.79 — subscription MTD grew ~$0.42 while the month elapsed fraction rose, nudging the forecast down ~$0.84.*

## Today (2026-09-30, in progress at 22:58 UTC, ~95.7% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 6.42 | 9.10 |
| Subscription accrual (pool-rate est.) | 26.47 | 37.54 |
| **Combined** | **32.88** | **46.64** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 444,062 | 223.46 |
| #463 | 363,224 | 182.78 |
| #467 | 27,424 | 13.80 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **836,277** | **420.82** |

*Fleet share: ~0.65% of pool. Pool: US$64,675.25 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
