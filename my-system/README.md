# my-system — your work goes here

Everything in the numbered folders is a template. **This is where your version lives.**

This folder is gitignored apart from this file, so your real board data, meeting notes and
draft updates never land in a commit or a screenshot. That matters more than it sounds — the
outputs of a working system are exactly the material you'd least like to share by accident.

## What ends up in here

```
my-system/
  capstone-plan.md          your copy of 0-capstone/capstone-plan-template.md
  standing-instructions.md  your copy of 2-project-setup/project-standing-instructions.md
  standup-brief.md          appended to by your morning automation
  proposed-tickets.md       drafts waiting for your approval
  updates/                  weekly stakeholder update drafts
  feedback-themes/          one file per week
```

Nothing here is required. It's the shape most people's folder ends up in by Week 4.

## Getting started

Ask Claude Code or Cowork:

```
Copy the capstone plan template into my-system/ and help me fill in section 1.
```

Either tool knows from `CLAUDE.md` to copy rather than edit the original.

## If you want to keep a history

Your outputs are ignored by git on purpose. If you'd rather version your own system — and by
Week 4 you'll want to see how the prompts evolved — the plans and instructions are the parts
worth tracking:

```
git add -f my-system/capstone-plan.md my-system/standing-instructions.md
```

Force-add the documents. Leave the automation outputs ignored.
