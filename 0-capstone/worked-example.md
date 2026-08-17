# Worked Example — a finished capstone plan

**This is the example from the Week 3 slides, written out in full.**

It belongs to a fictional PM, Maya, who runs a B2B SaaS product with two squads.
**Yours will look nothing like this — that's the point.** Same anatomy, your job, your data.

---

## 1. The problem

**The work:** Every week I assemble the same picture three times — once for standup, once for
my Friday stakeholder update, and once whenever someone asks "what's happening with X?".
The inputs are always the same: the board, my meetings, and the customer feedback channel.

**What it costs me:** Roughly 4 hours a week, most of it on Friday afternoon when I'm least
sharp. And the quality drops exactly when the week has been busiest — which is when the
update matters most.

**Why it's a good candidate:** It's recurring, the inputs are all digital and already
connected, and the hard part is assembly, not judgement. The judgement is mine and stays mine.

---

## 2. The system in one sentence

> My AI operating system assembles the state of my product every day and every Friday by
> reading Jira, my meeting transcripts, Slack and my calendar, so that I edit and approve
> instead of hunting and retyping.

---

## 3. Integrations

| Tool | What it provides | Read or write? | Status |
|---|---|---|---|
| Jira | Sprint state, ticket movements, blockers | Read + write (drafts tickets) | ✅ connected |
| Granola | Commitments and decisions from calls | Read | ✅ connected |
| Slack (#customer-feedback) | Raw customer signal | Read | ⬜ workspace admin approval requested |
| Google Calendar | What's coming this week, who I'm seeing | Read | ✅ connected |
| Gmail | Escalation emails from account managers | Read | ⬜ later |

**Anything blocked?** Slack needs admin approval — asked on Monday, expect it this week.
Until then the feedback synthesiser runs on a manual export, which is fine for testing.

---

## 4. Workflows

### Scheduled (runs without me)

| When | What it does | Output lands where |
|---|---|---|
| Weekdays 08:00 | Pre-standup brief: what moved, what's stuck, and anything I committed to in yesterday's calls that has no ticket | `standup-brief.md` in my project folder |
| Fridays 15:00 | Assembles the week — board movement, decisions from meetings, risks — and drafts my stakeholder update in my format | Draft file, waiting for me |
| Mondays 07:00 | Batches the week's customer feedback into themes with counts, flags any theme that's new | `feedback-themes.md` |

### Triggered (I start it)

| Trigger | What it does |
|---|---|
| After a customer call | Reads the transcript, extracts decisions and actions, drafts candidate Jira tickets with acceptance criteria for my approval |
| Before a stakeholder 1:1 | One-pager: what we last agreed, what's moved since, what I need from them |

---

## 5. Skills

| Skill | What it enforces |
|---|---|
| `ticket-format` | Our house user story shape — context, acceptance criteria, explicit out-of-scope. No ticket leaves without acceptance criteria. |
| `update-voice` | How I write updates: lead with the risk, no adjectives, numbers or nothing, under 300 words. |

---

## 6. The human-approval rule

**Nothing sends, posts or files itself.** Every automation ends in a draft waiting for me:
tickets are proposed, not created; the stakeholder update sits in a file until I've edited it.

**The one exception:** the daily standup brief writes to a private file only I read. Nothing
about it is visible to anyone else, so it runs unattended without review.

---

## 7. What's already running

- [x] v0.3 pre-standup brief — running since Wednesday, against my real board
- [ ] Friday update drafter — prompt written, not yet scheduled
- [ ] Feedback synthesiser — blocked on Slack approval

**Best output so far:** Thursday's brief caught that I'd promised the design lead a decision
on the onboarding flow in Tuesday's call, and there was no ticket for it. I'd genuinely
forgotten. That single line justified the whole thing.

---

## 8. Risks and open questions

- The Friday update reads as generic when the week was quiet — I think the instruction needs
  a "if nothing material happened, say so in two lines and stop" rule.
- I don't want ticket drafts cluttering the real backlog. Plan: they go to a separate
  "proposed" project and I move them across after review.
- Slack approval may not land. Mitigation: manual export weekly; it's 5 minutes.

---

## 9. What I'll demo in Week 4

**The before:** 4 hours a week of assembly, worst on Friday afternoons.

**The run:** I'll show Thursday's standup brief with the caught-commitment line, then trigger
the meeting-actions router live on a recorded call.

**The after:** I read and edit for about 20 minutes a week instead of assembling for four
hours. What I removed was retyping, not thinking.

**Rough time saved:** ~3 hours a week, and one fewer thing to dread on a Friday.
