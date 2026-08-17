# Other connectors worth having

## Google Workspace (Calendar, Drive, Gmail)

**Why:** Calendar is the quiet upgrade. It turns a brief from "here's what happened" into
"here's what's coming at you today". Drive gives Claude your actual documents.

**Friction:** near zero. No admin approval for personal use.

**Try:** `What's on my calendar this week that I'm unprepared for?`

---

## Notion

**Why:** if your specs, notes or second brain live there, this is where your context is.

**Try:** `Find everything we've written about [FEATURE] and tell me what's contradictory.`

---

## Linear

**Why:** the Jira alternative at most startups, with an excellent MCP server. Every prompt in
this kit that says "Atlassian" works with Linear — swap the source line.

---

## Slack

**Why:** where feedback and decisions actually live. Mining a feedback channel for themes is
genuinely powerful.

**Friction:** usually needs workspace-admin approval. Ask early, and use
`governance.md` to answer the questions they'll have.

**Try:** `Read #customer-feedback from the last month and group it into themes with counts.`

---

## Analytics (PostHog, Mixpanel, Amplitude)

**Why:** once your product is live and instrumented, the same pattern applies to product data.
Not part of this cohort — there's nothing shipped to measure yet — but the moment you have
something in production, this is the next connector to add.
