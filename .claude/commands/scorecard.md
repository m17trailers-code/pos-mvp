# /scorecard — rewrite reports/weekly-scorecard.md (Sunday)

**Input:** `scripts/studio stats YYYY-WW` for the closing week and the week
before, `plans/YYYY-WW.md` (what was planned vs posted), `knowledge/kpi.md`
targets, `knowledge/formats.md`.
**Output:** `reports/weekly-scorecard.md`, overwritten weekly. Also allowed:
update the **Current** column in `knowledge/kpi.md`, add evidence lines under
formats in `knowledge/formats.md`, and promote hooks with ≥ 75% 3s retention
into the patterns list in `knowledge/hooks.md`.
**Destination:** `reports/`, `knowledge/kpi.md`, `knowledge/formats.md`,
`knowledge/hooks.md`.

## Procedure

1. Read `CLAUDE.md` and the inputs. Run `studio stats` for both weeks.
2. Write the scorecard with these sections:
   1. **KPI table** — every row of `knowledge/kpi.md`: target, this week,
      last week, arrow. Medians for rates, sums for counts.
   2. **Plan vs posted** — 7 planned slots, which were posted, which slipped,
      long-video count (target ≥ 3).
   3. **Experiment result** — the week's single experiment: metric split
      between arms, sample sizes, a verdict (`adopt` / `repeat` / `drop`).
      With fewer than 3 videos per arm, say "repeat".
   4. **Double down** — formats or hook patterns above target on follows/1K
      and 3s retention, with the numbers.
   5. **Kill** — formats or patterns below target two weeks running, with the
      numbers. Anything that touched a compliance line goes here regardless.
   6. **Next week's experiment** — one variable, with the hypothesis in one
      sentence, to hand to `/plan-week`.
3. Update the knowledge files listed above. Keep each change to one line per
   fact.
4. Print the self-check block. KPI served: the ones the table moved.
