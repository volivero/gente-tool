# Method notes for the tool

## Data in the tool
17 departments with published viable-area results (km² and share of departmental territory): 12 for
onshore wind, 10 for utility-scale solar. NCI and NGI for the same 17 departments (GENTE Deliverable 14,
Tables 17 and 22). Values in the tool reproduce the published INC and ING maps class by class.

## Placement modes
- Mode 0, interpretive layer: score = share / max share of the active technology.
- Mode 1, weighted criteria: score = (1 − w)·share_norm + w·[(1 − NCI) + NGI]/2, default w = 0.35.
- Mode 2, veto: excluded if NCI > cMax (default 0.08) or NGI < gMin (default 0.15). Survivors keep the
  baseline colour class; colour is not rescaled after exclusion.
- Mode 3, tiers: deploy if NCI ≤ tMid (0.10) and NGI ≥ 0.40; prepare if NCI > tMid + 0.15 or NGI < 0.28;
  conditional otherwise. With defaults: 3 / 5 / 4 departments for wind.

## Why gMin = 0.15
With cMax = 0.08, six of the twelve wind departments leave on conflict. The remaining six have NGI
0.118, 0.162, 0.211, 0.285, 0.420, 0.463: with a slider step of 0.05, each step between 0.10 and 0.30
excludes exactly one department. 0.15 keeps the criterion visibly active by default (Cesar leaves),
leaves five survivors, and keeps the whole ladder available for demonstration. 0.30 would leave two.

## Best–Worst Method as implemented
Best chosen first, rated against the others (2–9); then Worst, others rated against it (2–9); 1 reserved
for Best and Worst themselves; a_BW entered once and validated as the largest value. Weights from the
linear model. Consistency: input-based ratio CR_I = max_j |a_Bj·a_jW − a_BW| / (a_BW² − a_BW), against
the five-criteria thresholds of Liang, Brunelli & Rezaei (2020): 3: 0.1667, 4: 0.1898, 5: 0.2306,
6: 0.2643, 7: 0.2819, 8: 0.2958, 9: 0.3062. Ordinal consistency checked as the minimum requirement.

## Known limit
Weights do not recompute the ranking: per-criterion departmental scores do not exist. The ranking responds
to the placement of conflict and governance. Computing departmental means of each criterion layer from the
GENTE rasters (zonal statistics) would remove this limit; it is the natural next version.
