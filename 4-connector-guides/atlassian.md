# Atlassian — Jira and Confluence

The spine of Week 3. Read the board, cross-check the PRD, write stories back.

## Setup

1. Accept the invite to the cohort instance (or use your own work account).
2. Claude Desktop → **Settings → Connectors → Atlassian** → sign in with that account.
3. Approve the scopes. Read access is enough to start; you need write for the story-creation
   exercise.

## Verify it works

```
Using the Atlassian connector, what issues are in [YOUR PROJECT KEY]?
```

If that returns your project, you're done. If it returns nothing, check you're signed in with
the account the invite went to.

## Things worth knowing

- **Name the project explicitly.** "In PROJECT-KEY" beats "in Jira" every time.
- **Boards are views, projects are containers.** Your sandbox is a project — nothing you do
  there touches anyone else's work.
- **Writes are real.** A created ticket is a created ticket. Draft first, review, then create.
- **Confluence pages** can be read and written the same way. Ask it to cite the page it used.

## Useful first questions

```
What's blocking the current sprint in [PROJECT]?
Which stories in [PROJECT] have no acceptance criteria?
Does the PRD in [SPACE] cover the top three complaints in my synthesis?
```
