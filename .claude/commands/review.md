# /review <queue folder> — editorial and compliance pass on a draft

**Input:** a queue slug, e.g. `2026-09-28_doorbell-3am`.
**Output:** fixes written directly into the draft's `script.md`, `shots.md`,
`caption.md`; a `## Review YYYY-MM-DD` section appended to `status.md`
listing what changed and what still needs the owner.
**Destination:** that one `queue/` folder only. Never posts, never moves files.

## Procedure

1. Read `CLAUDE.md`, `knowledge/platform-rules.md`, `hooks.md`, `formats.md`,
   `voice.md`, `kpi.md`, then all four files in the folder.
2. If `status.md` says `APPROVED` or `POSTED`, stop and say so. Only `DRAFT`
   gets edited.
3. Check, in this order, and fix in place:
   1. **Compliance.** Real gore, self-harm, minors in danger, real likeness,
      copyrighted IP, claims of a real event. Anything borderline goes under
      `## Compliance flags` in `status.md` with the exact line quoted.
   2. **Disclosure.** Product or brand mentioned → `#ad` / "commission earned"
      present in every caption option.
   3. **Length.** Timing sheet total matches the length band. A `long` must
      total ≥ 65s. Sum the rows; do not trust the header.
   4. **Scare placement.** Main scare between 55% and 75% of runtime. Not in
      the first 3s. Not telegraphed by text, caption, or cover.
   5. **Hook strength.** Score with the rubric. Below 18/25 → rewrite the hook
      and note the old one in the review section.
   6. **Pacing.** Any block > 10s with no change in image, text, or sound →
      split it or add a beat. Last 20% has at least one reveal or line.
   7. **Shots.** Every timing row is covered by a shot. Every shot has image
      prompt, motion prompt, duration, aspect, avoid-list. Durations sum to at
      least the runtime. Prompts do not ask the model for legible text, hands
      close-up, or a recognisable face unless `Avoid` explains how.
   8. **Caption.** Three options, distinct registers, 5–8 hashtags, cover text
      ≤ 5 words, posting window present.
   9. **Voice.** Matches `knowledge/voice.md`. If voice.md is empty, say so.
4. Append to `status.md`:
   ```
   ## Review YYYY-MM-DD
   - Changed: ...
   - Still needs owner: ...
   - Verdict: READY FOR OWNER / NEEDS REWRITE
   ```
   Leave the first line of `status.md` as `DRAFT`.
5. Print the self-check block. KPI served: name the one the fixes protect.
