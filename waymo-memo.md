# BRIEFING MEMO — Verifying Waymo's "82% Fewer Injury Crashes" Claim

To: City Council Member | From: Teja Piepur Chakravarthi, M.S. Computer Science, University of North Texas | Date: November 22, 2026 | Re: Can you repeat Waymo's headline safety claim? — Yes, but only with the method attached.

## BOTTOM LINE — VERDICT: DEPENDS ON THE METHOD

The claim checks out in direction in every version of the calculation, but its size moves 14 points depending on two choices in the human benchmark. Quote 82% only together with how it was built (see Recommended wording).

## RECOMMENDED WORDING

"Across 271.3 million rider-only miles through June 2026, Waymo recorded 82% fewer injury crashes per mile than the human benchmark — 0.67 vs. 3.77 per million miles — when the benchmark is adjusted for crashes humans don't report and matched to the streets Waymo drives. Without either adjustment, the gap is 69%."

## HOW THE CLAIM IS BUILT

A crash rate is crashes divided by miles driven, expressed per million miles (IPMM). Waymo's rate uses its rider-only crashes reported to NHTSA under the Standing General Order, regardless of fault. The human benchmark uses state police-reported crashes and vehicle miles traveled for passenger vehicles on the surface streets Waymo operates on (freeways excluded). Two adjustments matter: (1) a 32% underreporting correction, from NHTSA's Blincoe et al. (2023), for injury crashes humans never report; (2) a dynamic (spatial) benchmark, from Chen et al. (2024), that reweights the city-wide human rate to the streets Waymo actually drives (S2 areas), because not all streets are equally risky. Data: Waymo Safety Impact Data Hub, through June 2026; files "Collision count and comparisons to benchmarks" (1,804 rows) and "Geographic distribution of benchmark and Waymo RO miles" (19,032 rows).

## REBUILDING THE HEADLINE NUMBER

Claim row: Outcome "Any Injury," All Locations (mileage blended), All Crashes, benchmark "Any-injury-reported." Waymo: 183 injury crashes / 271.329 million miles = 0.674 per million miles. Human benchmark: 3.774 per million miles, i.e. 1,023.9 crashes would be expected at the human rate — 840.9 (about 841) fewer. Reduction: 1 − (0.674 / 3.774) = 82.1% fewer, 95% confidence interval 78.9% to 85.0% fewer.

## HOW SENSITIVE IS IT?

The same claim, four ways (Waymo rate 0.674 in all four; only the benchmark changes):

| Benchmark version | Benchmark IPMM | Fewer crashes | 95% range |
|---|---|---|---|
| Unreported crashes added + matched to Waymo's streets (headline) | 3.774 | 82.1% | 78.9–85.0% |
| Unreported crashes added, not matched | 3.136 | 78.5% | 74.6–81.9% |
| Observed crashes only + matched | 2.581 | 73.9% | 69.2–78.0% |
| Observed crashes only, not matched | 2.144 | 68.6% | 62.9–73.5% |

Adding the unreported crashes moves the claim more (+8.3 points with matching, +9.9 without) than street matching does (+3.6 and +5.3 points). Every version's interval excludes zero, so the direction is solid; the size is not — the four results sit 13.6 points apart, so this is not a "solid" 82%.

## TWO ASSUMPTION TESTS

(1) Unreported-crash estimate: benchmark with the correction divided by benchmark without it is 3.774 / 2.581 = 1.46 with street matching and 3.136 / 2.144 = 1.46 without — close to the 1.47 implied by a 32% correction (1 / 0.68), i.e. an implied unreported share of 31.6% vs. the stated 32%. The estimate reproduces. (2) Where Waymo drives (San Francisco, 134 S2 areas, 67.9 million Waymo miles): the human injury-crash rate is 2.77 per million miles across all areas, but 3.56 when each area is weighted by Waymo's miles — about 29% higher where Waymo actually drives. The five areas Waymo drives most have human rates of 2.97, 8.56, 4.15, 3.12 and 2.04 per million miles. An unweighted city average would understate the risk on Waymo's streets, which is why the dynamic benchmark raises the comparison.

## WHAT NOT TO SAY

Do not claim a fatal-crash reduction. Waymo recorded only 2 fatal crashes (0.007 per million miles). The unmatched version gives 73.1% fewer with a 95% range of −10.2% to 97.8% — it includes no difference, so "don't say it yet." The matched version gives 79.3% (15.4–98.3%), but with 2 crashes against 7.4–9.6 predicted, the data are too thin. Also do not generalize beyond the five operating areas (Phoenix, San Francisco Bay Area, Los Angeles, Austin, Atlanta) or to freeways, which the benchmark excludes.

Sources: Waymo Safety Impact Data Hub (waymo.com/safety/impact), data through June 2026, accessed November 22, 2026; methodology after Scanlon et al. (2024), Kusano et al. (2025), Chen et al. (2024), Blincoe et al. (2023). All figures recomputed from the downloaded CSVs; rounding only at the end.
