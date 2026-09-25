# /intake — fill the knowledge layer from the owner's answers

**Input:** the owner's answers to 12 questions, either interactively in this
session or already written in `inbox/intake-answers.md`.
**Output:** filled `knowledge/voice.md`, `formats.md`, `hooks.md`,
`audience.md`, `offer.md`, `competitors.md`, plus updates to
`channels/m17.yaml` (timezone, cadence, posting windows, follower count).
**Destination:** `knowledge/`, `channels/`. Nothing else.

## Procedure

1. Read `CLAUDE.md`, `channels/m17.yaml` and every file in `knowledge/`.
2. If `inbox/intake-answers.md` exists, read it and skip any question it
   already answers. Otherwise ask the questions below **one at a time**, in
   order, in plain language. Accept short, messy answers; ask one follow-up
   only when an answer is too vague to write from.
3. After the last answer, rewrite the knowledge files. Keep the existing
   headings. Replace placeholder comments with the owner's material, in the
   owner's words where possible. Where an answer is missing, leave the heading
   with a single line `TODO: not answered in intake` so it is visible.
4. Update `channels/m17.yaml` only for fields the answers cover.
5. Print a short summary: which files changed, and the three biggest gaps
   still open in the knowledge layer.
6. Print the self-check block from `CLAUDE.md`.

## The 12 questions

1. **Voice.** Describe M17 in one sentence as if telling a stranger. Then: is
   there narration, on-screen text only, or both? Any words or phrases the
   channel always uses, and any it must never use?
2. **Best three videos.** For each: what happened in the first 3 seconds, how
   long it was, what the scare was and where it landed, and the rough numbers
   (views, follows, saves) if known.
3. **Worst three flops.** Same breakdown, plus your own theory of why.
4. **Formats.** Which of found footage / jump scare / creepy POV / "what's in
   the room" have you actually posted? Any recipe you follow every time
   (camera style, lighting, ending)?
5. **Audience comments.** Paste or paraphrase 10–20 real comments. Which
   phrases repeat? What do people ask for more of? What do they complain about?
6. **Audience data.** From TikTok analytics: top countries, age bands, gender
   split, and the hours your followers are most active. Time zone you post in.
7. **Posting rhythm.** How many videos per day can you realistically produce
   and post? Which days are hardest? Preferred posting times so far?
8. **Higgsfield workflow.** Which models or presets you use, typical clip
   length per generation, how many clips make one video, and what the model
   does badly (faces, hands, text, motion) so shot lists avoid it.
9. **Products.** Any products you could plausibly promote in a horror context
   (props, lights, cameras, merch, apps, books)? Any brands that have already
   reached out? Status of the TikTok Shop appeal.
10. **Competitors.** 8–10 horror accounts you watch. For each, one line on what
    they do that you wish you did.
11. **Red lines.** Beyond the hard rules in CLAUDE.md, anything you personally
    will not make (themes, religious imagery, animals, specific settings)?
12. **Constraints and goals.** Hours per week you can give this, budget for
    tools, and the date you want 10K followers by.

## Self-check (print before finishing)

- Touched TikTok? NO — this command only reads answers and writes Markdown.
- Suggested any fake engagement? NO.
- Compliance flags raised from the owner's red lines? Listed in
  `knowledge/platform-rules.md` under "Our lines" if new.
- Wrote only to `knowledge/` and `channels/`.
- KPI served: all of them — this is the input every other agent depends on.
