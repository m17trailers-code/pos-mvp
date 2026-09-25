# /ingest-analytics — load TikTok analytics into studio.db and posted/*/stats.md

**Input:** a TikTok analytics CSV export in `inbox/`, or screenshot text the
owner typed into an `inbox/*.md` file.
**Output:** rows in `studio.db` (tables `videos`, `stats`), refreshed
`posted/<slug>/stats.md` for matched videos, and a short console summary.
**Destination:** `studio.db`, `posted/`. Nothing else.

## Procedure

1. Read `CLAUDE.md`. List `inbox/` and pick the newest analytics file(s) the
   owner named, or ask which one if several are new.
2. **CSV:** run `scripts/studio ingest inbox/<file>.csv`. It maps common
   TikTok export headers (Video title, Post time, Video views, Likes, Comments,
   Shares, Favorites, New followers, Average watch time, Watched full video)
   and the owner's optional extra columns (`Format`, `Length`, `Hook text`,
   `3s retention`, `50% retention`, `slug`). If it dies on a header, show the
   owner the header row and ask which column is which; do not guess.
3. **Screenshot text:** build a small CSV in `inbox/` with the same headers
   from the numbers the owner typed, then run the same command. Never try to
   read pixels you cannot see; ask for the numbers.
4. Run `scripts/studio stats` (last 7 days) and paste the table into the
   session so the owner sees what landed.
5. For videos that did not match a `posted/` folder, tell the owner which
   folder name to add so next ingest links them (title must contain the slug
   tail, or add a `slug` column).
6. Print the self-check block. KPI served: all — this feeds every number.

## Never
- Log in to TikTok or fetch analytics yourself. Exports come from the owner.
- Edit `script.md`, `caption.md`, or anything in `queue/`.
