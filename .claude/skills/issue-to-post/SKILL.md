---
name: issue-to-post
description: Turn a GitHub issue (plus its linked commits, PRs, logs, or test output) into a draft Fixlog post in content/posts/. Use when Sassi asks to write up an issue, a fix, an experiment, or a failure as a post.
---

# Issue → draft Fixlog post

Output is always a **draft** (`draft: true`) for Sassi to review. Never publish, deploy, change `draft`, or post anywhere outside the repo.

## 1. Gather evidence

Read the issue and everything it links to. Use `gh` when the issue is on GitHub:

```bash
gh issue view <n> --repo <owner/repo> --comments
gh pr list --repo <owner/repo> --search "<n>" --state all
git log --oneline --grep "#<n>"
```

Collect: what the problem was, what was tried, what happened (with real output), and whether it ended up fixed. Note the URL or commit SHA for each fact. If a result is missing, don't fill it in. Leave a `TODO(Sassi): …` in the draft instead.

## 2. Pick the outcome

| outcome | when |
|---|---|
| `worked` | the fix landed and there is evidence it holds (test, log, merged PR) |
| `failed` | the approach was abandoned or didn't solve it |
| `in-progress` | still open or being fixed |
| `poking` | exploring with no conclusion yet |

If it's unclear, use `in-progress` and say why in the draft.

## 3. Write the file

`hugo new posts/<short-slug>.md`, then fill it in. Front matter:

```yaml
title: "<specific, plain title>"
date: <today>
draft: true
summary: "<one-line hook>"
tags: [<2–4 lowercase tags>]
outcome: "<worked|failed|in-progress|poking>"
sources:
  - kind: "issue"     # issue | pr | commit | log | test
    ref: "<owner/repo#n or short SHA or file name>"
    url: "<link, if any>"
    note: "<what it proves, optional>"
```

Optional, and only with real numbers from the evidence: `metrics`, `snippet`, `note`, `facts` (see CLAUDE.md).

Body, in this order: the one-line hook, then `## Context`, `## What I tried`, `## What happened`, `## Takeaway`, and optionally `## Next steps` as a `- [ ]` checklist. Put the takeaway's key line in a `>` blockquote.

## 4. Voice and rules

- First person as Sassi. Concise, honest, a little playful. Keep the dead ends.
- Every factual claim traces to a source in `sources`. When something is your inference, say so ("I think…", "inferred from the log, not confirmed").
- Real output goes in fenced code blocks with `{file="…"}` where it helps.
- Leave out secrets, tokens, customer data, internal hostnames, and private IPs. Redact them in logs.
- It's not FixByte marketing. Don't make claims on FixByte's behalf.

## 5. Check and hand off

Run `hugo server -D` and open the post to check it renders. Then tell Sassi the file path, the outcome you picked, and any `TODO(Sassi)` gaps.
