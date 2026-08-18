# Week 3 Homework — Integration → Delivery

**Applied AI Cohort · Week 3 · due before Week 4 (Wednesday 26 August)**

---

## The short version

| # | Task | Tag | Rough time |
|---|---|---|---|
| **1** | **Design your capstone** — the plan for your personal AI operating system | `#capstone` | 45–60 min |
| **2** | **Get v0.3 running** against your own work data | `#v0.3` | 15–20 min |
| **3** | *Stretch:* finish your SnapLedger story and deploy it | `#shipped` | 45–90 min |
| **4** | *Stretch+:* build an eval suite for AI receipt reading | `#shipped` | 90+ min |
| **5** | *Bonus:* a skill that encodes one of your standards | `#skills` | 30 min |

Tasks 1 and 2 are the ones that matter. Everything below them is there because some of you
will want more, and because Week 4 is easier if you've already been through the pain.

Post everything in the community space. **If you get stuck, say so there** — that's more
useful to everyone than quietly stopping, and I'll pick it up.

**Before you start:** open the starter kit and read `SETUP.md`. It's fifteen minutes, it
covers setting the folder up in **Cowork**, in **Claude Code**, or both, and it tells you which
to reach for. Tasks 1 and 2 are Cowork work; tasks 3 and 4 are Claude Code.

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

**Where to schedule it:** a **Cowork scheduled task** on weekdays is the right answer for
almost everyone — no terminal, and it fires whether or not your laptop is open. If you'd rather
it ran on your machine against your own folder, or the work is repo-shaped, the alternatives
and the trade-offs are in `5-automation-recipes/scheduling.md`. Decide where the output lands
before you schedule anything; a brief you have to go looking for is a brief you stop reading.

**What to do:**

1. Run it by hand once and read what comes back. Only then schedule it.
2. Confirm it ran unattended at least three times this week
3. Read the outputs properly — don't just let them pile up
4. Change **one thing** based on what you read. One. Then watch what that does.
5. Post the best morning's output with `#v0.3`, and say what you changed and why

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

## 4. Build an eval suite for receipt reading *(stretch+)*

The genuinely hard one, and the most transferable thing in the course. Only worth starting if
task 3 is done.

SnapLedger's core promise is that it reads receipts. Let's find out how well AI actually does
that, and — more importantly — **how you'd know**.

**Everything you need is already in your repo,** in `evals/`: 40 receipts belonging to Priya
Raman, the freelancer from your Week 2 research. Photographed on desks, emailed, scanned. One
has faded past reading. One is handwritten. Two are the same purchase captured twice. Some are
in euros.

- **30 come with a published answer key** — your development set
- **10 are held back with no answers anywhere in the repo.** You run your extractor over them
  and post the raw output; I have the answers and score them.

That second number is the interesting one. It's very easy to build something that scores
brilliantly on the 30 you tuned against and falls apart on anything else, and the gap between
the two tells you which you built.

**The work, in three steps:**

1. **Extract** — a feature that sends a receipt image to Claude and returns merchant, date,
   currency, total, VAT and card. Needs an **Anthropic API key**: create one at
   `console.anthropic.com`; a few dollars of credit covers this many times over. Set a spend
   limit anyway.
2. **Score** — tests that run it across all 30 and compare against the answer key. Report
   **per field**, not one blended number.
3. **Slice** — break the score down by what kind of receipt it is. Every receipt is tagged.
   You're looking for a shape: does it fail on handwriting? On foreign currency? On anything
   photographed at an angle?

**The full brief is `evals/README.md` in your repo.** Read it before you build — the scoring
decisions shape the feature, not the other way round.

**One rule, and it's the one people trip over:** your extraction code must never read the
answer key. Only the test file may. Ask Claude Code to "make the tests pass" without saying
this and a well-behaved agent will read the answers and build you a suite that scores 100% and
measures nothing. If that happens, don't just fix it — that's a real production failure mode
and catching it is worth more than the score.

**Then answer the PM questions**, which are the actual point:

- Which receipts failed, and is there a pattern?
- What confidence threshold would you set before a receipt goes straight through versus
  landing in a human review queue — and what does that threshold cost, on both sides?
- What would you tell a customer your accuracy is, and what would you refuse to promise?

**Post** with `#shipped`: your per-field scores, your breakdown by receipt type, your raw
output on the held-back ten, and your answers to those three questions.

**What good looks like:** "it loses 40% of its accuracy on anything handwritten, so
handwriting goes to review regardless of confidence, and I'd tell a customer 95% on printed
receipts rather than 88% overall." That sentence is a PM doing AI product work, and nothing
about it required you to be an engineer.

Most PMs shipping AI features today have never done this once.

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

I'll also score anyone who posts held-back receipt output, and tell you the gap between your
development-set score and your held-out one.

**If any of this feels like too much**, tell me. There are catch-up resources in the community
space, and I'm happy to do a one-to-one to get you unstuck. The point of this week is momentum,
not homework for its own sake.

---

## Reference

- **Starter kit** — everything above has a template or a recipe in it. Start with `SETUP.md`,
  and `5-automation-recipes/scheduling.md` for anything that needs to repeat.
- **Your SnapLedger repo** — the app, the design reference, and the `evals/` receipt set
- **Your sandbox Jira project** — stays open all week
- **Community space** — slides, recording, catch-up resources
- **Week 4 is Wednesday 26 August** — capstone demos. Three minutes each: the before, the run,
  the after.
