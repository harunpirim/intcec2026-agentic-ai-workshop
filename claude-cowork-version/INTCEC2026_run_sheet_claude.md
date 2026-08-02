# Facilitator Run Sheet (Claude Cowork edition) — INTCEC 2026
## "Agentic AI as a System for Engineering Research" · 60 minutes

### Two weeks before
- [ ] Full dry run in a fresh `intcec-workshop` folder with a clean Cowork session — time each part, save the outputs as your reference set.
- [ ] Send the pre-workshop email (see `INTCEC2026_preworkshop_email_claude.md`) — the paid-plan requirement MUST reach attendees early; it's the #1 risk in this format.
- [ ] Print ~30 handouts (attendees paste prompts from it — paper works better than switching windows).
- [ ] Ask organizers about Wi-Fi reliability and whether you can recruit 1–2 helpers.

### Day before / morning of
- [ ] Re-run the full pipeline once (product UIs change; your screenshots/expectations should match current Cowork).
- [ ] Your demo machine: signed in, workshop folder connected, warm-up already run once so a completed example is on screen.
- [ ] Phone hotspot charged as backup for YOUR demo machine.
- [ ] Have the open-source (Colab) version's link ready as a fallback for attendees without paid plans who don't want to pair.

---

## Minute-by-minute

| Clock | Segment | Notes |
|---|---|---|
| **0:00–0:02** | Welcome, who's in the room | Hands: who uses Claude/ChatGPT? Who has Cowork or Claude Code installed? Counts your pairing needs. |
| 0:02–0:05 | Slides 2–4: chatbots → agents, the loop | One-liner to retain: *agent = LLM + tools + memory in a loop.* |
| 0:05–0:09 | Slides 5–6: landscape, the Claude stack | Tool-agnostic honesty: same loop everywhere; today's route = zero plumbing. |
| 0:09–0:12 | Slide 7: the system view | Thesis slide. One session, one folder, four stages, human verifies at each hand-off. |
| 0:12–0:16 | Slides 8–9: strengths, failures, responsible use | Faculty engage here; take 1–2 questions max. |
| 0:16–0:18 | Slide 10: what we'll build | Real files in their folder — set that expectation explicitly. |
| **0:18–0:20** | Slide 11 up: setup begins | Pair anyone without a paid plan now, not later. |
| **0:20–0:25** | Warm-up check | Everyone's Claude created `hello.md`. Checkpoint: thumbs up. Permission dialogs are normal — say so preemptively. |
| 0:25–0:35 | **Part A: literature scan** | They paste, personalize topic. While agents run: narrate YOUR run's tool calls on screen. Checkpoint: two people share their topic + one clicked link. |
| 0:35–0:47 | **Part B: data analysis** | Longest waits here — use them: walk through the saved `.py` from your reference run, discuss the audit habit. Checkpoint: someone reads out their R². |
| 0:47–0:57 | **Part C: Word draft + stretch** | The .docx opening on their machine is the payoff moment. Fast tables run the make-it-a-skill stretch. |
| 0:57–1:00 | Wrap: checklist, slide 13 | Folder = portable record. Offer both workshop versions' materials. |

## Contingency plans

| Risk | Plan |
|---|---|
| Many attendees lack paid plans | Pair up (planned-for); worst case switch those attendees to the Colab open-source version link |
| Conference Wi-Fi dies | Hotspot + demo-led: you drive, attendees re-do at home from the handout |
| Usage limits hit mid-session | Stagger: half the room starts Part B while half discusses Part A audit questions |
| Dataset download blocked on venue network | Prompt already instructs Claude to generate a documented synthetic equivalent |
| Product UI changed since dry run | You re-ran it the day before — narrate differences; concepts are UI-stable |
| Projector fails | Handout is self-contained; run as a guided lab |

## Timing philosophy
Cowork steps run for minutes — that waiting time is teaching time (audit discussion, questions), not dead air. Part boundaries are hard sync points. Never debug one attendee's machine >60 s; hand to a helper or pair them.
