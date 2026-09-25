# M17 Studio

A one-person AI social-media team for the TikTok horror channel M17
(@m17515588). It plans, researches, writes scripts and Higgsfield shot lists,
drafts captions and reads analytics. It never posts, comments, follows or logs
in to TikTok. Everything ends in an approval queue the owner acts on by hand.

Start with `CLAUDE.md`. Agents are Claude Code commands in `.claude/commands/`.

## Weekly loop
1. Monday: `/research-week` → `/plan-week`
2. Daily: `/write-script <slot>` → edit the `queue/` folder → set `status.md` to `APPROVED`
3. Generate in Higgsfield from `shots.md`, edit, post by hand using `caption.md`
4. Move to `posted/`, drop stats in `inbox/`, then `/ingest-analytics` → `/brief`
5. Sunday: `/scorecard`

## Build phases
- Phase 1: brain, channel config, knowledge templates, `/intake` — done
- Phase 2: `/write-script`, `/hooks`, `/review`, queue format, `scripts/studio` — done
- Phase 3: `/research-week`, `/plan-week`, competitors, first weekly plan — done
- Phase 4: `/ingest-analytics`, `/brief`, `/scorecard`, `studio.db` — done

Requirements: Python 3.11+, no network, no paid services.
