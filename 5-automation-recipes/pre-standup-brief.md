# Pre-standup brief

**The flagship recipe.** Runs before you're awake enough to want it, and catches the thing you
forgot you promised.

**Cadence:** weekdays, 08:00 (or 30 minutes before your standup)
**Needs:** your tracker. Better with a meeting tool.

---

## The prompt

```
Every weekday at 08:00:

1. Using the Atlassian connector, list every issue in [PROJECT-KEY] that changed status in
   the last 24 hours, and every issue currently blocked or flagged at risk.
2. Using [MEETING TOOL], read yesterday's meeting transcripts. Extract anything I committed
   to, and anything committed to me.
3. Cross-reference: name any commitment from step 2 with no corresponding ticket from step 1.

Write a dated entry to standup-brief.md with three sections:

MOVED — what changed, and who moved it
STUCK — what's blocked, how long, who owns it
UNTICKETED — commitments with no ticket. These are the ones I'll get asked about.

Under 200 words. If a section is empty, say so in one line. Never invent a ticket reference —
if you can't find one, write "no ticket found".
```

---

## What good looks like

```
Thursday 20 August

MOVED
- ABC-114 In Progress → Review (Sam). ABC-119 opened, unestimated.

STUCK
- ABC-102 blocked 4 days on the auth spike. Owner: Priya. Nobody has chased it.

UNTICKETED
- In Tuesday's design sync you agreed to decide on the onboarding flow by Thursday.
  No ticket found.
```

The third section is the one that earns its keep. The first two you could have found yourself
in three tabs.

---

## Tuning

| Problem | Fix |
|---|---|
| Too noisy | Add "only issues in the current sprint" or "ignore sub-tasks" |
| Too quiet on Mondays | Widen the window to 72 hours for Monday runs |
| Reads like a status report | Add: "Lead with anything I'd be embarrassed not to know" |
| Missing the good stuff | Check the meeting tool is actually connected — step 3 silently degrades |

## Variations

- **No tracker?** Run steps 2 and 3 against your notes and calendar alone.
- **Managing several areas?** One run per project beats one run covering everything.
- **Not a standup person?** Same recipe, 17:00, framed as "what I should pick up tomorrow".
