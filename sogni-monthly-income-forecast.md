# Sogni Worker Monthly Income Statement — September 2026 (final) & October 2026

*Maintained by the twice-daily earnings task (7:50 AM / 7:50 PM ET). Updated only when numbers change.*
*Last updated: 2026-10-04 23:44 UTC · FX: 1 USD = 1.423858 CAD*

## October 2026 — month to date + forecast (in progress)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 0.96 | 1.37 |
| Subscription accrual (provisional) | 10.97 | 15.62 |
| Combined MTD | 11.93 | 16.99 |
| **Forecast month-end total (pace, provisional)** | **~93** | **~132** |

*October's pool rate is not yet stable: the new-month rate deviates >5× from September's final, so accruals provisionally use September's final rate $0.0005023/unit — the fetch script auto-falls-back until the new rate settles. Pace projection at ~3.99 of 31 days elapsed ($11.93 earned → ~$93/mo) is a noisy read that includes 3 idle days (Oct 2, 3, and most of Oct 4 — workers back online ~6:40 PM EDT Oct 4); the independent October outlook from the 2026-09-30 earnings audit is base case ~$945 (PAYG ~$177 + subscription ~$765).*

***October gap (user instruction 2026-10-04): workers #462/#463 were idle ~3 days (last jobs Oct 1 09:35–09:37 UTC, back online ~6:40 PM EDT Oct 4). Oct 2, 3, and most of Oct 4 earned ~$0 — 3 days of October will be missing from the month's totals.***

## Today (2026-10-04, in progress at 23:44 UTC, ~98.9% of day elapsed)

| | USD | CAD |
|---|---|---|
| PAYG (51% est.) | 0.00 | 0.00 |
| Subscription accrual (pool-rate est., provisional) | 1.61 | 2.29 |
| **Combined** | **1.61** | **2.29** |

*Workers #462/#463 came back online ~6:40 PM EDT (~22:40 UTC) after ~3 days idle; 75 unlimited jobs and 3,208.24 unlimited spark units since return. No PAYG jobs yet this UTC day.* (19:44 ET / 23:44 UTC hourly run)

## September 2026 — final (month closed)

| | USD | CAD |
|---|---|---|
| PAYG earnings (MTD actual) | 596.59 | 849.55 |
| Subscription accrual (final estimate) | 421.26 | 599.88 |
| **Combined final** | **1,017.85** | **1,449.42** |

*Subscription is api.sogni.ai's estimatedPayoutUsd — still an estimate until revenue reconciles (~Nov 15 payout window). Closed-day Sep 30: PAYG $7.33 + subscription $27.64 = $34.98 (CA$49.81). Closed-day Oct 1: PAYG $0.96 + subscription $9.36 = $10.33 (CA$14.71). Closed-day Oct 2: $0.00 — workers idle all day. Closed-day Oct 3: $0.00 — workers still idle. Oct 4 in progress (23:44 UTC sample): PAYG $0.00 + subscription $1.61 = $1.61 (CA$2.29) — workers back online ~22:40 UTC.*

## Subscription — per worker (September final)

| Worker | Render units | USD |
|---|---|---|
| #462 | 445,836 | 223.93 |
| #463 | 363,898 | 182.77 |
| #467 | 27,424 | 13.77 |
| #478 | 1,567 | 0.79 |
| **Fleet total** | **838,724** | **421.26** |

*Fleet share: ~0.19% of pool. Pool: US$64,676.65 live estimate (11:50 UTC read; was $64,676.76 at 23:50 UTC). Per-worker USD = pro-rata of fleet USD by units.*

## Prior month

| | USD |
|---|---|
| August 2026 (est.) | 139.95 |

*August 2026 full detail from Month view: total US$455.92 (PAYG 315.98 + Unlimited 139.94).*

## Payout schedule

- **August 2026** → ~US$139.95, USDC on Base, **Oct 16, 2026**
- **September 2026** → ~US$1,017.85 (subscription ~$421.26 est. until reconciliation), USDC on Base, **Nov 15, 2026**
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
