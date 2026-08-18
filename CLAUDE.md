# CLAUDE.md — how to work in this folder

**What this is:** the Colab Applied AI starter kit. Templates, prompts, connector guides and
automation recipes for building a personal AI operating system.

**Who you're working with:** a product person — a PM, designer or analyst — who may or may not
write code. They can read Markdown and follow instructions. Don't assume they read code, and
don't answer in code when prose would do.

**This file applies to both surfaces.** Claude Code reads it automatically. In Cowork, the
folder instructions should say: *"Read CLAUDE.md in this folder first and follow it."*
See `SETUP.md`.

---

## What you're usually being asked to do

1. **Fill in a template** — most often `0-capstone/capstone-plan-template.md`
2. **Adapt a recipe** from `5-automation-recipes/` to this person's tools and cadence
3. **Draft or tune a standing instruction** — the prompt behind a scheduled task
4. **Run an automation once, manually**, against their live tools, so they can see the output
   before they schedule it
5. **Review something they wrote** — a plan, a prompt, a ticket — against the standards in
   `1-standing-instructions/ANATOMY.md`

## House rules

- **The numbered folders are source material. Don't fill them in.** When someone works
  through a template, copy it to `my-system/` first and edit the copy. The originals stay
  clean so the next person can use them.
- **Everything a student produces goes in `my-system/`.** It's gitignored, so their real work
  data never lands in a commit.
- **Never invent** a ticket reference, quote, metric, source or date. `"no ticket found"` is a
  correct answer; a plausible-looking ticket key is a serious failure.
- **Fill `[BRACKETS]` by asking, not guessing.** One clarifying question is cheaper than a
  confidently wrong assumption. If the answer doesn't change the output, pick a sensible
  default and say which you picked.
- **Nothing sends, posts, files or assigns.** Every automation here ends in a draft, a file or
  a proposal that waits for a human. If asked to create Jira tickets or send anything, confirm
  first and use exactly the wording that was reviewed — don't improve it on the way in.
- **If a source is unavailable, say so.** Never quietly substitute a different source or work
  from memory of what was probably there.
- **Keep confidential material out.** No customer PII, credentials, API keys or restricted
  financials in any file in this folder. Sanitise before loading; flag it if you spot it.

## Voice

Plain and direct. British spelling. No marketing adjectives. Short lines. Tables where a
table is clearer than a paragraph. Every recipe ends with "what good looks like" — match that
shape when you write a new one.

## Where things live

| Folder | Contents |
|---|---|
| `SETUP.md` | Setting this up in Claude Code, in Cowork, or both. Read first. |
| `0-capstone/` | The capstone plan template and a worked example |
| `1-standing-instructions/` | v0.1 → v0.3 of the scheduled digest, annotated. `ANATOMY.md` is the theory. |
| `2-project-setup/` | Context checklist, and the "how to work with me" template |
| `3-prompt-library/` | Research, synthesis, PRD/stories, live-data prompts |
| `4-connector-guides/` | Atlassian, meeting tools, GitHub, governance |
| `5-automation-recipes/` | Nine automations. `scheduling.md` explains how to make them repeat. |
| `6-week4/` | Filled in after Week 4 |
| `my-system/` | Where the student's own work goes. Gitignored. |

## Two questions worth asking early

- **"Do you want this to run in Cowork or in Claude Code?"** They're different cockpits on the
  same engine and the answer changes what you build. `SETUP.md` has the comparison.
- **"Does this need to repeat on a schedule?"** If yes, read
  `5-automation-recipes/scheduling.md` before you write the prompt — where it runs determines
  what it can reach and where the output can land.
