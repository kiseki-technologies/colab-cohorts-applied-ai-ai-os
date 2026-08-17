# Context checklist — what to load, what to leave out

An AI system is only as good as what it knows about your world. This is the loading list.

## Load these (in rough order of value)

- [ ] **Current strategy or quarterly goals** — one page beats twenty
- [ ] **The PRD or spec** for whatever you're working on now
- [ ] **Research synthesis** — themes, quotes, contradictions
- [ ] **Personas or segments**, if they're real and used
- [ ] **Recent meeting transcripts** — decisions age fast; keep the last month
- [ ] **A few examples of your own writing** — updates, tickets, docs. This is how it learns
      to sound like you rather than like a model.
- [ ] **Competitive/market context** — the market map, positioning notes
- [ ] **Glossary** — your acronyms, product area names, team names

## The one most people skip

**Examples of your own writing.** Three real stakeholder updates will do more for output
quality than any amount of prompt engineering. The model can copy your shape; it can't
guess it.

## Leave these out

- ❌ Customer names, emails, or anything personally identifying — sanitise first
- ❌ Anything under NDA that you haven't checked
- ❌ Salary, performance or HR material
- ❌ Credentials, API keys, tokens
- ❌ Financial data your org treats as restricted — use ranges or say "commercially sensitive"

**When in doubt:** would you be comfortable if this document appeared in a screenshot in a
conference talk? If not, sanitise it before it goes in.

## Keeping it fresh

Context rots. Once a month: remove superseded docs, add the current quarter's goals, refresh
the meeting transcripts. Ten minutes, and it's the difference between a system that knows
your world and one that knows last quarter's.
