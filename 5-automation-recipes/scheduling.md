# Making it repeat — scheduled tasks and routines

Every recipe in this folder says something like *"Every weekday at 08:00."* This page is how
that actually happens.

There are four ways to make Claude repeat work for you. They differ on three things that
matter, and the rest is detail:

- **Does it run when your laptop is shut?**
- **Can it reach the files in this folder?**
- **What does it need to be pointed at — your connectors, or a GitHub repo?**

---

## The four options

| | **Cowork scheduled task** | **Claude Code routine** | **Claude Code Desktop task** | **`/loop`** |
|---|---|---|---|---|
| Where it runs | Cloud | Cloud | Your machine | Your machine |
| Laptop can be shut | ✅ | ✅ | ❌ | ❌ |
| Reaches this folder | Only if you attach it — and then it runs locally | ❌ works from a fresh clone of a GitHub repo | ✅ | ✅ |
| Needs a GitHub repo | ❌ | ✅ | ❌ | ❌ |
| Your connectors | ✅ | ✅ | ✅ | ✅ |
| Asks permission mid-run | Per your approval mode | ❌ runs autonomously | ✅ configurable | ✅ inherits the session |
| The task itself survives a restart | ✅ | ✅ | ✅ | ❌ session-scoped, expires after 7 days |
| Fastest cadence | Hourly | Hourly | Every minute | Every minute |
| Plan | Any paid plan | Any paid plan, with Claude Code on the web | Any paid plan | Any paid plan |

**For almost everything in this kit, the answer is the first column.** The nine recipes read
your tools and write you something to read. That's exactly what a Cowork scheduled task is for,
and it's the only option that needs neither a terminal nor a repo.

---

## Option 1 — Cowork scheduled tasks *(start here)*

**Use it for:** the morning brief, the Friday update, weekly feedback themes, the blocked
ticket watcher. Anything that reads your connectors and produces prose.

1. In Cowork, click **Scheduled** in the sidebar, then **New task**
2. Choose **Create with Claude** — it asks you a few multiple-choice questions and writes the
   task — or **Set up manually** if you already have the prompt from a recipe here
3. Fill in the name, paste the prompt, pick an approval mode, and choose the frequency:
   hourly, daily, weekdays, weekly, or manual
4. Optionally attach a folder — read the warning below first
5. Save, then **run it once by hand** before you trust the schedule

Each run is its own Cowork session. Results appear on the **Scheduled** page, and you can read
past runs there. They run remotely, so they fire on time whether or not your machine is awake.

**The folder warning.** A scheduled task that needs local files runs locally — which means it
only fires when your machine is on and Claude Desktop is open. Attach the folder if the output
genuinely has to land in `my-system/`; leave it off if you'd rather the task ran reliably and
you copied the good outputs in yourself. See *Where the output lands* below.

## Option 2 — Claude Code routines *(cloud, repo-shaped)*

**Use it for:** anything that touches code or a repo. Nightly checks on your SnapLedger app,
a review of every PR you open, drift between your backlog and a spec that lives in git.

Create one at `claude.ai/code/routines`, in the Claude Code desktop app under **Routines →
New routine → Cloud**, or from the CLI:

```
/schedule every weeknight, check main for failing tests and open a PR with the fix
```

Claude asks about the schedule, the repositories and the prompt, then saves it to your
account. `/schedule list`, `/schedule update` and `/schedule run` manage them afterwards, and
you can ask things like *"why did my nightly review do nothing this morning?"*.

Three things to know before you rely on one:

- **It needs a GitHub repository.** Each run clones your repo fresh and starts from the
  default branch; changes come back as a `claude/`-prefixed branch you review. That's the
  whole model — cloud routines have no access to files on your machine.
- **It runs autonomously.** No permission prompts, and by default *every connector on your
  account is included*, writes and all. Remove the ones the routine doesn't need, and write
  the prompt so it drafts rather than acts. This is where "you approve, it operates" is
  easiest to lose by accident.
- **There's a daily cap** on how many routine runs start — currently 5 on Pro, 15 on Max, 25 on
  Team and Enterprise. One automation running weekday mornings costs you one a day. Your
  current allowance is shown at `claude.ai/code/routines`.

Triggers aren't only schedules. A routine can also fire on an API call or a GitHub event — the
PR-review-on-every-pull-request pattern is a routine with a GitHub trigger. Schedules are the
Week 3 use; the rest is there when you want it.

## Option 3 — Claude Code Desktop scheduled tasks *(local)*

**Use it for:** the case Options 1 and 2 can't cover — a scheduled run that must read and
write files in *this folder*, on your machine, with your local setup.

