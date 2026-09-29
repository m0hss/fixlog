# Fixlog

Sassi's personal, unofficial dev log. Hugo (extended, 0.146+), custom theme in `themes/fixlog/`.

## Run

```bash
hugo server -D        # http://localhost:1313
hugo --gc --minify    # production build to public/
hugo new posts/<slug>.md
```

## Writing posts

- First person as Sassi. Concise, honest, a little playful. Failures stay in.
- Shape: title, one-line hook (`summary`), then `## Context`, `## What I tried`, `## What happened`, `## Takeaway`, `## Next steps`. The archetype scaffolds this.
- Every claim needs a source (issue, commit, log, test output). List them in `sources:` front matter. Mark anything inferred as inferred.
- Never invent numbers. `metrics`, `facts`, and `snippet` front matter must come from a real run.
- Never publish secrets, credentials, customer data, or internal hostnames.
- Fixlog is not FixByte marketing and makes no claims on FixByte's behalf.

Front matter the theme reads: `outcome` (worked | failed | in-progress | poking), `tags`, `summary`, optional `entry` (override the auto entry number), `metrics` (list of label/value/note), `snippet` (file/code/tag), `note` (label/text), `facts` (label/value, post sidebar), `sources` (kind/ref/url/note).

Markdown extras: `> quote` renders as the "Core lesson" callout, `- [ ]` task lists render as the next-steps checklist, fenced code takes `{file="path"}` for the window header.

## Status page

`data/status.yaml` drives `/status/`. Verified facts only: what happened, impact, status, fix. Leave `cause_confirmed: false` until the cause is actually confirmed. Remove `sample: true` once real data is in.

## Design

`design/DESIGN.md` is the source of truth (from the Google Stitch export). Tokens live at the top of `themes/fixlog/assets/css/main.css`. The full Stitch export sits untracked in `stitch_fixlog_developer_lab_notebook/`. Its sample numbers are mockup filler, not facts.

## Skills

Project skills live in `.claude/skills/`:

- `issue-to-post`: turn a GitHub issue (plus commits, logs, test output) into a draft post with sources. Always `draft: true`.
- `status-update`: update `data/status.yaml` with verified facts only. No guessed causes, no internal hostnames or secrets.

Use them instead of improvising for those tasks.

## Gotchas

- Don't run `hugo --gc` (or a second build) while `hugo server` is running. It prunes `resources/_gen`, and the running server keeps serving CSS links that now 404, so the page shows as unstyled HTML. Restart the server if that happens.

## Workflow

Drafts are for Sassi to review. Don't publish, deploy, or post externally unless Sassi asks.
