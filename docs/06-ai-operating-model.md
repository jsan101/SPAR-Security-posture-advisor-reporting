# AI Operating Model

The practice is AI-orchestrated and human-governed. The principle, stated once:

> **A claim about the outside world needs a frontier model. A claim about a file does not.** And no claim about a number comes from a model at all.

---

## Who does what

| Work | Done by | Why |
|---|---|---|
| Every count, share, score, lifecycle bucket, and reconciliation | **Deterministic scripts** | Arithmetic never degrades and never depends on a model |
| Threat correlation, ATT&CK mapping, outside-in exposure, chain-stage assessment | **Frontier model** | Judgment about the outside world, with consequences if wrong; HITL verification |
| Adjudicating ambiguous evidence; choosing and ordering storylines; executive-summary headlines | **Frontier model**, then human approval | Decides what the client hears first |
| Running scripts, pulling case records, building deliverables, visual QA, tone review, writing back to memory | **Lighter model** | The content is already fixed by the time these steps see it |
| Storyline selection, suppressions that could mask real signal, contradiction calls, major-incident scope notes, delivery | **Human** | Kept by the advisor in every mode |

**The rule that makes the split safe:** a lighter-model step never authors a citation, an attribution, an ATT&CK mapping, or an exposure finding. It may transcribe one a frontier step produced and the human approved. If it needs a source it doesn't have, it **stops and reports the gap**. It does not reach for a plausible-looking vendor page.

The tone reviewer follows the same rule. If a wording change would touch a citation, attribution, mapping, exposure finding, or executive headline, it goes back to the step that wrote it.

---

## Execution waves

| Wave | Runs in parallel | ~Minutes |
|---|---|---|
| 0 · Gate and ask | Tier check; one intake packet to the advisor; memory prep | 5–10 |
| 1 · Fan-out | All scripts ‖ case-record pull ‖ exposure pass ‖ industry landscape | 15–20 |
| 2 · Judgment | Adjudication ‖ storyline correlation and chain stage; then the posture score | 10–15 |
| 3 · Gate | One content pack assembled; **one human approval** | 5–10 |
| 4 · Build | Deck ‖ written record and spreadsheet, all from the approved pack | 10–15 |
| 5 · QA and close | Visual QA ‖ tone review; fixes; memory write-back; export; validator | 10–15 |

Wave 0 exists because a background step cannot ask the advisor a question, so everything that needs a person happens before the work fans out. Builds can run in parallel only because the content pack is frozen first; three builders reading one approved file produce matching deliverables.

**An hour is a target. The gates are the specification.** If a wave overruns, the cycle takes longer. The human approval point is never what gets dropped.

---

## Operating modes

| Mode | Condition | Estimated time per cycle |
|---|---|---|
| **A: Full delegation** | Frontier-class AI that passes a calibration test | 1.5–3 hours |
| **A-R: Routed** | Lighter model orchestrating, frontier model for intelligence steps | About 1 hour (target) |
| **B: Assisted** | Lighter model only; the advisor drives step by step and verifies every citation | 3–5 hours |
| **C: Manual** | No AI; the advisor plus the scripts and template builds | 6–9 hours at first, 4–6 with practice |

**Degradation rule:** the mode is set by the weakest link you'd have to trust blindly. A model that invents one citation or miscomputes one score component drops to assisted duties for the rest of the cycle. In routed mode, an orchestrator that absorbs an intelligence step instead of delegating it drops the whole cycle to assisted mode, because the routing *is* the safety argument.

**New models** take a calibration test before running a live cycle. The specification, the client memory files, and the scripts are the practice; models and tools are replaceable parts on top of it.
