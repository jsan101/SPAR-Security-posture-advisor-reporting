# Security Posture Advisor

**Turning MDR telemetry into a recurring, evidence-grade security brief**
Jeremy San Nicolas · Staff Threat Advisor · October 2026

---

## Summary

Security Posture Advisor is a recurring client briefing practice I designed and run for managed detection and response (MDR) clients. Each cycle combines a client's detection export, the record of what the MDR team escalated, service and configuration data, and passive open-source intelligence. It produces a call deck, a written record, and a working spreadsheet, and it keeps a running memory of every finding and recommendation so the next cycle starts where the last one ended.

Since May 2026 it has produced more than 100 briefs across 40+ client environments in about ten industries, covering more than a million alerts. The method has gone through 22 documented revisions in that time.

Every brief is held to one test: *could the client's CISO use this to justify a budget or policy decision without opening the security console?*

---

## The problem

MDR reporting is good at saying what happened in the alert queue. Clients usually want answers to the questions that come after that:

- Which alerts are costing my team the most time, and what exactly do we change to remove them?
- Which of these detections match campaigns aimed at my industry right now?
- What can an attacker learn about us without touching an endpoint?
- What is likely to come next, and what should we prepare?
- Is our detection and response configuration set up to catch it, and are our agents still supported?
- What did the service handle on our behalf?

Security Posture Advisor is built to answer all six, every cycle, in a form a client's leadership can act on.

---

## Intent: a four-part mission

1. **Reduce noise.** Recommend specific suppression and policy changes based on the client's own false-positive clusters, then measure whether last cycle's changes worked.
2. **Validate the real signal.** Check true-positive findings against current public threat reporting from primary sources (for example Mandiant/Google Threat Intelligence, Microsoft Threat Intelligence, CISA, Talos, Unit 42), and map them to MITRE ATT&CK.
3. **Show the danger from the outside in.** Use passive OSINT to show exposure independently of the console, and turn every finding into a client-side-first Action Plan with owners, timelines, and expected outcomes.
4. **Show what the service absorbed.** Report the alerts worked and closed without needing the client, and the proactive work done outside the alert queue, as counts the client can verify. No invented hours-saved or cost figures.

---

## What a client receives

| Deliverable | Purpose |
|---|---|
| **Call deck** | The cadence conversation |
| **Written record** | The same content in prose, for distribution and audit trail; anything that does not fit the slides lives here |
| **Working spreadsheet** | A fixed set of tabs the client's team works from: scorecard, priority findings, escalations, exposure, noise clusters, Action Plan, outlook, configuration health, service metrics, and more |
| **Machine-readable export** | A structured copy of the finished deck, so data and slides always match |

### What the brief covers

**Posture scorecard and trend.** A directional 0–100 score built from containment, verdict hygiene, noise trend, follow-through on prior recommendations, and open exposure. The full calculation ships in the spreadsheet so the client can check it.

**Detection and response configuration health.** Client's policy compared with the service baseline; response-policy settings; escalation matrixes split by channel; detection-rule coverage; and agent health.

**Priority storylines.** The few findings that mattered most this window, each with hosts, detection rules, ATT&CK techniques, dated public corroboration, links to the console and the client's own case records, and a flag when the same foothold has returned from a prior cycle.

**Service transparency.** Monthly service metrics and response times against objective by severity, with any severity below objective stated in plain words. A "work delivered" section shows how many alerts were closed without needing the client, what hunts and tuning were done, and what happened most recently. A hunt that found nothing is reported as a result.

**Outside-in exposure.** Known-exploited vulnerabilities that overlap the observed software, leaked-credential counts for client domains (never the credentials themselves), lookalike domains and brand abuse, and internet-indexed services. Collection is passive only: no scanning or probing of client infrastructure. 

**Noise reduction.** False-positive clusters with the exact console steps to suppress them, plus the measured effect of last cycle's tuning.

**Threat context.** Findings mapped to dated, linked public reporting; the actors currently active against the client's industry; and a watch list that crosses anything seen in the environment with current exploitation activity, where active exploitation outranks a CVSS score.

**Horizon.** Two or three items from a 90-day industry outlook, each tied to where it touches this client and one preparation to start now. An attack chain-stage read flags when an environment shows activity at two or more adjacent stages of the intrusion pattern behind current ransomware/ supply chain attack/Frontier AI operations, and names what the next stage would look like.

**Action Plan.** Client-side actions first (patching and end-of-life migration, identity hardening, egress controls, remote-tool policy, awareness, vendor follow-up, backup validation), service changes second.

---

## Evolution

| When | What changed |
|---|---|
| **May 2026** | First version: a consistent cross-client deck focused on two things, noise and signal
| **June 2026** | 
| **July 2026** | 
| **August 2026** | 
| **September 2026** | 

The direction across those versions has been consistent: more context for the client, more of the work made checkable, and corrections made openly when the method was wrong.

---

## How it stays trustworthy

- **No fabricated intelligence.** Every attribution and ATT&CK mapping carries a linked, dated source. A claim that cannot be sourced does not ship.
- **Scripts compute every number.** Counts, shares, scores, and lifecycle dates come from deterministic code, never from a language model.
- **An absent field is not a negative field.** A blank record is reported as undetermined, not as a failure and not as a success.
- **Passive OSINT only,** with leaked credentials never reproduced.
- **No client's data reaches another client.**
- **An automated gate.** Nothing ships until a validator confirms data consistency, scoring arithmetic, citation rules, and formatting rules.

### Where AI fits

The practice is AI-orchestrated and human-governed. A frontier model handles the judgment calls about the outside world: threat correlation, ATT&CK mapping, exposure analysis, and adjudicating ambiguous evidence. A lighter model handles drafting and mechanical steps, and it is not allowed to write a citation, attribution, or exposure finding; if it needs one, it stops and reports the gap. Scripts do all arithmetic. A human approves the storylines, suppression decisions, and anything ambiguous before any deliverable is built. The method is written so it can also run with assisted AI or with no AI at all.

---

## Value

**For clients**
- A brief leadership can act on without console access, covering noise, real incidents in context, external exposure, and what is coming next.
- Claims they can verify: dated sources, a score whose inputs are in their spreadsheet, and service counts they can audit.
- Continuity: findings that recur, actions that are aging, and configuration and fleet trends carried across cycles. Roughly one in three priority findings has recurred in a later cycle, which is why the memory matters.
- Lead time on agent-support deadlines, exploited vulnerabilities in software they run, and early attack-chain activity.
- A factual record of what the service handled for them.

**For the service**
- A consistent deliverable across a large client book, with scope stated accurately for each service tier.
- Configuration and lifecycle issues raised early and in a constructive tone.
- Reusable intelligence and a packaged method that other advisors can adopt.

**For the practice of security advisory**
- A working example of using AI in client-facing security work responsibly: frontier models where judgment about the outside world is needed, scripts for every number, and a human gate before anything ships.

---

*Client names and client-specific data are deliberately excluded from this write-up.*
