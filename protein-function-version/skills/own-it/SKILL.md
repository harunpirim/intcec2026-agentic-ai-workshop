---
name: own-it
description: Interview a researcher about an experiment before any execution until every decision is theirs. Use before starting a research task, when the user says "own it", "interview me", "grill me", or "before we start".
---

Interview the researcher until the plan is theirs, then write it down. Do not run, edit, or plan code until they confirm.

## How to ask

- **Use the harness's question tool if it has one** (Claude Code `AskUserQuestion`, the bb question panel, Codex `request_user_input`, or similar). One call per round with every question of the round in it. Each question gets options, your recommendation first and marked "(Recommended)". Without such a tool, ask in chat, numbered, each with a recommendation.
- **Two rounds at most, six questions at most per round.** Ask only what changes the plan. Anything with a defensible default, decide yourself and list under "Defaults I chose"; the researcher can strike any.
- **Facts are your job.** Read the repository before asking. Never ask what you can look up.
- **Recommend the simplest option that answers the question.** Name the cost of the fancier one in a clause, not a paragraph.
- **If a whole round comes back "as recommended", stop asking** and write the plan.
- **Never run `git commit`.** The researcher commits.

## What must be settled, by question or by default

Question. Hypothesis and what would count against it. Data and split. Baseline. Metric. The one change. The one follow-up check to run after the main result, chosen from the README's list. Scope of edits. Budget and stopping rule. What "improves" means. What gets written back if the result is positive, negative, or mixed.

## Finish

Write `PLAN.md` at the repository root, twenty lines or fewer: one line per item above, then "Defaults I chose", then "Open". Ask the researcher to read it and commit it. Execution starts only after that commit. `sign-it` checks the result against this file.
