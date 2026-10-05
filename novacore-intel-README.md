# Novacore Intel — business-intelligence data pack

Companion files to `hourly-income.csv` in this private repo. Built by
`~/workspace/tools/novacore-intel/assemble.py`. Read-only against all
sources; nothing here touches novacoreai.ca, Netlify, or site files, and
`hourly-income.csv` itself is never modified.

## Files

### hourly-hardware.csv
Per-rig hourly rollups from the 10-minute sensor log
(`gpu-temps-YYYY-MM-DD.log`). Columns:

| column | meaning |
|---|---|
| timestamp_utc / timestamp_toronto | hour bucket start |
| rig / nft | x870 (#462) or x570 (#463) |
| samples | 10-min samples in the hour |
| gpu_avg_c / gpu_max_c | GPU temp avg / max (°C) |
| gpu_avg_util_pct | mean GPU utilization |
| gpu_avg_power_w | mean board power (RTX 5090 TDP 575W) |
| fan_avg_pct | mean fan duty cycle |
| cpu_max_c | CPU (k10temp) max; warm ≥85°C (Ryzen TjMax 95) |
| ddr_max_c | DDR5 DIMM max; blank for x570 (DDR4, no DIMM sensors) |
| nvme_max_c | NVMe composite max; warm ≥65°C |
| ram_max_used_pct | blank — the temp log lines carry no RAM figures |
| pct_time_gpu_warm / pct_time_cpu_warm | % of samples ≥80°C / ≥85°C |

### business-probabilities.csv
TypeSafe Noul (Jev) probability assessments, one row per question, grounded
in the assembled data. Columns: timestamp_utc, question, probability_0_1,
basis_summary, key_inputs. Questions cover: October finishing within ±15% of
the pace forecast; a watchdog anomaly flag in 24h; a worker silent stall in
7 days; a GPU thermal-throttle event in 7 days; September payout within ±10%
of estimate; SOGNI ±20% in 30 days (+ directional USD-earnings impact note).

### hardware-risk.csv
TypeSafe Noul wear-and-tear failure probabilities per component per rig over
30/90/365-day horizons, grounded in deterministic thermal signals computed
first: time-above-threshold, >10°C thermal-swing count, fan duty-cycle
averages, sustained power vs 575W TDP. Columns: timestamp_utc, component,
rig, nft, age_months, hours_observed, pct_time_above_warm, thermal_cycles,
risk_30d, risk_90d, risk_365d, confidence_0_1, notes.

**Honesty rule:** rigs are ~2 months old (ops began Aug 2026) and the thermal
baseline is only ~4 hours (tracker started 2026-10-04). confidence_0_1 is
0.25 by rule for every hardware-risk row, and notes say the baseline is
thin. x570 DDR risk is unobservable (DDR4 has no DIMM sensors) — those rows
are prior-only. PSU risk is inferred (no PSU sensors) from GPU power draw.

## Caveats
- The sensor history starts 2026-10-04 ~19:38 EDT; anything "thermal" before
  that is unobserved. 3 transient `nvidia-smi rc=1` probe failures are
  monitoring gaps, not hardware faults.
- `hourly-income.csv`'s `month_usd`/`month_units` columns track the
  provisional *subscription* month (September final), not October MTD —
  October MTD lives in the forecast document.
- SOGNI probability has no price history behind it (single spot snapshot +
  24h change); it leans on generic small-cap volatility priors.
- Probabilities are decision aids, not predictions; re-run the assembler for
  a fresh assessment as new data accumulates.
