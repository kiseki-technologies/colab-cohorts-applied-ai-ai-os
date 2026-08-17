# Stakeholder update drafter

Turns the worst hour of your Friday into fifteen minutes of editing.

**Cadence:** weekly, ~2 hours before you'd normally write it
**Needs:** tracker + meeting tool. Calendar helps.

---

## The prompt

```
Every [Friday] at [15:00], draft my [weekly] stakeholder update.

Sources:
- [PROJECT-KEY] in Jira — what moved this week, what slipped, what's blocked
- My meetings from the last 7 days — decisions taken, risks raised, commitments made
- [any other source]

Format:
[YOUR FORMAT — e.g.
 1. Headline: one sentence on where we are
 2. Risks and slippage — lead with these, don't bury them
 3. Progress — what actually shipped or moved materially
 4. Decisions needed from you]

Under [300] words. Write it in my voice: [plain, direct, numbers or nothing, no adjectives].

For every claim, attach the evidence (issue key, meeting, date) in a separate section at the
bottom so I can check it before I send. Never state something as done unless the ticket says
it's done.

Save it to updates/[DATE]-draft.md. Do not send anything.
```

---

## What good looks like

You edit for ten minutes and send. The evidence section means you can check a claim in seconds
rather than re-deriving it.

If you find yourself rewriting from scratch, the voice instruction is too vague — add two of
your own previous updates to the project and say "match the style of these".

---

## The honest warning

This one is seductive because it saves the most obvious time. It's also the one where an
unreviewed error is most expensive, because it goes to the people whose trust you rely on.

**Never let this one send automatically.** Not in month one, not in month six.
