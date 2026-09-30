# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 23:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 596.59 | 846.27 |
| Subscription accrual (MTD estimate) | 421.27 | 597.58 |
| Combined MTD | 1,017.86 | 1,443.85 |
| **Forecast month-end total** | **1,017.91** | **1,443.91** |

*Subscription MTD from api.sogni.ai (421.27). 29 of 30 days closed, current day ~99.9% elapsed (~99.996% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,017.87 — PAYG MTD grew ~$0.19 and subscription ~$0.04 while the month elapsed fraction rose, nudging the forecast up ~$0.04.*

## Today (2026-09-30, in progress at 23:58 UTC, ~99.9% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 7.33 | 10.40 |
| Subscription accrual (pool-rate est.) | 27.64 | 39.21 |
| **Combined** | **34.98** | **49.62** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 445,832 | 223.93 |
| #463 | 363,898 | 182.78 |
| #467 | 27,424 | 13.77 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **838,720** | **421.27** |

*Fleet share: ~0.65% of pool. Pool: US$64,675.57 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
