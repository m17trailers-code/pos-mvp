# queue/ — drafts waiting for the owner

One folder per video: `YYYY-MM-DD_kebab-slug/` (date = intended posting date).

| File | Contents |
|---|---|
| `script.md` | premise, hook, timing sheet (time range · visual · on-screen text · sound · purpose), ending, SFX list |
| `shots.md` | one entry per Higgsfield generation: image prompt, motion prompt, duration, aspect 9:16, covers, avoid |
| `caption.md` | 3 caption options, hashtags, cover text, best posting window |
| `status.md` | first line `DRAFT` / `APPROVED` / `POSTED`, then compliance flags, assumptions, owner notes, review log |

Lifecycle (all by the owner's hand):
1. Agent writes the folder with `DRAFT`.
2. Owner edits, then `scripts/studio approve <slug>` → `APPROVED`.
3. Owner generates in Higgsfield, edits, posts in the TikTok app.
4. `scripts/studio posted <slug>` → `POSTED`, folder moves to `posted/`, `stats.md` template created.
