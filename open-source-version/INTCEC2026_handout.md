# Agentic AI as a System for Engineering Research
## Hands-On Handout — INTCEC 2026, Chicago

**Notebook:** [Open in Colab](https://colab.research.google.com/github/harunpirim/intcec2026-agentic-ai-workshop/blob/main/open-source-version/INTCEC2026_agentic_ai_workshop.ipynb)  ·  repo: https://github.com/harunpirim/intcec2026-agentic-ai-workshop
**Requirements:** a laptop with any browser, a Google account, and a free API key (below). Nothing is installed on your machine.

---

## Before you start (do this before the session if possible)

1. **Get a free API key** — no credit card:
   - Recommended: Google AI Studio → https://aistudio.google.com/apikey → "Create API key" → copy it somewhere safe.
   - Backup: Groq → https://console.groq.com/keys → "Create API Key".
2. **Open the notebook link** above and choose *File → Save a copy in Drive* so you can edit and keep it.
3. **Run the first two cells** (install + key entry). If the model check cell prints a sentence, you are ready.

**Key safety:** treat the API key like a password. Don't share it or commit it to GitHub. You can delete/regenerate it after the workshop.

---

## Part A — Literature review agent (10 min)

The agent has one tool: a live literature search (arXiv, with automatic OpenAlex fallback). It plans queries, reads results, and synthesizes — and every citation is a real arXiv ID or DOI you can check.

1. Run the tool-definition cell, then the agent cell as-is.
2. **Edit `RESEARCH_TOPIC` to your own research area** and re-run.
3. Verify one result: open `arxiv.org/abs/<ID>` (or `doi.org/<DOI>`) for any row of the table.

**Prompt ideas to try:**

- "…only include papers that use real experimental data."
- "…organize the table by methodology instead of date."
- "…identify which papers share authors or build on each other."

## Part B — Data analysis agent (12 min)

A `CodeAgent` writes and executes pandas/scikit-learn code on the UCI Concrete Compressive Strength dataset (1,030 mixes, 8 features).

1. Run the data-loading cell, then the analysis cell.
2. **Read the step logs** — the agent prints every line of code it ran. This is your audit trail.
3. Ask your own question of the data, e.g.:
   - "What water/cement ratio maximizes 28-day strength? Support with a plot."
   - "Is fly ash an effective partial cement replacement here? Quantify."
   - "Compare a linear model to the random forest — is the extra complexity justified?"

## Part C — Writing agent + the system view (10 min)

The writing agent receives Part A's review and Part B's results and drafts Related Work + Preliminary Results + Future Work.

1. Run the drafting cell.
2. Re-run with a different rhetorical target: grant proposal, sponsor summary, thesis chapter.
3. **Stretch:** run the manager-agent cell — one agent delegating to another (`managed_agents`). This is the pattern that scales to real research pipelines.

---

## Responsible use checklist (before anything goes in a paper)

- [ ] Every citation came from a live database call, and I spot-checked them.
- [ ] I read the code the agent executed and agree with its methodological choices.
- [ ] Versions pinned, seeds set, agent logs saved (runs are stochastic).
- [ ] My venue's AI policy checked — IEEE requires disclosure of AI-generated text and bars AI authorship (verify current policy at submission).
- [ ] No unpublished/sensitive data sent to a free API tier. (For sensitive work: run a local model with Ollama — same code, swap the model line.)

## Troubleshooting

| Symptom | Fix |
|---|---|
| `401 / invalid key` | Re-paste the key (no spaces); confirm PROVIDER matches the key you got |
| `'ascii' codec can't encode` | Your paste grabbed extra text around the key — use the copy button on the key page, re-run the key cell |
| `429 / rate limit` | Wait ~60 s; free tiers throttle. Or switch PROVIDER to your backup key |
| `429 "prepayment credits are depleted"` | Not a rate limit — that Google project has no free quota (billing-attached account). Switch PROVIDER to "groq", or create the key under a free-tier project at ai.studio/projects |
| `404 "model no longer available"` | Google retires model versions — run the model-list cell in the notebook and set MODEL_ID to any listed model |
| Install cell fails | Runtime → Restart runtime, run cells again from the top |
| arXiv tool returns nothing | Broaden the query; arXiv search is keyword-based |
| arXiv `HTTP 429` message | arXiv throttles shared Colab IPs; the tool auto-retries — if it still reports 429, wait ~30 s and re-run |
| Dataset download fails | The notebook auto-generates a synthetic fallback — keep going |
| Agent loops without finishing | Interrupt (⏹), lower `max_steps`, make the prompt more specific |

## Take it home

- smolagents docs: https://huggingface.co/docs/smolagents
- LangGraph: https://langchain-ai.github.io/langgraph/ · CrewAI: https://docs.crewai.com · AutoGen: https://microsoft.github.io/autogen/
- Local & private: https://ollama.com
- The notebook is yours (you saved a copy in Drive) — swap in your data, your topics, your model.

*Questions after the conference: Harun Pirim — 1p1r1m1@gmail.com*
