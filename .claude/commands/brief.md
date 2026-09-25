# /brief — rewrite reports/daily-brief.md (one page)

**Input:** `scripts/studio stats` (last 7 days) and `scripts/studio stats all`,
`queue/` state (`scripts/studio list`), the current `plans/YYYY-WW.md`,
`channels/m17.yaml` (follower count), `knowledge/kpi.md`, `knowledge/hooks.md`.
**Output:** `reports/daily-brief.md`, overwritten every morning.
**Destination:** `reports/` only, plus one allowed side effect: append the
day's best and worst hook rows to the hook log in `knowledge/hooks.md`.

## Procedure

1. Read `CLAUDE.md` and the inputs. Run the two `studio stats` commands and
   `studio list`.
2. Write the brief with exactly these headings, in this order, one page max:
   1. **What happened** — 3 bullets: yesterday's post (views, 3s, follows/1K)
      vs the 7-day median; anything unusual.
   2. **Best hook and why** — the video with the highest 3s retention among
      the last 7 days, with its hook text quoted, and one sentence on the
      mechanism (curiosity, instruction, number, place, time).
   3. **Worst hook and why** — lowest 3s retention or follows/1K, same
      treatment, plus a compliance note if the premise touched a red line.
   4. **Follower delta toward 10K** — current followers, gained last 7 days,
      remaining, weeks-to-10K at the current pace, and the follows/1K the
      channel would need to hit the target date in `channels/m17.yaml` goals.
   5. **What to post today** — the plan slot for today with its status; if
      not drafted, the exact `/write-script` command to run. Confirm a ≥ 65s
      video is in today's or tomorrow's plan.
   6. **3 fresh hooks** — three lines in the pattern that won yesterday,
      scored with the rubric.
   7. **One thing to fix** — a single, concrete, testable change for the next
      draft (a text line, a timing shift, an ending), not a list.
3. Update `channels/m17.yaml` → `status.followers` only if the owner gave a
   new number in `inbox/`.
4. Print the self-check block. KPI served: follower delta / week.
