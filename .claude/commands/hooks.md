# /hooks <topic> — 10 scored hooks for a topic or format

**Input:** a topic ("abandoned pool"), a format ("found footage"), or a queue
slug to generate alternates for.
**Output:** `research/hooks/YYYY-MM-DD_topic.md` with 10 hooks, each scored.
Printed in the session as well.
**Destination:** `research/hooks/` only. Winners are copied into
`knowledge/hooks.md` by the owner, or by `/scorecard` once they have data.

## Procedure

1. Read `CLAUDE.md`, `knowledge/hooks.md` (patterns + rubric), `voice.md`,
   `formats.md`, `audience.md`.
2. Generate 10 hooks. Each hook is three lines:
   - **Visual** (first 2 seconds, one static or slow shot, describable to Higgsfield)
   - **On-screen text** (≤ 8 words, no "wait for it", no "jump scare", no emoji spam)
   - **First sound** (spoken line, ambient, or silence)
   Vary the pattern: at least 3 question-based, 3 statement-based, 2 with a
   specific time or number, 2 that give an instruction to the viewer
   ("look at the second window").
3. Score each 1–5 on the five rubric lines in `knowledge/hooks.md` and total
   out of 25. Sort by total. One sentence of "why" per hook.
4. Flag any hook that implies a real event, real place incident, or real
   person. Rewrite or drop it.
5. Save the file with a header: topic, date, which format(s) it suits, which
   length band the top 3 fit.
6. Print the self-check block. KPI served: 3s retention.
