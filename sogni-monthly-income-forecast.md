# Sogni Worker Monthly Income Statement — September 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-09-30 07:58 UTC · FX: 1 USD = 1.418513 CAD*

## September 2026 — month to date + month-end forecast

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 592.44 | 840.38 |
| Subscription accrual (MTD estimate) | 413.97 | 587.22 |
| Combined MTD | 1,006.41 | 1,427.61 |
| **Forecast month-end total** | **1,029.32** | **1,460.10** |

*Subscription MTD from api.sogni.ai (413.97). 29 of 30 days closed, current day ~33.2% elapsed (~97.8% of month elapsed). Forecast = linear extrapolation (MTD ÷ elapsed fraction); prior forecast 1,029.57 — combined MTD ticked up ~$1.2, holding the forecast nearly flat. Sep 29 closed at $33.84 (PAYG $7.56 + subscription ~$26.28 at the live pool rate).*

## Today (2026-09-30, in progress at 07:58 UTC, ~33.2% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 3.18 | 4.51 |
| Subscription accrual (pool-rate est.) | 8.29 | 11.76 |
| **Combined** | **11.47** | **16.28** |

## Subscription — per worker (September MTD)

| Worker | Render units | USD |
|---|---|---|
| #462 | 423,155 | 219.05 |
| #463 | 347,556 | 179.91 |
| #467 | 27,424 | 14.20 |
| #478 | 1,567 | 0.81 |
| **Fleet total** | **799,702** | **413.97** |

*Fleet share: ~0.64% of pool. Pool: US$64,628.78 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

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
