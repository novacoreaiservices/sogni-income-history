# Sogni Worker Monthly Income Statement — September 2026 (final) & October 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-10-01 17:58 UTC · FX: 1 USD = 1.421278 CAD*

## October 2026 — month to date + forecast (in progress)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 0.96 | 1.37 |
| Subscription accrual (provisional) | 9.36 | 13.31 |
| Combined MTD | 10.33 | 14.68 |
| **Forecast month-end total (pace, provisional)** | **~428** | **~608** |

*October's pool rate is not yet stable: at 01:01 UTC it read $0.204/unit on only ~1,626 units (the pool budget is allocated early and dilutes as the month fills). Accruals use September's final rate $0.0005023/unit and are marked provisional — the fetch script auto-falls-back while the new-month rate deviates >5× from the prior month's final rate. Pace projection at 74.91% of Oct 1 elapsed ($10.33/day pace → ~$428/mo) is a day-one read only; the independent October outlook from the 2026-09-30 earnings audit is base case ~$945 (PAYG ~$177 + subscription ~$765).*

## Today (2026-10-01, in progress at 17:58 UTC, ~74.91% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 0.96 | 1.37 |
| Subscription accrual (pool-rate est., provisional) | 9.36 | 13.31 |
| **Combined** | **10.33** | **14.68** |

## September 2026 — final (month closed)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 596.59 | 847.92 |
| Subscription accrual (final estimate) | 421.28 | 598.75 |
| **Combined final** | **1,017.87** | **1,446.68** |

*Subscription is api.sogni.ai's estimatedPayoutUsd — still an estimate until revenue reconciles (~Nov 15 payout window). Closed-day Sep 30: PAYG $7.33 + subscription $27.64 = $34.98 (CA$49.71).*

## Subscription — per worker (September final)

| Worker | Render units | USD |
|---|---|---|
| #462 | 445,836 | 223.94 |
| #463 | 363,898 | 182.78 |
| #467 | 27,424 | 13.77 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **838,724** | **421.28** |

*Fleet share: ~0.65% of pool. Pool: US$64,678.65 live estimate. Per-worker USD = pro-rata of fleet USD by units.*

## Prior month

| | USD |
|---|---|
| August 2026 (est.) | 139.95 |

*August 2026 full detail from Month view: total US$455.92 (PAYG 315.98 + Unlimited 139.94).*

## Payout schedule

- **August 2026** → ~US$139.95, USDC on Base, **Oct 16, 2026**
- **September 2026** → ~US$1,017.87 (subscription ~$421.28 est. until reconciliation), USDC on Base, **Nov 15, 2026**
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
  render units. In the first days of a month the live pool rate is unstable
  (tiny unit base), so accruals provisionally use the prior month's final
  rate until the new rate settles.
- CAD conversions use the mid-market rate noted above, refreshed each run.
- Forecasts are projections, not settled payouts.
