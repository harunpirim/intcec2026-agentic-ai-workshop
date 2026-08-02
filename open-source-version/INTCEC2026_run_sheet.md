# Facilitator Run Sheet — INTCEC 2026 Workshop
## "Agentic AI as a System for Engineering Research" · 60 minutes

### Two weeks before
- [ ] Upload notebook to GitHub or Drive; create the Colab share link; make the short link (bit.ly or tinyurl); **update slide 11 and the handout** with the real link.
- [ ] Do a full dry run in a fresh Colab with a fresh Gemini key — time each part.
- [ ] Send the pre-workshop email to registrants (see `INTCEC2026_preworkshop_email.md`).
- [ ] Ask the organizers: projector aspect ratio, Wi-Fi reliability, room layout, whether you can recruit 1–2 helpers.

### Day before / morning of
- [ ] Re-run the notebook end-to-end (APIs and library versions can shift).
- [ ] Create a **spare Gemini key + spare Groq key** for attendees whose sign-up fails.
- [ ] Print ~30 handouts (or QR-code the markdown/PDF).
- [ ] Phone hotspot charged as Wi-Fi backup for YOUR demo machine.
- [ ] Pre-open tabs: slides, Colab (already run once so outputs are visible), aistudio.google.com/apikey.

---

## Minute-by-minute

| Clock | Segment | Notes |
|---|---|---|
| **0:00–0:02** | Welcome, who's in the room | Quick hands: who has used ChatGPT? Claude Code/Copilot? Built an agent? Calibrates your pace. |
| 0:02–0:05 | Slides 2–4: chatbots → agents, the loop | Land the one-liner: *agent = LLM + tools + memory in a loop.* |
| 0:05–0:09 | Slides 5–6: landscape, frameworks | Tool-agnostic framing; why smolagents today (setup speed, readable code). |
| 0:09–0:12 | Slide 7: the system view | This is the thesis slide. Human verification is a pipeline stage. |
| 0:12–0:16 | Slides 8–9: strengths, failures, responsible use | Faculty engage most here; hold questions to 1–2. |
| 0:16–0:18 | Slide 10: what we'll build | Set expectations: pre-built notebook, run then modify. |
| **0:18–0:20** | Slide 11 up: setup begins | Helpers circulate. Anyone without a key gets your spare. |
| **0:20–0:25** | Setup check | Everyone runs install + key + sanity cells. Checkpoint: "thumbs up when the model answered." Stragglers pair with a neighbor — don't stall the room. |
| 0:25–0:35 | **Part A: literature agent** | Run as-is (2 min), then they switch to their own topic (5 min), verify one arXiv ID live on screen (1 min). Checkpoint: ask 2 people what topic they tried. |
| 0:35–0:47 | **Part B: data agent** | Run (3–4 min inference). While it runs, narrate the step logs — *this is the audit trail.* Then free-form questions on the dataset. Checkpoint: someone shares an R² value. |
| 0:47–0:57 | **Part C: writing agent + stretch** | Run drafting cell; discuss how outputs of A+B became inputs. Fast attendees run the manager-agent stretch. |
| 0:57–1:00 | Wrap: responsible-use checklist, slide 13 | Point to handout links; offer to share materials; invite emails. |

## Contingency plans

| Risk | Plan |
|---|---|
| Conference Wi-Fi dies | Your hotspot + demo-led mode: you drive, attendees watch; they re-do it at home with the handout. |
| Gemini free tier throttles the room | Switch PROVIDER to Groq (one-line change, in the notebook and handout). |
| >50% attendees didn't pre-register keys | Do Part A demo-led while helpers get keys issued; compress Part B to one question; keep Part C. |
| Running 10 min behind at 0:35 | Cut Part B "your turn" block; jump to Part C at 0:45 — the pipeline story needs A + C minimum. |
| Projector fails | Notebook markdown cells are self-explanatory; run it as a guided lab from the handout. |

## Timing philosophy
Part boundaries are hard sync points; "your turn" blocks are the flex. A straggler who skips an exercise stays synchronized at the next boundary. Never debug one attendee's laptop for more than 60 seconds — hand them to a helper or a neighbor.
