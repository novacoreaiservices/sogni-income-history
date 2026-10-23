# hourly-income.csv — issues log

Generated: 2026-10-23T04:38:46Z (analysis snapshot below). Companion file: `daily-income-oct-2026.csv`.
Nothing in `hourly-income.csv` was edited or deleted for this audit. This file only documents what is in it.

## Analysis snapshot

- File analysed: `hourly-income.csv` in this repo, as of its last row at 2026-10-23T03:44:41Z.
- Data rows analysed: 387 (2026-09-29T06:26:58Z to 2026-10-23T03:44:41Z, after converting all timestamps to UTC).
- SHA-256 of the analysed file content: `e608dc62eee6d866cc0012dad13314b35201caeddff04e98bcf29ea4d0a7bf66`
- GitHub blob SHA of the analysed version: `324945d653b11006b1b07ceb72cdd7554b034c5e`
- Rows the hourly pipeline appends after that snapshot are new samples, not edits; they are outside this analysis.

## Definitions used (so the counts are reproducible)

- **Duplicated clock-hour:** two or more rows whose `timestamp_utc` (converted to UTC) fall in the same clock-hour bucket (date + hour, minutes/seconds dropped). Counted by distinct buckets, not by rows.
- **Gap:** two chronologically adjacent rows (sorted by UTC timestamp) more than 90 minutes apart.
- `today_*` values in the CSV are samples of an in-progress day, not per-hour amounts. Downstream 8pm-window math in the pipeline uses the *latest* row at or before an instant, so a duplicated hour does not double-count earnings; the later sample supersedes the earlier one for the same in-progress day.

## Duplicated clock-hours — 13 found

| # | Clock-hour (UTC) | Rows (file order) | Timestamps (UTC) | today_total_usd values | Type |
|---|---|---|---|---|---|
| 1 | 2026-09-29 06:00Z | 1, 2 | 2026-09-29T06:26:58Z; 2026-09-29T06:42:27Z | 3.27; 11.28 | differing (in-progress day, later sample higher) |
| 2 | 2026-09-29 09:00Z | 5, 6, 7, 8 | 2026-09-29T09:00:12Z; 2026-09-29T09:31:25Z; 2026-09-29T09:39:17Z; 2026-09-29T09:47:53Z | 13.49; 13.82; 14.01; 14.23 | differing (4 rows in one hour, in-progress day) |
| 3 | 2026-09-29 10:00Z | 9, 10 | 2026-09-29T10:06:57Z; 2026-09-29T10:58:54Z | 14.64; 15.32 | differing |
| 4 | 2026-09-29 11:00Z | 11, 12 | 2026-09-29T11:50:15Z; 2026-09-29T11:58:47Z | 16.23; 16.29 | differing |
| 5 | 2026-09-29 21:00Z | 22, 23 | 2026-09-29T21:20:19Z; 2026-09-29T21:58:56Z | 30.69; 31.46 | differing |
| 6 | 2026-09-29 23:00Z | 25, 26 | 2026-09-29T23:50:28Z; 2026-09-29T23:58:52Z | 33.97; 34.14 | differing |
| 7 | 2026-10-01 01:00Z | 51, 52 | 2026-10-01T01:02:13Z; 2026-10-01T01:59:10Z | 0.89; 1.53 | differing |
| 8 | 2026-10-02 04:00Z | 78, 79 | 2026-10-02T04:00:15Z; 2026-10-02T04:59:01Z | 0.0; 0.0 | identical (zero day) |
| 9 | 2026-10-02 14:00Z | 88, 89 | 2026-10-02T14:00:46Z; 2026-10-02T14:59:34Z | 0.0; 0.0 | identical (zero day) |
| 10 | 2026-10-02 16:00Z | 90, 91 | 2026-10-02T16:00:02Z; 2026-10-02T16:59:09Z | 0.0; 0.0 | identical (zero day) |
| 11 | 2026-10-02 18:00Z | 92, 93 | 2026-10-02T18:00:22Z; 2026-10-02T18:59:33Z | 0.0; 0.0 | identical (zero day) |
| 12 | 2026-10-02 21:00Z | 95, 96 | 2026-10-02T21:00:18Z; 2026-10-02T21:59:12Z | 0.0; 0.0 | identical (zero day) |
| 13 | 2026-10-14 15:00Z | 182, 183 | 2026-10-14T15:09:13Z; 2026-10-14T15:55:37Z | 16.97; 18.28 | differing |

