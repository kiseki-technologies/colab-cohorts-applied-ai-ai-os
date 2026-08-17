# Blocked ticket watcher

Small, unglamorous, and it stops things rotting quietly.

**Cadence:** daily, or Monday and Thursday
**Needs:** tracker

---

## The prompt

```
Every day at [09:00], using the Atlassian connector, find every issue in [PROJECT-KEY] that
has been blocked or flagged at risk for more than [3] days.

For each one:
- how long it's been blocked, and what the blocker is
- who owns unblocking it
- when it was last touched, and by whom
- a short, polite nudge message I could send that person, referencing the specific blocker

Write to blocked.md. If nothing has been blocked longer than the threshold, write the date and
"nothing stale." Do not include issues that are simply not started.
```

---

## What good looks like

The drafted nudge is the part that changes behaviour. Chasing is a tax on your attention and
your goodwill; having the message already written removes the friction that lets things sit.

## Tuning

- Threshold too low and you'll nag; start at 3 days and adjust.
- Add "ignore issues in the backlog — only active sprint" if it's noisy.
- Add "note if the same issue has appeared in this file more than twice" to catch the
  genuinely stuck ones.
