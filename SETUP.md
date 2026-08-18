# Setup — Claude Code, Cowork, or both

**Read this before Week 3's session.** It takes about fifteen minutes and it's the difference
between building something on the day and watching someone else build something.

This kit is a **folder**, deliberately. Both Claude Code and Cowork can be pointed at the same
folder and work on the same files. You do not have to choose one — most people in this cohort
will end up using both, for different jobs.

---

## Before you start

| You need | Why | Check |
|---|---|---|
| A paid Claude plan — Pro, Max, Team or Enterprise | Cowork and scheduled automation are paid features | claude.ai → your account |
| This folder on your machine | Both tools work on local files | You're reading this file, so — done |
| Ten minutes of connector setup | The whole of v0.3 depends on it | See below |
| A terminal you're willing to open **(Claude Code only)** | It's one command; you never have to write code | Terminal.app, or the Claude Code desktop app instead |

On Team and Enterprise plans some of this needs an admin to enable it. If something below
isn't there, that's usually why — ask, don't assume it's broken.

---

## Step 1 — Connect your tools once (both surfaces share them)

This is the step people skip and then wonder why nothing works.

Go to **claude.ai → Settings → Connectors** (`claude.ai/customize/connectors`) and connect the
tools you actually use. For this cohort: **Atlassian**, your **meeting recorder**, and
**Google Calendar** if you want the good version of the morning brief.
`4-connector-guides/` has one page per tool.

**Connect them once and both Cowork and Claude Code can see them** — Claude Code picks up the
connectors from the claude.ai account you signed in with. Run `/mcp` inside Claude Code to
check. This catches people out because it didn't always work this way, and older notes will
tell you the two are separate.

**Verify before you build.** Ask a question you already know the answer to:

```
Using the Atlassian connector, what issues are in [YOUR PROJECT KEY]?
```

If that comes back wrong or empty, fix it now. Everything else in this kit sits on top of it.

---

## Step 2a — Set this folder up in Claude Code

1. Install Claude Code from `claude.com/claude-code` and sign in with your Claude account
2. Open a terminal in this folder and run:

```
claude
```

3. Accept the workspace trust prompt. Claude Code reads `CLAUDE.md` automatically, so it
   already knows what this folder is and how you want it to work.
4. Try it:

```
Read 5-automation-recipes/pre-standup-brief.md, then help me fill in the brackets
for my own board and run it once.
```

Prefer buttons to a terminal? The **Claude Code desktop app** is the same tool with a
window around it, and it's where local scheduled tasks live. Both read the same folder.

## Step 2b — Set this folder up in Cowork

1. Open **Claude Desktop** (macOS or Windows). Cowork projects with a local folder are set up
   on the desktop app and stored on that machine — file access runs through it.
2. Select **Cowork**, then create a project and choose **use an existing folder**
3. Point it at this folder
4. In the project's **instructions**, paste:

```
Read CLAUDE.md in this folder first and follow it. I'm a product manager, not an
engineer. My work goes in my-system/ — never edit the numbered folders.
```

5. Try the same thing you tried in Claude Code:

```
Read 5-automation-recipes/pre-standup-brief.md, then help me fill in the brackets
for my own board and run it once.
```

Cowork projects are stored locally on that machine and don't sync between your devices. Set it
up on the laptop you actually work on.

---

## Which one, when

They're the same engine. Cowork runs the same agentic architecture that powers Claude Code —
what differs is the cockpit, and what each one can reach.

| | **Cowork** | **Claude Code** |
|---|---|---|
| Where it lives | Claude Desktop, web, mobile, Chrome side panel | Terminal, or the Claude Code desktop app |
| Best at | Documents, drafts, research, briefs — work that ends in prose | Repos, code, git, precise file edits, running things |
| Your tools | Connectors | The same connectors, plus MCP servers you add locally |
| Sees every step | Summarised — you watch the outcome | Yes — every file read, every command, every diff |
| Git, branches, pull requests | Not what it's for | Yes — this is the reason to open it |
| Your phone | Yes | Via Claude Code on the web |
| Learning cost | None | One command, then it's a conversation |

**Rules of thumb for this kit:**

- **Filling in your capstone plan, adapting a recipe, drafting a stakeholder update,
  synthesising research → Cowork.** It's the natural home for everything in `0-capstone/`,
  `2-project-setup/`, `3-prompt-library/` and most of `5-automation-recipes/`. No terminal, and
  you can start a task from your phone and read the result over lunch.
- **Anything touching your SnapLedger repo — implementing a ticket, opening a pull request,
  the evals in `evals/` → Claude Code.** It's the one that can branch, commit and push.
- **Anything where you want to see exactly what it did → Claude Code.** When you're tuning a
  prompt and the output is wrong, watching each step is how you find out why.
- **Anything you'll want to run every morning → read
  `5-automation-recipes/scheduling.md` first.** Where it runs determines what it can reach.

**When in doubt, start in Cowork.** If you hit something it can't do, that thing is almost
always a repo operation, and that's your signal to open Claude Code in the same folder.

---

## Using both on the same folder

That's the intended design, not a workaround. The folder is the shared object: Cowork drafts
your Friday update into `my-system/`, and Claude Code commits it. Two things to know.

- **Don't run both against the same file at the same moment.** Nothing dramatic happens —
  one just overwrites the other's edit. Finish a task before you start the same one elsewhere.
- **Only Claude Code does git.** If you want a history of how your system evolved — and you
  will, by Week 4 — commit from Claude Code and let Cowork stay out of it.

---

## Where your own work goes

`my-system/`. It's gitignored, so your real board data, your meeting notes and your draft
updates never end up in a commit or a screenshot.

**Copy templates, don't fill them in.** `0-capstone/capstone-plan-template.md` stays a
template; your plan is `my-system/capstone-plan.md`. Ask either tool to do the copy for you —
both know this rule from `CLAUDE.md`.

---

## When something doesn't work

| Symptom | Usually |
|---|---|
| Connector returns nothing | Permissions, not the connector. Can you see the same data in the browser, signed in as that account? |
| Wrong project or space | Name it explicitly — "in project ABC", not "in Jira" |
| Claude Code can't see a connector | You signed in with an API key rather than your claude.ai account. Run `/login`. |
| Cowork can't see the folder | Set the project up in Claude Desktop on the machine the folder is on, and make sure the app is running |
| No **Cowork** option at all | Free plan, or an admin hasn't enabled it on Team/Enterprise |
| It edited a template instead of a copy | Tell it to revert and re-read `CLAUDE.md`. Then `git status` will show you what changed. |

Still stuck? Post it in the community space with what you typed and what came back. A specific
failure is worth more to everyone than a quiet retreat.
