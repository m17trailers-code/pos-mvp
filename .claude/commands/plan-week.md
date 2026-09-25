# /plan-week — 7-slot content plan for the coming week

**Input:** the latest `research/YYYY-WW.md`, `posted/*/stats.md` (last 2–4
weeks), `reports/weekly-scorecard.md` if it exists, and the two knowledge
files that matter most: `formats.md` and `kpi.md`.
**Output:** `plans/YYYY-WW.md` for the next ISO week (Monday start).
**Destination:** `plans/` only.

## Procedure

1. Read `CLAUDE.md`, `channels/m17.yaml`, `knowledge/formats.md`, `hooks.md`,
   `kpi.md`, `offer.md`, `platform-rules.md`, the latest research note and
   the latest scorecard. If research is empty, plan from formats + stats and
   say so at the top.
2. Decide the week's **one experiment**: a single variable (hook pattern,
   length, ending style, posting hour, a new format). Everything else stays
   on proven ground so the experiment is readable in the scorecard.
3. Fill **7 slots**, one per day, each with:
   - day and date, posting window (from `channels/m17.yaml`)
   - format, length band and target seconds
   - hook angle in one line (visual + text idea)
   - goal per post: which KPI it is built to move
   - experiment flag: yes/no
   - shoppable: yes/no (only if `offer.md` has an approved product; count
     against the daily limit in `platform-rules.md`)
   - status: `idea` / `drafted (slug)` / `posted`
4. Rules the plan must satisfy, checked before saving:
   - at least **3 long** (≥ 65s) slots in the week, and every day's plan has
     at least one ≥ 65s option (a single slot per day means that slot must be
     the long one on ≥ 3 days; mark short days clearly as such and never two
     short days in a row without a long one between)
   - at most 1 experiment variable
   - no two identical hook patterns back to back
   - shoppable count ≤ daily limit; disclosure noted
   - nothing that violates the compliance lines
5. Add a **Production notes** section: which slots share a set or a base
   image so Higgsfield work can be batched, and which slot to draft first.
6. Print the self-check block. KPI served: follower delta / week and long
   videos posted / week.
