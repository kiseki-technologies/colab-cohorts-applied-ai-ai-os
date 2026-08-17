# Anatomy of a standing instruction

A standing instruction is the prompt behind a scheduled task. It runs without you in the room,
so it can't ask clarifying questions. That changes how you write it.

Every instruction in this kit has the same five parts.

---

### 1. Cadence and trigger
*When does this run, and what does it look at?*

Be explicit about the window: "the last 24 hours", "since the last entry", "this sprint".
Without a window, an unattended task re-reports the same things forever.

### 2. Sources
*Exactly where the information comes from.*

Name the connector, the project, the folder, the channel. "Check Jira" is weaker than
"Using the Atlassian connector, list issues in PROJECT-KEY that changed status in the last
24 hours". Vague sources produce confident invention.

### 3. The judgement instruction
*What to do with what it finds.*

This is the difference between v0.1 and v0.2, and it's where most of the value lives.
"Tell me what changed" produces a list you still have to read. "Assess what changed against
[MY CONTEXT] and only surface what plausibly affects [MY THESIS]" produces something you act on.

### 4. Output contract
*Shape, length, and where it goes.*

Name the file. Name the sections. Set a word limit. Say what to do when there's nothing to
report — otherwise a quiet week produces the most padding.

### 5. The escalation rule
*What "important" looks like, and what to never do.*

"Flag anything that blocks a release." · "Never invent a ticket reference." ·
"If a source is unavailable, say so — don't work around it silently."

---

## The three failure modes, and the line that fixes each

| Failure | What you see | The fix |
|---|---|---|
| **Padding** | Long entries on quiet days | "If nothing material happened, write the date and 'nothing material.' Do not pad." |
| **Invention** | Ticket numbers or quotes that don't exist | "Quote only what you can cite. Never invent a reference. If unsure, say so." |
| **Sameness** | Every entry reads identically | Add context to assess against, and ask for what changed *relative to the last entry* |

---

## Tuning, honestly

Your first run will be mediocre. That's normal and it's not a reason to abandon it.
Read the first output and change exactly one thing — usually the judgement instruction.
Three rounds of that gets you something you'd miss if it stopped.
