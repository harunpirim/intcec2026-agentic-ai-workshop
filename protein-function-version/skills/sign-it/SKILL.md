---
name: sign-it
description: Final step before work is submitted. Walk the researcher through the few decisions, claims, and contradictions they must stand behind, so they sign knowingly. Use when the user says "sign it", "sign off", or is about to commit, submit, or send results.
---

The researcher is about to put their name on this. They need the few things they would have to defend, not everything you did. You surface those, record their answers, and never sign for them.

## 1. Collect, silently

Read `PLAN.md`, `git log` and `git diff` from the baseline tag, `results/`, the tests, and any report. Extract, then **cut to at most ten items**, most consequential first:

- **Claims** that appear in the conclusion or the reply, each with its file and number.
- **Decisions the agent made**, or that departed from `PLAN.md`. Not the researcher's own decisions; they made them.
- **Contradictions**: numbers, text, code, or plan disagreeing. Always included.
- **Unverified**: anything stated without a file behind it.

Merge related items into one line. If an item would not change what the researcher writes back, drop it. Do not show the collection; show the questions.

## 2. Ask

Interview by default. **Use the harness's question tool if it has one**: one item per question, three lines at most (the item, its source, why it matters), options **accept / qualify / reject / don't know**. Batch trivial items into one question. Without such a tool, ask in chat, one item at a time.

Report mode only if the researcher asks: one self-contained HTML page, ten lines or fewer, each with a source link and the four options. Deliver it and wait.

Do not argue. Do not praise. Record answers in the researcher's words.

## 3. Verdict

Write `SIGNOFF.md` next to the results, one page: date, signer, thesis, one line per item with its answer, open items, and one paragraph of what the signer asserts.

If any consequential item is rejected, unknown, or contradicted, say **not ready to sign** and what would make it ready, one line each. If the researcher chooses to leave it unsigned, record that. It is a valid outcome.

## Rules

Numbers come from files. "The agent said so" is not evidence. Never run `git commit`. The researcher signs; you record.
