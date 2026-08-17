# Meeting actions router

The gap between "we agreed that in the call" and "there's a ticket for it" is where most
product chaos lives. This closes it.

**Cadence:** triggered after a call (or daily, batched)
**Needs:** meeting tool + tracker

---

## The prompt

```
Read the transcript of [MEETING / my meetings from today].

Produce three things:

1. DECISIONS — what was decided, by whom, and the reasoning if it was captured.
2. ACTIONS — who owns what, by when. Mark anything where the owner is ambiguous.
3. CANDIDATE TICKETS — for anything that implies product work, draft a ticket following the
   conventions in [CLAUDE.md / my project instructions]: context, acceptance criteria,
   explicit out-of-scope, and the quote from the meeting that justifies it.

Do not create anything in Jira. Write the candidates to proposed-tickets.md for my review.

If something was discussed but not decided, list it separately under OPEN — do not turn an
unresolved discussion into a ticket.
```

---

## What good looks like

The OPEN section is the quality signal. A router that turns every discussion into a ticket is
worse than useless — it fills your backlog with things nobody agreed to.

---

## Promoting a candidate to a real ticket

Once you've reviewed:

```
Create the tickets I've marked APPROVED in proposed-tickets.md in [PROJECT-KEY],
using exactly the wording as written. List what you created with issue keys.
```

**"Using exactly the wording as written"** matters — you reviewed a specific text, and that's
the text that should land.
