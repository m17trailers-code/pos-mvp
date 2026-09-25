# /research-week — turn the inbox into a weekly research note

**Input:** whatever the owner has put in `inbox/` since the last research note:
trend notes, competitor links with the owner's description, screenshots plus
the text the owner typed from them, pasted comment threads, analytics notes.
**Output:** `research/YYYY-WW.md` for the current ISO week.
**Destination:** `research/` only. Also allowed: append rows to
`knowledge/competitors.md` and `knowledge/audience.md` when the inbox contains
new facts about them (say so in the output).

## Never
- Scrape, browse, or log in to TikTok, or fetch competitor videos. Only the
  owner's pasted material counts. If the inbox is empty, say so and write a
  short note listing what the owner should drop in next time.

## Procedure

1. Read `CLAUDE.md`, `knowledge/formats.md`, `hooks.md`, `audience.md`,
   `competitors.md`, `kpi.md`, and the previous `research/` note if any.
2. Read every file in `inbox/` dated since the last note. Ignore `README.md`
   and `intake-answers.md`.
3. Write the note with exactly these sections:
   - **5 trends** — each: what it is, evidence from the inbox (quote or file
     name), how M17 could use it in our formats, risk (fad / compliance / off-voice).
   - **5 competitor hooks broken down** — each: account, what the first 3
     seconds showed (visual, text, sound), why it worked, what we would change
     to make it ours. Source is the owner's description, never a fetched video.
   - **10 audience questions** — real questions or repeated themes from
     comments, each with the format it suggests.
   - **Implications for the plan** — 3 to 5 bullets `/plan-week` should act on.
   - **Inbox handled** — list the files used so the owner can archive them.
4. Print the self-check block. KPI served: 3s retention (hooks) and
   comments per 1K (audience questions).
