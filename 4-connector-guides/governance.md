# Governance — the questions IT will ask

The PM who can answer these is the PM whose integration gets approved. Have the answers before
you ask.

## The four questions

**1. Where does the data go, and is it retained?**
Know your organisation's plan and its data-retention terms. Enterprise agreements typically
differ from consumer plans. Find the answer for *your* account rather than assuming.

**2. Read-only or write access?**
Scope the minimum that does the job. Most of what's valuable — briefs, syntheses, drafts —
needs read only. Ask for write access when you actually need it, not preemptively.

**3. What does our AI policy allow?**
Many organisations have one now. Read it before you connect a work tool. If there isn't one,
that's worth raising — and being the person who raises it constructively is a good look.

**4. Can access be revoked?**
Yes, and you should know how before you grant it. Revoke connectors you've stopped using.

---

## Business case template

> **What I want to connect:** [TOOL], read-only, scoped to [PROJECT/SPACE].
>
> **What it's for:** [e.g. "an automated daily brief that summarises ticket movement and
> flags blockers, so I spend less time assembling status and more time on decisions."]
>
> **What data is involved:** [e.g. "issue titles, statuses and comments in one project. No
> customer PII, no financial data."]
>
> **Where it goes:** [your answer to question 1].
>
> **Controls:** read-only scope; access revocable at any time; no automated actions — every
> output is a draft I review.
>
> **What I'd like:** approval for a [4]-week trial, after which I'll share what it produced
> and we can decide.
>
> Happy to walk through it with whoever owns this.

---

## The habits that keep this clean

- Sanitise before you load. Customer names and PII don't need to be there for the work to work.
- Revoke what you've stopped using — a quarterly sweep takes five minutes.
- Never paste credentials, keys or tokens into a prompt.
- If you wouldn't be comfortable with it appearing in a screenshot, don't put it in.