In the Claude Code desktop app: **Routines → New routine → Local**. Give it a name, write the
instructions the same way you'd type them, pick the working folder (required — point it at
this one), and choose a schedule: manual, hourly, daily, weekdays or weekly. For anything the
picker doesn't offer, just ask Claude in a session: *"schedule a task to run all the tests
every 6 hours."*

- It only fires while the app is open and your computer is awake. Sleep through 9am and the
  run is skipped — though Desktop will start one catch-up run when you wake up, which may be
  hours late. If timing matters, say so in the prompt: *"only look at today's commits."*
- Each task has its own permission mode. Click **Run now** after creating it, approve what it
  asks for with "always allow", and future runs stop stalling.
- The prompt lives on disk at `~/.claude/scheduled-tasks/<task-name>/SKILL.md` if you'd rather
  edit it there.

## Option 4 — `/loop` *(right now, in this session)*

**Use it for:** watching something while you wait. Not for standing automation.

```
/loop 10m check whether the deploy finished and tell me what happened
```

It runs inside the open session, on your machine, and stops when you press `Esc`. Recurring
loops expire after seven days. It's the wrong tool for a morning brief and the right tool for
"tell me when CI goes green".

---

## Choosing, in one question

**"What does this need to touch?"**

| It needs to… | Use |
|---|---|
| Read my connected tools and write me something to read | **Cowork scheduled task** |
| Read or write files in this folder, on a schedule | **Desktop scheduled task** (or a Cowork task with the folder attached) |
| Work in a GitHub repo — code, branches, pull requests | **Claude Code routine** |
| Keep an eye on something for the next twenty minutes | **`/loop`** |

---

## Where the output lands

This is the design decision people miss, and it's the one that decides whether you actually
read the thing. A cloud task has no `my-system/` folder to write to. You have three honest
options:

1. **Leave it in the session.** The Scheduled page holds every run. Cheapest, and fine while
   you're still tuning — but a brief you have to go and find is a brief you stop reading.
2. **Attach the folder.** The output lands in `my-system/standup-brief.md` exactly as the
   recipes describe. The cost is that the task now only runs when your machine is on.
3. **Send it somewhere you already look.** Have the task write to a Google Doc, or draft an
   email to yourself, through a connector. This is usually the right answer for a daily brief:
   the friction of opening one more app is what kills these.

Whichever you pick, say it explicitly in the prompt's output contract. "Write to
`standup-brief.md`" means nothing to a task with no folder attached, and you'll get a run that
looks successful and produced nothing you can find.

---

## The rules that stop this going wrong

**Run it manually first.** Every time. The prompt that reads beautifully produces something
mediocre on the first real run, and you want to find that out while you're watching.

**Read the first three unattended runs properly.** Then change exactly one thing. Three rounds
of one change beats one round of five.

**Nothing sends, posts, files or assigns.** A scheduled task is unattended by definition, so
the approval rule has to live in the prompt: *"Do not create anything in Jira. Write the
candidates to a file for my review."* On a cloud routine, also remove the connectors it
doesn't need — an autonomous run with write access to your board is a different risk from a
draft in a file.

**Give it a stop condition.** *"If nothing material happened, write the date and 'nothing
material.' Do not pad."* Unattended tasks that pad are how you learn to stop reading them.

**Put an end date in your head.** If you haven't read the output in a fortnight, turn it off.
Automations you ignore are worse than no automation — they make the useful ones invisible.

---

## What to schedule where, for the nine recipes

| Recipe | Where | Why |
|---|---|---|
| `pre-standup-brief.md` | Cowork scheduled task, weekdays | Reads connectors, writes prose. The flagship. |
| `stakeholder-update-drafter.md` | Cowork scheduled task, weekly | Same — and **never** let this one send |
| `feedback-themes-weekly.md` | Cowork scheduled task, weekly | Same |
| `blocked-ticket-watcher.md` | Cowork scheduled task, daily | Same |
| `sprint-health-warning.md` | Cowork scheduled task, weekly | Time it mid-sprint |
| `competitor-watch.md` | Cowork scheduled task, weekdays | Needs only web access — works on day one |
| `meeting-actions-router.md` | Triggered, not scheduled | You run it after a call. Save it as a manual task so the prompt is one click away. |
| `pre-meeting-one-pager.md` | Triggered, not scheduled | Same |
| `prd-drift-checker.md` | Cowork task if your spec is in Confluence; **routine** if it's in a repo | Follow the spec |

**Triggered doesn't mean unsaved.** Both Cowork and the Desktop app let you save a task with
no schedule and a **Run now** button. That's where your after-a-call prompts belong — the
friction you're removing is finding the prompt, not typing "go".
