# Colab AI OS Starter Kit

**Applied AI Cohort · Colab Cohorts · v1 (Week 3)**

This is the toolkit version of everything we've built across the course: the standing
instructions, prompts, connector guides and automation recipes, plus the templates for
your capstone. Everything here is meant to be **copied and adapted**, not admired.

Nothing in this kit is theoretical. Every prompt has been run; every recipe describes
something that works today.

---

## Start here (15 minutes)

1. **Set the folder up in your tool of choice — `SETUP.md`.** Claude Code, Cowork, or both.
   Do this before the session; it's the one thing that costs you the day if you leave it.
2. **Read `0-capstone/capstone-plan-template.md`.** That's your Week 3 homework deliverable.
3. **Read `0-capstone/worked-example.md`** to see what a finished plan looks like.
4. **Copy one recipe** from `5-automation-recipes/` and get it running against your own data.
   Start with `pre-standup-brief.md` — it's the fastest route to something useful tomorrow
   morning. `5-automation-recipes/scheduling.md` is how you make it repeat.
5. **Skim `1-standing-instructions/ANATOMY.md`.** It explains *why* the prompts here are shaped
   the way they are, so you can write your own.

Your full homework brief is in `WEEK-3-HOMEWORK.md`.

---

## Two ways to use this kit

This is a folder, deliberately. **Point Cowork at it, point Claude Code at it, or both** —
they read the same files and follow the same house rules from `CLAUDE.md`.

| | Reach for it when |
|---|---|
| **Cowork** | You're writing, planning, researching, or drafting from your connected tools. No terminal. Works from your phone. This is where most of this kit lives. |
| **Claude Code** | You're in a repository — implementing a ticket, opening a pull request, running the evals — or you want to watch every step it takes. |

`SETUP.md` has the full comparison, the setup steps for each, and what to do when you want to
use both on the same folder. The short version: **start in Cowork, and open Claude Code when
you hit something that needs git.**

---

## What's in here

| Folder | What it's for |
|---|---|
| `SETUP.md` | Getting this folder working in Claude Code, Cowork, or both. Read first. |
| `CLAUDE.md` | The house rules both tools follow when working in this folder |
| `0-capstone/` | The capstone plan template and a worked example. Start here. |
| `1-standing-instructions/` | The v0.1 → v0.3 prompts behind the scheduled digest, annotated |
| `2-project-setup/` | How to set up a Claude project that knows your product context |
| `3-prompt-library/` | Research, synthesis, PRD/stories and live-data prompts with fill-in slots |
| `4-connector-guides/` | Connecting Atlassian, meeting tools, GitHub — and the governance answers |
| `5-automation-recipes/` | Nine automations, each with the schedule, the prompt and what good looks like |
| `6-week4/` | Filled in after Week 4: skills, shipping to GitHub, capstone patterns |
| `my-system/` | **Your** work. Gitignored, so your real data stays out of commits. |

---

## The version ladder

Your system has been growing one upgrade a week. This kit contains every rung.

| Version | What changed | Where in this kit |
|---|---|---|
| **v0.1** | A scheduled task that runs without you | `1-standing-instructions/v0.1-competitor-watch.md` |
| **v0.2** | Better inputs and a judgement instruction: report → assess | `1-standing-instructions/v0.2-assess-not-report.md` |
| **v0.3** | Connected: it reads your live tools through MCP | `1-standing-instructions/v0.3-connected.md` |
| **v1.0** | Your capstone: several automations working as one system | `0-capstone/` |

---

## Two rules that apply to everything here

**1. You approve, it operates.** Every automation in this kit ends in a draft, a file or a
proposal — never an action taken on your behalf without review. If you adapt a recipe to
post, send or file automatically, do it deliberately, and only once you trust it. This matters
most for anything you schedule: an unattended run can't ask you first, so the rule has to be
written into the prompt. `5-automation-recipes/scheduling.md` says how.

**2. Confidential data stays out.** Use sanitised copies or the course sample data.
Check your organisation's AI policy before you connect a work tool.
`4-connector-guides/governance.md` gives you the answers to the questions IT will ask.

---

## Adapting anything here

Every file uses `[SQUARE BRACKETS]` for the bits you replace. A prompt with three brackets
filled in correctly beats a clever prompt with none. Read the "what good looks like" section
in each recipe before you tune anything.

**Copy before you fill in.** The numbered folders stay clean; your version goes in
`my-system/`. Ask either tool to do the copy — both know the rule.

Questions, or something that doesn't work? Post in the community space. If a recipe fails
for you, that's useful information for everyone — share the failure.
