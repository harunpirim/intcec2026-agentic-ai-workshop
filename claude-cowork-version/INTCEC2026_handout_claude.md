# Agentic AI as a System for Engineering Research
## Hands-On Handout (Claude Cowork edition) — INTCEC 2026, Chicago

**Requirements:** a laptop (macOS or Windows), the Claude desktop app from https://claude.ai/download, and a **paid Claude plan** (Pro $20/mo or higher — Cowork is included on all paid plans). No API keys, no notebooks, no other installs.

**No paid plan?** Pair with a neighbor — every exercise works two-to-a-screen. (Claude Code users: the same prompts work in a terminal session.)

---

## Before you start

1. Install the Claude desktop app and sign in.
2. Create an empty folder on your computer named `intcec-workshop`.
3. Open **Cowork** in the app and connect/select that folder — this is where Claude will save everything it makes.
4. **Warm-up prompt** (paste it; you're ready when Claude replies and a file appears in your folder):

> Create a file called hello.md in this folder containing one sentence about what an AI agent is. Then tell me what tools you have available in this session.

---

## Part A — Literature scan (10 min)

Paste, replacing the topic with **your own research area**:

> Do a mini literature review on **[YOUR TOPIC]**. Search for recent papers and preprints (2023–2026), select the 5 most relevant, and save a file `part-a-litreview.md` containing: (1) a table with columns Link | Year | Title | One-line contribution | Method type, and (2) a 5-sentence synthesis below it — what is the trend, and what gap remains? Cite only sources you actually found via search, with working links.

**Verify (this is the point):** click 2–3 links in the saved file. Real agents ground citations in live searches — every reference should resolve.

**Variations to try:** "only papers with real experimental data" · "organize by methodology" · "flag which papers share authors".

## Part B — Data analysis (12 min)

> Download the UCI Concrete Compressive Strength dataset (1,030 concrete mixes; if the download fails, generate a documented synthetic equivalent instead). Then, in a subfolder `part-b/`: profile the data, identify the 3 features most correlated with strength, fit a random-forest regressor with a train/test split (random_state=42) and report test R² and RMSE, and save a predicted-vs-actual figure with labeled axes (MPa). Save the analysis code you ran as a .py file and write a short report ending with a 3-sentence engineering interpretation.

While Claude works, watch the task list and tool calls — that visible plan-act-observe loop is the "agent loop" from the intro.

**Audit (before anything like this enters a paper):** open the saved `.py` file. Did you agree with the split, the metric, the model settings? Ask follow-ups:

> Justify the train/test split choice. Would results change materially with 5-fold CV? Run it and compare.

## Part C — Deliverable + the system view (10 min)

> Using `part-a-litreview.md` and the results in `part-b/`, write an IEEE-style Word document `part-c-draft.docx` with: a Related Work paragraph citing the reviewed papers (with links), a Preliminary Results paragraph reporting R² and RMSE, and two Future Work sentences. Formal tone, no hype.

Re-run with a different target: "grant proposal preliminary-data section" or "plain-language summary for a project sponsor" — same evidence, different rhetoric.

**Stretch — make it a system component:**

> Save this literature-review procedure as a reusable skill called `mini-lit-review`, so that in any future session I can ask you to run a mini literature review on a new topic and get the same table + synthesis format.

That's the difference between using an agent and building a system: captured, repeatable procedures.

---

## Responsible use checklist (before anything goes in a paper)

- [ ] Every citation has a working link I spot-checked.
- [ ] I read the code Claude executed (it's saved in my folder) and agree with its choices.
- [ ] The session's files, code, and figures are archived together (runs are stochastic).
- [ ] My venue's AI policy checked — IEEE requires disclosure of AI-generated text and bars AI authorship (verify current policy at submission).
- [ ] I checked my plan's data policy before sharing unpublished/sensitive data; Team/Enterprise plans offer stronger controls.

## Troubleshooting

| Symptom | Fix |
|---|---|
| Can't use Cowork | It requires a paid plan (Pro+) — pair with a neighbor for the session |
| Usage limit warning | Paid plans have session limits; pause between parts, or pair up |
| Dataset download blocked | The prompt already covers it — Claude generates a documented synthetic equivalent |
| Claude asks permission a lot | Normal: it requests access per folder/action — approve for the workshop folder |
| A long step seems stuck | Cowork tasks legitimately run for minutes; check the task list before interrupting |
| Windows install issues | Requires Windows 10 v1909+ / 11 with Hyper-V enabled |

## Take it home

- Docs: https://docs.claude.com (skills, connectors/MCP, Claude Code)
- Your workshop folder is a complete, portable record: data, code, figures, drafts.
- Connect your real tools next: Drive, GitHub, reference managers, lab databases via MCP connectors.
- Prefer free/open-source? Ask for the companion version of this workshop (smolagents + Colab).

*Questions after the conference: Harun Pirim — 1p1r1m1@gmail.com*
