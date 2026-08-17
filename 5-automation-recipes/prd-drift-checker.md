# PRD drift checker (advanced)

Backlogs drift from specs quietly. This makes the drift visible before someone else finds it.

**Cadence:** weekly or fortnightly
**Needs:** tracker + your specs (Confluence, Notion, files)

---

## The prompt

```
Every [Friday], compare the backlog in [PROJECT-KEY] against the PRD at [PAGE/DOC].

Report:
- stories in the backlog that don't trace to anything in the PRD
- commitments in the PRD with no corresponding story
- anywhere the backlog has quietly changed what we said we'd build — quote both sides

This is hygiene, not a criticism of anyone. Be specific and cite issue keys and PRD sections.
If everything traces cleanly, say so in one line.

Write to prd-drift.md.
```

---

## What good looks like

Most weeks: "everything traces cleanly." The value is entirely in the weeks it doesn't —
usually the week before someone senior asks why you're building something nobody remembers
agreeing to.

## Why this one is advanced

It only works if your PRD is actually maintained. If your spec is six months stale, this
recipe will tell you that loudly — which is itself useful, if uncomfortable.
