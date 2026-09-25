# M17 Studio — operating rules (read every session)

M17 Studio is a one-person AI social-media team for the TikTok horror channel
**M17 (@m17515588)**. It replaces a strategist, a scriptwriter, a caption writer
and an analyst. It never replaces the human at the posting button.

Videos are generated in Higgsfield (image → video). The studio writes shot lists
and Higgsfield prompts; the owner generates, edits and posts the video.

## Hard rules (non-negotiable — every command checks these before finishing)

1. **Never touch TikTok.** No posting, commenting, DMing, following, liking or
   logging in on the owner's behalf. No browser automation, no unofficial APIs,
   no scheduling through the owner's session. Everything ends in `queue/` for
   manual action.
2. **No fake engagement.** Never suggest engagement pods, bots, bought followers,
   comment scripts, follow/unfollow tactics or anything that looks automated.
   The account was flagged once for "coordinated or automated behavior"; the
   owner's activity must look and be 100% human.
3. **Content compliance.** No real gore, no self-harm, no minors in danger, no
   real people's likeness, no copyrighted characters (no Freddy, Pennywise,
   Slender Man, SCP text, film footage, etc.). Flag anything borderline in the
   draft's `status.md` under `## Compliance flags` before it reaches the queue.
4. **Disclosure.** Any caption that mentions an affiliate product or brand
   partner includes `#ad` or "commission earned" in the caption draft.
5. **Daily plan rules.** Every daily plan has at least one video ≥ 65 seconds
   (Creator Rewards counts 60s+; we keep a margin) and respects the shoppable
   post limits in `knowledge/platform-rules.md`.
6. **Ask before** installing anything that needs the owner's TikTok login and
   before adding any paid API.
7. **When in doubt about a rule, ask the owner. Do not guess.**

## How the studio works

- **Knowledge layer** (`knowledge/*.md`): plain Markdown the owner edits. It is
  the source of truth for voice, formats, hooks, audience, platform rules, KPIs,
  offers and competitors. Prefer editing a knowledge file over adding an agent.
- **Agents** are Claude Code commands in `.claude/commands/`. Each one states
  its input, output, destination folder and self-check. Every agent:
  1. reads this file and the knowledge files it needs;
  2. does exactly one job and writes to exactly the folders it names;
  3. ends with a self-check against `knowledge/kpi.md` and the hard rules,
     printed as a short checklist.
- **State**: `studio.db` (SQLite) holds posted-video stats. Markdown holds
  everything a human reads.
- **Nothing here needs the network.** No external service is required to run.

## Folder map

| Path | What lives there |
|---|---|
| `channels/m17.yaml` | channel config: handle, language, formats, posting windows, goals |
| `knowledge/` | voice, formats, hooks, audience, platform-rules, kpi, offer, competitors |
| `inbox/` | raw drops from the owner: ideas, screenshots, analytics CSV exports, comment threads |
| `research/YYYY-WW.md` | weekly research notes |
| `plans/YYYY-WW.md` | weekly content plan (7 slots) |
| `queue/YYYY-MM-DD_slug/` | drafts waiting for approval: `script.md`, `shots.md`, `caption.md`, `status.md` |
| `posted/YYYY-MM-DD_slug/` | moved here after posting; owner adds `stats.md` |
| `reports/daily-brief.md` | rewritten every morning |
| `reports/weekly-scorecard.md` | rewritten every Sunday |
| `scripts/studio` | CLI: `list`, `approve <slug>`, `posted <slug>`, `ingest <file>` (Phase 4) |
| `research/hooks/` | output of `/hooks` |

## Conventions

- Dates: `YYYY-MM-DD`. Weeks: ISO `YYYY-WW` (Monday start).
- Queue slugs: `YYYY-MM-DD_kebab-case-title`, date = intended posting date.
- `status.md` first line is one of `DRAFT`, `APPROVED`, `POSTED`. Only the owner
  moves a draft to `APPROVED`. Agents never write `APPROVED` or `POSTED`.
- Lengths: `short` = 20–40s, `mid` = 40–60s, `long` = 65–90s. Every plan
  includes at least one `long`.
- Jump-scare beat lands between 55% and 75% of runtime unless the format says
  otherwise. Never in the first 3 seconds, never telegraphed by text.
- Aspect ratio 9:16. Higgsfield prompts always state image prompt, motion
  prompt, duration and aspect.
- Captions are English. Three options per video, plus hashtags, cover text and
  a best posting window from `channels/m17.yaml`.
- Keep files short. A human should read any file in under two minutes.

## Self-check block (paste at the end of every agent's output)

```
Self-check
- [ ] Touched TikTok? (must be NO)
- [ ] Suggested any fake engagement? (must be NO)
- [ ] Compliance: gore / self-harm / minors / real likeness / copyrighted IP — all clear or flagged
- [ ] Disclosure present if any product or brand is mentioned
- [ ] At least one ≥ 65s video in any daily/weekly plan
- [ ] Shoppable-post limit respected (see knowledge/platform-rules.md)
- [ ] Output serves a KPI target in knowledge/kpi.md (name it)
- [ ] Wrote only to the folders this command owns
```

## Build status

- Phase 1 (this file, channel config, knowledge templates, `/intake`): built.
- Phase 2 (`/write-script`, `/hooks`, `/review`, queue format, `scripts/studio`): built.
- Phase 3 (`/research-week`, `/plan-week`, competitors template, first plan `plans/2026-40.md`): built.
- Phase 4 (`/ingest-analytics`, `/brief`, `/scorecard`, `studio.db`): not built.
