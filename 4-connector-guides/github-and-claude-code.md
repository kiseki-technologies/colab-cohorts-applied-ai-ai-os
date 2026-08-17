# GitHub and Claude Code

Two separate things that people conflate, so let's be precise.

- **The GitHub connector in Claude Desktop** lets Claude read repos, issues and PRs in chat.
- **Claude Code** is Claude in your terminal, working on files directly. It configures its own
  MCP servers — **it does not inherit Claude Desktop's connectors.**

That second point is the one that surprises everyone.

---

## Setup

**1. Claude Code**

Install from `claude.com/claude-code` and sign in with your existing Claude account.
Run it once in any folder to confirm it works.

**2. The GitHub CLI**

Install `gh` from `cli.github.com`, then:

```
gh auth login
```

Follow the browser flow. This is what lets Claude Code push branches and open pull requests
without a credentials fight later. **Do this before the session** — it's the classic time sink.

**3. MCP inside Claude Code**

A repository can ship its own MCP configuration, so cloning it gives Claude Code access to the
tools that project needs. The cohort template repo does exactly this for Jira — when you first
run Claude Code in it, approve the server it offers and you're connected.

If you're setting this up in your own repo later, `claude mcp` is the command to explore.

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

## Reviewing a PR when you don't write code

You don't need to read every line. You need to answer three questions:

1. **Does it do what the ticket asked?** Compare the PR description against your acceptance
   criteria.
2. **What did it decide that the ticket didn't cover?** Ask it directly — it will tell you.
3. **What did it flag as ambiguous?** That's feedback on your writing, not its work.
