# scripts/

`studio` is a single stdlib-only Python file. Run it as `scripts/studio <cmd>`
or add `alias studio="$PWD/scripts/studio"` to your shell.

| Command | What it does |
|---|---|
| `studio list` | queue and posted folders with status |
| `studio approve <slug>` | sets `status.md` to `APPROVED` (owner only) |
| `studio posted <slug>` | sets `POSTED`, moves folder to `posted/`, creates `stats.md` |
| `studio ingest <file>` | Phase 4 |

`<slug>` can be the full folder name or just the part after the date.
Nothing here talks to TikTok or the network.
