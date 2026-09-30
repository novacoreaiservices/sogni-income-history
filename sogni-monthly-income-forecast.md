# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 20:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 595.52 | 844.76 |
| Subscription accrual (MTD estimate) | 419.82 | 595.52 |
| Combined MTD | 1,015.34 | 1,440.27 |
| **Forecast month-end total** | **1,019.64** | **1,446.37** |

*Subscription MTD from api.sogni.ai (419.82). 29 of 30 days closed, current day ~87.4% elapsed (~99.58% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,020.51 — combined MTD grew ~$0.55 while the month elapsed fraction rose, nudging the forecast down ~$0.87.*

## Today (2026-09-30, in progress at 20:58 UTC, ~87.4% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 6.26 | 8.88 |
| Subscription accrual (pool-rate est.) | 23.77 | 33.71 |
| **Combined** | **30.03** | **42.59** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 440,970 | 222.85 |
| #463 | 360,751 | 182.31 |
| #467 | 27,424 | 13.86 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **830,711** | **419.82** |

*Fleet share: ~0.65% of pool. Pool: US$64,672.54 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
