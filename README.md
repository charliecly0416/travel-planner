# Travel Planner

A reusable agent skill for planning, researching, reviewing, and refining multi-day trips. It builds routes around booked transport, lodging, luggage, traveler preferences, budget, and current operating information.

## Contents

- `SKILL.md` — planning workflow and quality rules
- `references/output-template.md` — readable day-by-day itinerary structure
- `references/planning-checklist.md` — final route, booking, budget, and document audit
- `evals/evals.json` — representative test prompts
- `evals/evaluation.md` — first manual comparison against baseline responses

## Install for Codex

Copy this repository to `~/.agents/skills/travel-planner/`. The skill should be available the next time Codex loads its skills. To create a portable `.skill` archive, use the skill packaging utility or zip this directory while preserving the `SKILL.md` and `references/` structure.

## Evaluation

The initial manual evaluation scored 11/11 checks with the skill and 9/11 without it across three prompts. Each prompt was run once, so the results are an initial quality check rather than a repeatability benchmark.
