# Sogni Income History — Novacore

Private log of the hourly Sogni worker income reports for Novacore's Fast
Network workers (#462 and #463).

## Files

- **hourly-income.csv** — one row per hourly collection run (UTC timestamps).
  Backfilled 2026-09-30 from the local hourly collection git history
  (2026-09-29 → 2026-09-30); each hourly run appends a row.
- **sogni-monthly-income-forecast.md** — the running monthly income-statement
  forecast (MTD actuals + month-end forecast, USD and CAD).

## Columns (hourly-income.csv)

| column | meaning |
|---|---|
| timestamp_utc | when the hourly run sampled the data (UTC) |
| timestamp_toronto | same moment in America/Toronto time (EDT/EST with DST handled) |
| day_label | the in-progress day (e.g. "30 Sep 2026") |
| today_total_usd | combined today earnings, USD (PAYG + subscription estimate) |
| today_payg_usd | pay-as-you-go earnings today, USD (51% share) |
| today_sub_usd | subscription/unlimited accrual today, USD |
| today_total_cad | combined today earnings in CAD |
| day_8pm_total_usd | combined earnings in the founder's day: 8pm Toronto to 8pm Toronto (during EDT this equals the UTC dashboard day exactly) |
| day_8pm_payg_usd | PAYG portion of the 8pm-to-8pm day |
| day_8pm_sub_usd | subscription portion of the 8pm-to-8pm day |
| day_8pm_total_cad | 8pm-to-8pm day total in CAD |
| month_forecast_usd | month-end projection: (8pm-day earnings / hours elapsed x 24) x days in month. Reads low early in the day until earnings accumulate |
| month_forecast_cad | month-end projection in CAD |
| fx_usdcad | mid-market FX rate used |
| today_unlimited_units | Unlimited Spark units today |
| yesterday_total_usd | previous closed dashboard (UTC) day's combined total, USD |
| yesterday_8pm_total_usd | last COMPLETED 8pm-Toronto to 8pm-Toronto window, USD (exact year-round; in winter the 8-9pm edges are adjusted) |
| yesterday_8pm_payg_usd | PAYG portion of that window |
| yesterday_8pm_sub_usd | subscription portion of that window |
| yesterday_8pm_total_cad | that window's total in CAD |
| month_usd | month-to-date subscription earnings, USD (live estimate) |
| month_units | month-to-date render units |
| w462_mtd_usd / w463_mtd_usd | per-worker MTD subscription split, USD |

## Methodology notes

- PAYG "today" comes from the Sogni dashboard Day view (an estimate until finalized).
- Daily subscription earnings = today's Unlimited Spark units × live monthly
  pool USD-per-unit. Caveats: units are assumed to map 1:1 to pool render
  units; the daily unit figure may cover only one worker; the pool rate drifts
  until month close.
- Payouts land ~45 days after month-end in USDC on Base.
