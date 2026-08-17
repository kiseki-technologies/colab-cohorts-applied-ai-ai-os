# From research to a backlog — the Week 3 prompts

These are the prompts behind Deep Work 1. Fill the brackets, run them in order, review hard
between each one. **The AI drafts; the scoping and the cuts are yours.**

---

## 1. The PRD

```
You have my research synthesis and the market map for [PRODUCT] in this project.

Draft a PRD for v0.1 — the first thing we would actually ship, not the full product.

Structure it as:
- The problem, in the users' words. Quote the research; cite who said it.
- Who it's for, and explicitly who it is not for
- What v0.1 does — the smallest set of capabilities that delivers the core value
- What v0.1 deliberately does NOT do, and why each thing waits
- How we'll know it worked — one or two signals, not a dashboard
- Open questions and the assumptions we're making

Rules: every claim about user need must trace to the research. Where the research is thin,
say so rather than filling the gap. Keep it under two pages — this is a v0.1, not a vision.
```

**Review before you move on:** is the "does NOT do" section longer than the "does" section?
If not, you haven't scoped yet.

---

## 2. Epics and stories

```
From the PRD, decompose v0.1 into epics and user stories.

You decide the split — I want your reasoning, not a fixed number. For each epic, tell me
why those stories belong together and why they're separated from the others.

For every story:
- The story itself, in whatever form makes it clearest
- Acceptance criteria specific enough that someone who has never spoken to me could build
  it and know when they were done
- What is explicitly out of scope for this story
- A link back to the PRD section or research finding it serves

Flag any story that is really two stories. Flag any acceptance criterion that can't be
verified by looking at the product.
```

**Review before you move on:** pick your vaguest story and ask *"what would a literal-minded
engineer build from this?"* That's the question the peer review will ask you.

---

## 3. Onto the board

```
Using the Atlassian connector, create these in [YOUR PROJECT KEY]:
- the epic
- each user story, linked to the epic, assigned to me

Use exactly the wording we agreed. Do not improve it on the way in.
After you create them, list what you created with the issue keys so I can check.
```

**Note:** "Do not improve it on the way in" matters. You want the board to hold the thing you
reviewed, not a fresh paraphrase of it.

---

## 4. Handing a story to Claude Code

Once your stories are on the board, in Claude Code:

```
Using the Atlassian connector, read [ISSUE-KEY] from [PROJECT].

Implement it in this repository, following the conventions in CLAUDE.md and the design
reference in the README.

Work on a branch named feat/[issue-key]. When you're done:
- summarise what you built and any decisions you had to make that the ticket didn't cover
- tell me anything in the ticket that was ambiguous
- commit and open a pull request

If the acceptance criteria are unclear, tell me before you build rather than guessing.
```

**The last two instructions are the point of the exercise.** What it says was ambiguous is
your ticket-quality feedback, and almost nobody in product ever gets it this fast.
