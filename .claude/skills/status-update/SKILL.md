---
name: status-update
description: Update the Fixlog status page (data/status.yaml) with verified service health facts or incidents. Use when Sassi asks to log an incident, mark a service degraded or back up, or refresh the status page.
---

# Status page update

`data/status.yaml` drives `/status/`. It is a public record, so it holds **verified facts only**: what happened, impact, status, fix.

## Rules

- **Nothing unverified.** Every field must come from something checked: a monitor, a log line, a status code, a message from Sassi, a commit. If it can't be verified, leave the field out.
- **No guessed causes.** Leave `cause_confirmed: false` (renders "Not confirmed yet") until the cause is actually confirmed. Only set `cause` with `cause_confirmed: false` if the text says it's under investigation.
- **Never include** internal hostnames, IPs, server names, ports, credentials, tokens, or customer data. Name services by their public name (e.g. "Propria.be").
- **Don't touch production.** This skill edits a YAML file. It doesn't restart, deploy, or probe anything beyond what Sassi asks.
- Remove `sample: true` (and the sample entries) the first time real data goes in, and tell Sassi.

## Schema

```yaml
updated: "YYYY-MM-DD"             # date the facts were last verified
window: "30 days"                 # label for the history bars
services:
  - name: "Public service name"
    url: "https://public.url"     # optional
    description: "One line"
    state: operational            # operational | degraded | outage
    probe: "HTTP GET /health"     # optional, how it's checked
    uptime: "99.9%"               # optional, only from a real monitor
    history: [operational, ...]   # optional, one per day, oldest first; none = no data
    note: "Short public note"     # optional
incidents:
  - id: "INC-YYYYMMDD-short"
    date: "YYYY-MM-DD"
    service: "Public service name"
    title: "What happened, plainly"
    status: investigating         # investigating | monitoring | resolved
    duration: "12m"               # optional, only if measured
    impact: "What users saw"
    cause: "Confirmed cause"      # optional
    cause_confirmed: false
    fix: "What was done"          # optional until there is one
    evidence: "Where the facts come from (log, monitor, commit)"
```

## Steps

1. Ask for (or read) the evidence. Write down each fact next to its source.
2. Edit `data/status.yaml`: update the service `state`, add or update the incident, and set `updated`.
3. When an incident resolves, keep it and flip `status: resolved`. Add `fix` and, if confirmed, `cause` with `cause_confirmed: true`.
4. Run `hugo server -D` and check `/status/`. The headline is computed from the service states.
5. Report to Sassi: what changed, the source for each fact, and any field you left out because it wasn't verified. Commit only if asked.
