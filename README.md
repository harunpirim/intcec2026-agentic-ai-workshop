# INTCEC 2026 Workshop — Agentic AI as a System for Engineering Research

Three versions of the same 60-minute workshop (20 min intro + 40 min hands-on). The first two share a three-stage pipeline (literature → data analysis → drafting) with different hands-on stacks. The third is a research sprint on a prepared repository: one bounded experiment, directed by the participant, signed at the end.

## `open-source-version/`
Hands-on in **Google Colab + smolagents** with a free Gemini or Groq API key.

- Free for attendees; nothing installed; provider-agnostic and fully inspectable code
- Requires: browser, Google account, free API key (pre-workshop email covers it)
- Files: slides (pptx), Colab notebook (ipynb), handout, run sheet, pre-workshop email
- **[Open the notebook in Colab](https://colab.research.google.com/github/harunpirim/intcec2026-agentic-ai-workshop/blob/main/open-source-version/INTCEC2026_agentic_ai_workshop.ipynb)**
- Known friction (all handled in the materials): API key paste errors, Gemini model retirements/billing quirks, arXiv throttling (auto-falls back to OpenAlex)

## `claude-cowork-version/`
Hands-on in **Claude Cowork** (desktop app; Claude Code works too).

- Zero plumbing: no API keys or notebooks; outputs are real files (docx, figures, code)
- Requires: Claude desktop app + any paid Claude plan (Pro+); pairing is the fallback
- Files: slides (pptx), handout with copy-paste prompts, run sheet, pre-workshop email

## `protein-function-version/`
Hands-on as a **research sprint** in the participant's own coding-agent harness (Claude Code, Codex, or pi).

- A reviewer's point about a protein-function prediction model, stated hypothetically: class imbalance handling is missing. The participant applies one change, balanced class weights, names the deciding metric before running, and signs the result or declines to.
- Two skills frame the sprint: `own-it` interviews the participant into a twenty-line `PLAN.md` before anything runs; `sign-it` puts at most ten claims, decisions, and contradictions in front of them at the end. The agent never commits; the participant does.
- Requires: laptop with `git`, `uv`, and one harness signed in; pairing is the fallback
- Files: slides (Markdown), handout, the two skills
- The prepared repository participants clone is separate: **[go-imbalance-sprint](https://github.com/yusuf8834/go-imbalance-sprint)**. An agent opened inside it sees only the sprint, never this repository.

## Choosing
Run open-source for zero cost of entry; Cowork for the fastest setup and tangible file deliverables; the research sprint for a room that already uses coding agents and wants to practice owning the result. The first two run sheets cross-reference each other as fallbacks.

Before the conference (any version): do a full dry run ~2 weeks out and again the day before. For the open-source version, re-verify the Colab link opens after any repo rename. For the sprint, run it yourself from a fresh clone first.
