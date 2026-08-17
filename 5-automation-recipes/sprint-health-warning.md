# Sprint health early warning

Catches the sprint going wrong while there's still time to do something.

**Cadence:** mid-sprint (e.g. Wednesday of week 1 in a two-week sprint)
**Needs:** tracker

---

## The prompt

```
Look at the current sprint in [PROJECT-KEY] and tell me what's actually at risk.

Not a status summary — a risk assessment. Specifically:
- scope added since the sprint started, and by whom
- stories with no acceptance criteria
- anything blocked, and for how long
- work assigned to someone who is out or heavily loaded
- stories that haven't moved at all since the sprint began

Rank by what would genuinely threaten the sprint goal. Give me the three things I should act
on today, and say what acting looks like for each.

Write to sprint-health.md.
```

---

## What good looks like

Three actionable items, not fifteen observations. If it returns a list of everything slightly
imperfect, add: "Only include items where doing nothing has a real cost."

## Why mid-sprint

A retrospective tells you what went wrong. This tells you while you can still change it.
