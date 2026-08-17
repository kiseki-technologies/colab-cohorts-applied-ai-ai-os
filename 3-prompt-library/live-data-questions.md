# Questions worth asking your connected tools

Once Claude can read your tools, the limiting factor is the quality of your questions.
These are starting points — the value is in adapting them to your world.

---

## Sprint health

```
Using the Atlassian connector, look at the current sprint in [PROJECT].

Tell me what's genuinely at risk and why — not a status summary. Specifically:
- anything blocked, how long, and who owns unblocking it
- stories without acceptance criteria
- scope that has been added since the sprint started
- anything assigned to someone who is out this week

Rank by what would actually threaten the sprint goal. Ignore noise.
```

## Meeting memory

```
Using [MEETING TOOL], read my meetings from the last [7] days.

Extract:
- every commitment I made, and to whom
- every commitment made to me
- decisions taken, with the reasoning if it was captured

Then cross-reference against [PROJECT] in Jira and tell me which commitments have no ticket.
```

## Stakeholder update

```
Assemble my [weekly] stakeholder update.

Sources: the board in [PROJECT], my meetings from the last week, and any decisions recorded
in [CONFLUENCE SPACE].

Format: [YOUR FORMAT — e.g. lead with risks, then progress, then what I need from them].
Under [300] words. Lead with anything that has slipped; don't bury it.

Attach the evidence for each claim so I can check it before I send.
```

## Feedback themes

```
Read [SOURCE — support tickets / #feedback channel / review exports] from the last [month].

Group into themes. For each: how many mentions, verbatim quotes, and which segment it came
from. Flag any theme that is new compared with [PREVIOUS PERIOD].

Do not merge themes that feel similar but have different causes. Tell me where the evidence
is too thin to call it a theme.
```

## PRD drift (advanced)

```
Compare the current backlog in [PROJECT] against the PRD in [CONFLUENCE PAGE].

Tell me:
- stories that don't trace to anything in the PRD
- PRD commitments with no story
- anywhere the backlog has quietly changed what we said we'd build

This is a hygiene check, not a criticism. Be specific about what to look at.
```
