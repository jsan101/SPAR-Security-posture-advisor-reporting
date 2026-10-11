# Methodology

How a Security Posture Advisor cycle runs, what goes in, and what comes out.

---

## 1. Inputs

| Input | Source | Notes |
|---|---|---|
| Service tier | Confirmed with the account at the start of every cycle | Sets the branding, the tier label, and what may be described as in-scope service |
| Detection export | The client's endpoint/identity/cloud/Third Party alerts for the detection window |
| MDR escalation records | Every case the MDR team raised in the window | Treated as ground truth for containment; contradictions between a case narrative and its recorded resolution are surfaced, never smoothed |
| Configuration and health data | Health report values and console reads supplied by the advisor |
| Agent fleet export |
| Monthly service metrics | Kept separate from the detection window; never blended |
| Proactive-work log | Hunts run (including ones that found nothing), tuning authored, detection content added | The only way a clean hunt can be reported |
| Vulnerability list | Optional |
| Industry threat profile | Refreshed whenever older than 45 days; every claim carries a link and date |
| Per-client memory | One structured file per client | Findings, recommendations, exposure items, escalations, score history |

All operator-supplied inputs are collected **once, at the start**, in a single intake packet. Each block records whether it was supplied, so "not supplied this cycle" is a recorded state. A script then determines what ships and what is omitted, and drafts the "what we need next time" list from the gaps.

---

## 2. Deliverables

| Deliverable | Purpose |
|---|---|
| Call deck | The cadence conversation; 30 content slides maximum, plus up to six cover/agenda/divider/closing slides |
| Written record | The same content in prose for distribution and audit; detail that doesn't fit the slide budget moves here |
| Working spreadsheet | Fixed-schema tabs the client team works from |
| Structured export | A 1:1 serialization of the finished deck so slides and data can't drift |

---

## 3. Outside-in exposure

Every exposure finding carries evidence, source, collection date, a confidence level (**Confirmed**, **Probable**, or **Possible**), and what it means for this client. Where an exposure finding meets an inside detection (for example, leaked credentials alongside identity alerts), the brief draws that line explicitly. That overlap is usually the strongest story in the deck.

---

## 5. Recurrence and memory

- Every finding gets a stable ID: `<Client>-<YYYYMM>-<P|E|N|A><n>` for priority, exposure, noise, and action items.
- A finding **recurs** when a later cycle shows the same technique on the same host, the same file hash, or the same external indicator. It keeps its original ID, its occurrence count increments, and the deck shows a RECURRING flag.
- Findings are **never merged on ATT&CK technique alone.** Every merge records its rationale.
- Occurrence counts track cycles observed, not alert volume.
- An MDR re-escalation of an unresolved prior case is treated as one of the strongest recurrence signals available.
- When a deliverable is re-issued for the same window, only one cycle is tracked and the earlier file is recorded as superseded.

---

## 6. Attack chain-stage assessment

Findings are mapped onto a composite intrusion playbook corroborated by public reporting on current threat actor operations:

1. Map each priority finding and remaining-signal cluster to a stage. A finding can map to none.
2. Count adjacent stages present in the window or still open from prior cycles.
3. **Two or more adjacent stages raise priority.** The brief says so plainly, names the missing next stage, and lists concrete watch items tied to client actions.
4. The framing is always anchored to public reporting about the client's industry, never to how common the pattern is across other clients.

---

## 7. Service transparency rules

- **No hours saved, dollar figures, FTE estimates, or efficiency multipliers.** None of it can be sourced.
