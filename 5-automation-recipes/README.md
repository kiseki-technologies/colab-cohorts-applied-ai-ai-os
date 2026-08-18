# Automation recipes

Nine automations. Each one gives you the cadence, the prompt, what good looks like, and the
first thing to change when it isn't good yet.

**Pick one. Get it running against your own data. Then pick another.**
A single automation you actually use beats five you planned.

| Recipe | Cadence | Needs |
|---|---|---|
| `pre-standup-brief.md` | Weekday mornings | Tracker + (ideally) meeting tool |
| `stakeholder-update-drafter.md` | Weekly | Tracker + meetings |
| `meeting-actions-router.md` | Triggered after calls | Meeting tool + tracker |
| `blocked-ticket-watcher.md` | Daily | Tracker |
| `feedback-themes-weekly.md` | Weekly | A feedback source |
| `sprint-health-warning.md` | Mid-sprint | Tracker |
| `pre-meeting-one-pager.md` | Triggered | Calendar + tracker + meetings |
| `prd-drift-checker.md` | Weekly | Tracker + docs |
| `competitor-watch.md` | Daily | Web only — no integrations needed |

**Start here if you're not sure:** `pre-standup-brief.md`. It needs one connector, it runs
tomorrow morning, and the "what you promised and never ticketed" line tends to justify itself
in the first week.

`_recipe-template.md` is for writing up your own — bring one to Week 4.

**`scheduling.md` is how you make any of these repeat** — Cowork scheduled tasks, Claude Code
routines, local scheduled tasks, and which one each recipe belongs in.

---

## How to run any of these

1. Copy the prompt, fill the `[BRACKETS]`
2. **Run it manually once**, in Cowork or Claude Code. Read the output. Fix the obvious
   problems.
3. Only then schedule it — `scheduling.md` covers the four ways, and which to pick
4. Read the first three unattended runs properly. Change one thing at a time.

Step 2 is the one people skip, and it's why their first automation disappoints them.

**Decide where the output lands before you schedule anything.** A recipe that says "write to
`standup-brief.md`" needs a folder to write to, and a cloud scheduled task does not have one
by default. `scheduling.md` explains the three honest options.
