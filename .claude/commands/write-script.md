# /write-script <slot or idea> — turn a plan slot or raw idea into a queue folder

**Input:** a slot from `plans/YYYY-WW.md` (e.g. `wed`, `slot 3`) or a raw idea in
plain words (e.g. "doorbell cam, 30s, jump scare").
**Output:** one folder `queue/YYYY-MM-DD_slug/` with `script.md`, `shots.md`,
`caption.md`, `status.md`. See `queue/README.md` for the exact format.
**Destination:** `queue/` only.

## Procedure

1. Read `CLAUDE.md`, `channels/m17.yaml`, `knowledge/voice.md`, `formats.md`,
   `hooks.md`, `audience.md`, `platform-rules.md`, `kpi.md`, `offer.md`.
   If a slot was given, read the current `plans/` file and the slot's goal.
2. Decide: format, length band (`short` 20–40s, `mid` 40–60s, `long` 65–90s),
   one-sentence premise, the single image the viewer will remember.
   If the plan says `long`, target 70–80s, never under 65s.
3. Write the **hook** first: opening visual, on-screen text (≤ 8 words), first
   sound. Score it with the rubric in `knowledge/hooks.md`; rewrite until every
   line scores ≥ 4 or note why not.
4. Build the **timing sheet** second by second in blocks of 2–10s:
   time range, what we see, on-screen text, sound/SFX cue, purpose of the beat.
   Place the main scare between 55% and 75% of runtime. Add a second smaller
   beat or reveal after it so the last 20% is not dead air. End on a line that
   makes a rewatch or a follow feel natural, no begging.
5. Write **shots.md**: one entry per generated clip. Each entry has
   `Image prompt`, `Motion prompt`, `Duration`, `Aspect: 9:16`, `Covers` (which
   timing rows) and `Avoid` (things the model does badly for this shot).
   Prompts describe the AI figure generically (pale, featureless, indistinct)
   and never name a real person, actor, or copyrighted character.
6. Write **caption.md**: three caption options in different registers
   (statement / question / recovered-footage log), 5–8 hashtags mixing broad
   and niche, cover text ≤ 5 words, best posting window from `channels/m17.yaml`.
   If any product or brand appears, add `#ad` or "commission earned".
7. Write **status.md**: first line `DRAFT`, then `## Compliance flags`,
   `## Assumptions` (anything you decided because a knowledge file was empty),
   `## Owner notes` (empty).
8. Run the `/review` checklist mentally on your own draft and fix the obvious
   before saving. Then print the self-check block from `CLAUDE.md`, naming the
   KPI this video targets (usually 3s retention + follows per 1K for short,
   full watch + Creator Rewards minutes for long).

## Never
- Write `APPROVED` or `POSTED`.
- Put the scare in the first 3 seconds or announce it in text.
- Depict real gore, self-harm, minors in danger, a real person, or an IP character.
- Suggest posting more shoppable videos than `platform-rules.md` allows.
