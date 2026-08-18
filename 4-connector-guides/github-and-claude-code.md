# GitHub, Claude Code and Cowork

Three things that people conflate, so let's be precise.

- **Connectors** are the integrations on your Claude account — Atlassian, Granola, Google,
  Slack. You add them once at `claude.ai/customize/connectors`.
- **Cowork** is Claude working on your files and your connected tools without a terminal, in
  Claude Desktop, on the web, or on your phone.
- **Claude Code** is Claude in your terminal (or its own desktop app), working on files
  directly, and the only one of the three that does git.

**Your connectors are shared.** Connect Atlassian once on your Claude account and both Cowork
and Claude Code can use it — Claude Code picks up the connectors from the claude.ai account
you signed in with. Run `/mcp` inside Claude Code to see the list. Claude Code can *also* add
MCP servers of its own that live only on your machine; those are the ones Cowork won't see.

That's the direction of the arrow: **account connectors flow everywhere; local MCP servers
stay local.**

---

## Setup

**1. Claude Code**

Install from `claude.com/claude-code` and sign in with your existing Claude account.
Run it once in any folder to confirm it works. Sign in with your claude.ai account, not an API
key — an API key gets you the tool without your connectors.

**2. The GitHub CLI**

Install `gh` from `cli.github.com`, then:

```
gh auth login
```

Follow the browser flow. This is what lets Claude Code push branches and open pull requests
without a credentials fight later. **Do this before the session** — it's the classic time sink.

**3. MCP inside Claude Code**

Most of what you need is already there through your account connectors. Beyond that, a
repository can ship its own MCP configuration in a committed `.mcp.json`, so cloning it gives
Claude Code access to the tools that project needs — you'll be asked to approve the server the
first time you run Claude Code in that folder.

`claude mcp list` shows what's configured and whether it connected. `claude mcp add` is the
command to explore when you're setting this up in your own repo later.

---

## The Week 3 flow

```
1. Create your repo from the template (GitHub → Use this template)
2. Clone it, open a terminal in the folder, run: claude
3. Ask it to read your ticket from Jira and implement it
4. Ask it to commit on a branch and open a pull request
5. Read the diff. Read what it says was ambiguous in your ticket.
```

Step 5 is the actual lesson. The code is the by-product.

---

## Which one for which job

| Job | Tool |
|---|---|
| Draft the PRD, the stories, the update | Cowork |
| Put the stories on the board | Either — both have the Atlassian connector |
| Implement a ticket in a repo | Claude Code |
| Open a pull request | Claude Code |
| Review the PR description against your acceptance criteria | Either |
| Run something every weekday morning | See `5-automation-recipes/scheduling.md` |

`SETUP.md` in the root of this kit has the full comparison.

---

## Reviewing a PR when you don't write code

You don't need to read every line. You need to answer three questions:

1. **Does it do what the ticket asked?** Compare the PR description against your acceptance
   criteria.
2. **What did it decide that the ticket didn't cover?** Ask it directly — it will tell you.
3. **What did it flag as ambiguous?** That's feedback on your writing, not its work.
