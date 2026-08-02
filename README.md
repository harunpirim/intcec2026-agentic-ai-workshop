# INTCEC 2026 Workshop — Agentic AI as a System for Engineering Research

Two complete, parallel versions of the same 60-minute workshop (20 min intro + 40 min hands-on). Same concepts, same three-stage pipeline (literature → data analysis → drafting), different hands-on stack.

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

## Choosing (or hedging)
Run open-source if you want zero cost-of-entry for attendees; run Cowork if you want the fastest setup and tangible file deliverables. The run sheets cross-reference each other as fallbacks — you can bring both and decide per-attendee.

Before the conference (either version): do a full dry run ~2 weeks out and again the day before; the Colab link is baked in; re-verify it opens after any repo rename.