Notes: the Sep 29 duplicates date from the pipeline's first day (extra manual/bootstrap captures alongside the hourly ones, and early rows stored with `-04:00` offsets — the raw `timestamp_utc` strings in rows 1–26 mix offset formats; all were converted to UTC for this analysis). The Oct 2 duplicates are a temporary twice-an-hour cadence (rows at ~HH:00 and ~HH:59) on a day the workers earned $0. None of the 13 were deleted.

## Gaps over 90 minutes — 5 found

| # | Gap start (UTC, row) | Gap end (UTC, row) | Duration | Cause / note |
|---|---|---|---|---|
| 1 | 2026-10-02T23:59:32Z (row 98) | 2026-10-04T23:46:17Z (row 99) | 2,866.7 min (47.78 h) | Operator-known: both workers were idle/offline Oct 2–4 (last jobs Oct 1; back online Oct 4 ~22:40Z). The companion daily file shows 0 units for Oct 2 and Oct 3, so no material earnings went unrecorded by this gap. |
| 2 | 2026-10-06T08:45:13Z (row 132) | 2026-10-12T04:45:19Z (row 133) | 8,400.1 min (140.00 h) | Operator-known: all monitoring/earnings routines were deliberately paused by the operator on Oct 6 and resumed Oct 12. Earnings for the missing days are recovered in the companion daily file from Sogni's public daily chart. |
| 3 | 2026-10-12T04:45:19Z (row 133) | 2026-10-12T09:45:30Z (row 134) | 300.2 min (5.00 h) | Resume day (see gap 2). No separate cause documented for this specific interval. |
| 4 | 2026-10-12T14:30:29Z (row 139) | 2026-10-12T17:48:54Z (row 140) | 198.4 min (3.31 h) | Resume day (see gap 2). No separate cause documented for this specific interval. |
| 5 | 2026-10-14T00:45:52Z (row 171) | 2026-10-14T04:39:51Z (row 172) | 234.0 min (3.90 h) | Operator-known: coincides with the full monitoring pause ordered the evening of Oct 13 (Toronto) and the resume at ~04:38Z on Oct 14. |

Causes are labelled operator-known where they come from the operator's own record; gaps 3 and 4 are stated plainly as undocumented rather than given an invented reason.

## About the companion file (daily-income-oct-2026.csv) — methodology

- **What it is:** one row per NFT (462, 463, 478) per UTC day, Oct 1–22, 2026, plus one COMBINED row per day (88 data rows). The COMBINED row is the sum of that day's three per-NFT rows in every column. **Do not sum COMBINED rows together with per-NFT rows — that double-counts.** Month-to-date totals are the sum of the 22 COMBINED rows (equivalently, the sum of all 66 per-NFT rows).
- **PAYG (`payg_usd`):** measured from Sogni's public daily chart endpoint (`/v1/analytics/chart/daily/events/query`, no login), using the dashboard's own math: gross render USD value adjusted to the cash (non-subscription) share, × 51% worker share.
- **Units (`units`):** subscription render spark for that NFT that day, from the same public chart.
- **Subscription (`subscription_usd`) — ESTIMATE, not actuals:** `units × rate_used`, where `rate_used` is ONE projected October rate applied to all 22 days: **0.0004915358 USD per unit**, taken from the earnings pipeline's fetch snapshot sampled at **2026-10-23T03:44:00.000Z** (projected rate = full-month pool ÷ projected full-month network units, per Uzi's established pool-rate method). The rate's source endpoint requires account authentication, so — unlike PAYG and units — the rate is not independently reproducible from public data; its inputs are not published here because this repository is public. Subscription earnings are only finalized by Sogni ~45 days after month-end; treat this column as the current best estimate, expected to move a little at finalization (the finalized August 2026 subscription came in ~12% under its in-month estimate).
- **CAD (`total_cad`, `fx`):** one FX rate applied to all rows: **1.401351** CAD per USD (USD→CAD rate carried in the same pipeline fetch snapshot, source open.er-api.com). Each row's `total_cad` = its `total_usd` × fx, rounded to cents; each COMBINED row's `total_cad` is the sum of its three per-NFT rows' CAD values.
- **Zeros vs blanks:** Oct 2 and Oct 3 are genuine fetched zeros (workers idle) and are written as `0.00`, not blank. A blank numeric field would mean "could not be fetched". **There are no blanks in this file — every day Oct 1–22 was fetched for all three NFTs.**
- **`source` column:** `sogni_public_daily_chart` on per-NFT rows (PAYG + units measured; subscription derived as above); `sum_of_per_nft_rows` on COMBINED rows.
- **`fetched_at_utc`:** 2026-10-23T04:38:46Z — one fetch time for all rows.
- The result was **not** tuned to any expected figure. The computed Oct 1–22 total is reported as computed; any difference from an expected check figure is rate movement, and the delta is stated in the commit report to the operator.
