# Week 3 Homework — Integration → Delivery

**Applied AI Cohort · Week 3 · due before Week 4 (Wednesday 26 August)**

---

## The short version

| # | Task | Tag | Rough time |
|---|---|---|---|
| **1** | **Design your capstone** — the plan for your personal AI operating system | `#capstone` | 45–60 min |
| **2** | **Get v0.3 running** against your own work data | `#v0.3` | 15–20 min |
| **3** | *Stretch:* finish your SnapLedger story and deploy it | `#shipped` | 45–90 min |
| **4** | *Stretch+:* AI receipt analysis with tests | `#shipped` | 90+ min |
| **5** | *Bonus:* a skill that encodes one of your standards | `#skills` | 30 min |

Tasks 1 and 2 are the ones that matter. Everything below them is there because some of you
will want more, and because Week 4 is easier if you've already been through the pain.

Post everything in the community space. **If you get stuck, say so there** — that's more
useful to everyone than quietly stopping, and I'll pick it up.

---

## 1. Design your capstone *(main task)*

**The deliverable:** a filled-in capstone plan. The template is in the starter kit at
`0-capstone/capstone-plan-template.md`, and there's a fully worked example next to it.

Your capstone is **a personal AI operating system** — several automations working together on
your real tools, with you approving rather than operating. It is not one script.

**It should be grounded in your own world**: your team, your product, or a side project.
Real data you already care about. Not SnapLedger — that was the sandbox.

The plan names:

- **The problem** — the recurring work this is for, and what it costs you today
- **Integrations** — which tools feed it, read or write, and what's already connected
- **Workflows** — what runs on a schedule, and what you trigger
- **Skills** — what encodes your standards or your voice
- **The approval rule** — what waits for you, and what (if anything) doesn't
- **What's already running** — honestly. "Nothing yet" is allowed; one running thing is worth
  ten planned ones
- **Risks and open questions** — including anything you need help with

**What good looks like:** two pages, specific enough that someone else could build it, with at
least one component already working. If you can't write the one-sentence summary in section 2,
the scope isn't clear yet — that's the part to wrestle with.

**Post:** your plan (or a link to it) with `#capstone`, plus one sentence: *"My capstone
automates ___."*

---

## 2. Get v0.3 running against your own work *(core)*

You built this in the session. Now let it earn its place for a week.

**Point it at your own data** — your team's board, your side project, your calendar. The
recipe is in the starter kit at `5-automation-recipes/pre-standup-brief.md`, and the annotated
standing instruction is at `1-standing-instructions/v0.3-connected.md`.

**What to do:**

1. Confirm it ran unattended at least three times this week
2. Read the outputs properly — don't just let them pile up
3. Change **one thing** based on what you read. One. Then watch what that does.
4. Post the best morning's output with `#v0.3`, and say what you changed and why

**What good looks like:** an output you'd have missed if it hadn't run. If after three days
nothing in it has been useful, post that instead — a specific "here's what it gave me and why
it's useless" is something I can fix with you in ten minutes.

---

## 3. Finish and ship your SnapLedger story *(stretch)*

You opened a pull request in the session. Take it the rest of the way.

1. Merge your PR (or finish the story if you ran out of time)
2. Deploy the app free on **Vercel** — connect your GitHub repo, accept the defaults
3. Open it on your phone. It's a mobile-friendly web app; it should feel like one.

**Post** the live link with `#shipped`.

**Why bother:** a link a colleague can click is a fundamentally different object from a
document describing what you'd build. This is the whole "show, don't tell" idea, made real.

---

## 4. Receipt analysis, with tests *(stretch+)*

The genuinely hard one. Only worth starting if task 3 is done.

SnapLedger's core promise is that it reads receipts. Let's find out how well AI actually does
that, and — more importantly — **how you'd know**.

1. Grab the **30 sample receipts** from the community space (they include some deliberately
   awkward ones: blurry, handwritten totals, no VAT line, a duplicate, one in euros)
2. Add a feature that sends a receipt image to Claude and extracts merchant, date, total and
   VAT. This needs an **Anthropic API key** — create one at `console.anthropic.com`; a few
   dollars of credit covers this comfortably. Claude Code will walk you through wiring it up.
3. **Write unit tests** that run the extraction across all 30 receipts and compare against the
   answer key that ships with them
4. Run them. Note the score.

**Then answer the PM questions**, which are the actual point:

- Which receipts failed, and is there a pattern?
- What confidence threshold would you set before a receipt goes straight through versus
  landing in a human review queue?
- What would you tell a customer your accuracy is — and what would you refuse to promise?

**Post** your score and your answers to those three questions with `#shipped`.

This is what evaluating an AI feature actually looks like. Most PMs shipping AI features today
have never done it once.

---

## 5. Build a skill *(bonus)*

We go deep on skills in Week 4. If you want a head start, pick one of these:

- **A ticket-format skill** — encodes your house user story shape so every ticket Claude drafts
  comes out right without you re-explaining
- **A PRD skill** — your PRD structure and the questions you always want answered

Try it on the SnapLedger backlog you built, or on real work. Post what you built with
`#skills`, and bring it to Week 4.

---

## What I'll be looking at before Week 4

I'll read every `#capstone` post and comment on it. Where a plan is over-scoped I'll say so —
better now than on demo day.

**If any of this feels like too much**, tell me. There are catch-up resources in the community
space, and I'm happy to do a one-to-one to get you unstuck. The point of this week is momentum,
not homework for its own sake.

---

## Reference

- **Starter kit** — everything above has a template or a recipe in it
- **Your sandbox Jira project** — stays open all week
- **Community space** — slides, recording, sample receipts, catch-up resources
- **Week 4 is Wednesday 26 August** — capstone demos. Three minutes each: the before, the run,
  the after.
