# Travel Planner Skill Evaluation

This is a manual comparison of the three prompts in `evals/evals.json`. Scores check only the listed assertions; they do not establish the factual accuracy of unverified prices, opening hours, or transit times.

| Case | With skill | Baseline | Finding |
|---|---:|---:|---|
| Kyoto walking, meals, and budget | 4/4 | 3/4 | Both cover three days and fit the meal budget. The skill output clearly separates transfers; the baseline combines a JR and bus transfer in one row. |
| Singapore arrival, lodging, and flight day | 4/4 | 3/4 | Both cover nature, landmarks, lodging, baggage, and costs. The skill output distinguishes airport arrival from check-in and gate timing; the baseline relies on an unexplained three-hour airport target. |
| Paris review with no itinerary attached | 3/3 | 3/3 | Both ask for the missing itinerary and explain review scope. The skill response also preserves the user's scenic-detour and no-shopping priorities. |
| **Total** | **11/11** | **9/11** | **Two assertion gains across 11 checks.** |

Qualitative review: the skill outputs are more explicit about assumptions, uncertainty, route timing, bag handling, fallback options, and budget scope. The Kyoto test exposed that restaurant specificity still depends on live research being available; the skill now explicitly requires naming a searchable branch or labeling it a candidate with a backup. The Singapore test also supports the route-specific airport reasoning rule. The Paris case is a useful guard against inventing findings when source material is missing.

Limits: one run per prompt, manually graded; no repeat-run variance or tool/token timing was captured. Current operational facts in the sample answers were not independently fact-checked as part of this skill-format evaluation.
