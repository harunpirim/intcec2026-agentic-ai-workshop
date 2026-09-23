---
title: "Hands-on handout: own the work"
event: INTCEC 2026, Chicago
duration: 40 minutes
updated: 2026-09-22
---

# Hands-on handout: own the work

You will direct a coding agent through one bounded experiment, then sign the result or decline to. The agent does the work. You make every decision and every commit.

**Bring:** a laptop with `git`, `uv`, and one agent harness installed and signed in: Claude Code, Codex, or pi. Details in the pre-workshop email. No harness? Pair with a neighbor; every step works two to a screen.

## Before we start (done at home, checked at minute 20)

```
git clone https://github.com/yusuf8834/go-imbalance-sprint go-imbalance-sprint
cd go-imbalance-sprint
uv sync
uv run python -m gosprint.baseline
uv run pytest -q
```

You are ready when the baseline prints micro F1 near 0.73 and all tests pass. Then open your harness **in that directory** and ask:

> which skills do you have?

It should name **own-it** and **sign-it**. If it does not, paste the contents of `skills/own-it/SKILL.md` as your first message and say "this is the own-it skill". Same later for `skills/sign-it/SKILL.md`.

## The task, in one paragraph

A model predicts Gene Ontology terms for bacterial proteins. Some terms have over a thousand training examples, some fewer than twenty, and the model treats them all alike, so it learns rare functions as "almost never." A reviewer writes: *class imbalance handling is completely missing.* Apply the standard remedy, balanced class weights, and decide what you would write back. Full statement in the repository README.

## Block 1, own it (minutes 23 to 30)

Say:

> Run own-it. The task is in README.md.

Questions arrive in your harness's question panel, each with a recommended answer. Answer as yourself. Push back at least once; the recommendation is a starting point, not the answer. The one that matters most: **which number decides whether balanced weights helped**, micro F1, macro F1, or rare-term F1. They will disagree. Your choice, made now, decides the verdict later.

When `PLAN.md` appears, read all twenty lines. Strike anything you do not agree with. Then commit it yourself:

```
git add PLAN.md
git commit -m "Plan: balanced class weights, decided by <your metric>"
```

The agent will not start until this commit exists. That is by design.

## Block 2, execute (minutes 30 to 44)

Say:

> Carry out PLAN.md. Train the balanced model into results/balanced/, run the follow-up check, and build results/balanced/report.html comparing baseline and balanced with precision and recall shown, not only F1.

While it works, watch for four things:

- Does it read anything it should not? Test labels are for the final evaluation only.
- Does it quote a number that is not in a file under `results/`?
- Does it try to commit? It must not.
- Does something fail, and how does it recover?

When it stops, review before you accept:

```
git status
git diff --stat
uv run pytest -q
open results/balanced/report.html
```

Commit when satisfied, and only then:

```
git add -A
git commit -m "Balanced class weights: results, follow-up check, report"
```

The work is now frozen. Nothing else gets computed.

## Block 3, sign it (minutes 44 to 55)

Say:

> Run sign-it.

At most ten items arrive, each with its source file and four answers: **accept, qualify, reject, don't know.** For each, open the file it names if you have any doubt. Qualify in your own words. Reject if the claim says more than the file supports. "Don't know" is an answer; it stays open.

When `results/SIGNOFF.md` appears, read the paragraph headed "What the signer asserts." If you would not put your name under it, do not. Commit it either way:

```
git add results/SIGNOFF.md
git commit -m "Sign-off: <signed | not signed>"
```

## Debrief (minutes 55 to 60)

Be ready to say one sentence you would write back to the reviewer, and which metric you named before running.

## Rules the agent follows in this directory

Never commits. Fits on the training split only. Quotes numbers from files. Edits only `src/`, `tests/`, and `results/`. Stays inside the directory. Ten minutes of compute. The full list is in `AGENTS.md`.

## Troubleshooting

| Symptom | Fix |
|---|---|
| Skills not found | Paste `skills/own-it/SKILL.md` as your first message; later `skills/sign-it/SKILL.md` |
| `uv sync` fails | Python 3.11 or newer is needed; `uv python install 3.12` then retry |
| Baseline prints a different F1 | Check `git status` is clean and `git log` shows the `baseline` tag; reclone if not |
| Agent starts before you committed the plan | Stop it. Say "wait for my commit." Commit. Say "go." |
| Agent asks to commit | Say no. You commit. |
| Harness has no question panel | Answers go in chat; the skill numbers its questions |
| No harness, no plan, no key | Pair. The person with the keyboard decides; the other one reads the files |

## Take home

The repository is yours. The two skills are plain text; copy them into any project. Try the sprint again with a local model and see where it breaks. Try rejecting something.
