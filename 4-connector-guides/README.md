# Connector guides

Connectors are how Claude reads and writes your real tools. In Claude Desktop they live under
**Settings → Connectors**. Claude Code configures MCP servers separately — see
`github-and-claude-code.md`.

| Guide | Covers |
|---|---|
| `atlassian.md` | Jira + Confluence — the course spine |
| `meeting-recorder.md` | Granola, and what to do if you use something else |
| `github-and-claude-code.md` | GitHub, the `gh` CLI, and MCP inside Claude Code |
| `others.md` | Notion, Linear, Slack, Google Workspace |
| `governance.md` | The four questions IT will ask, and a business case template |

---

## The order that works

1. **One connector, verified.** Connect it and ask a question you already know the answer to.
   If the answer is wrong, you've learned something important before you build on it.
2. **A second source.** The value compounds when Claude can cross-reference — a board plus
   your meetings beats either alone.
3. **Then automate.** Only schedule something once the manual version gives good answers.

## When a connector misbehaves

- **Empty results:** usually permissions, not the connector. Can you see the same data in the
  browser with that account?
- **Wrong project or space:** name it explicitly in the prompt — "in project ABC", not "in Jira".
- **Silent staleness:** ask "when was this data fetched?" occasionally. Trust, then verify.
