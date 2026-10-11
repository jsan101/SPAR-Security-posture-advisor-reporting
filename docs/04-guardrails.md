# Guardrails

The rules below apply in every operating mode, with or without AI, under any deadline.

---

## Non-negotiable rules

1. **Never fabricate threat intelligence.**
2. **Every attribution and ATT&CK mapping carries a linked, dated source**
3. **OSINT is passive only.** 
4. **Never reproduce leaked credentials.**
5. **Cadence findings recommend actions the client can take directly:** 
6. **Scripts compute every number.** 
7. **No client's data reaches another client,**
8. **Deliverables are client-facing end to end:**
9. **Never cite a denominator you can't enumerate.**

---

## Tone standard

These briefs often reach a security team in front of its own leadership. The analysis stays exactly as factual; the register treats the finding as shared work in progress rather than a verdict on the team.

- **State the fact, then the path.** 
- **Attribute to the environment, not to people.**
- **Own the service's lane in the first person.**
- **Absence is not accusation.**
- **Let the data carry urgency.**
- **Say what is working.**

| Instead of | Write |
|---|---|
| "6 settings off baseline" | "6 settings differ from the baseline" |
| "containment gap" | "open for confirmation" / "awaiting adjudication" |
| "customer unresponsive" | "awaiting client confirmation" |
| "you failed to patch these hosts" | "these hosts are still on version X; the upgrade is the Week 1 item" |
| "poor rule coverage" | "12 of 40 platform rules enabled" |
| "no action taken" | "no action recorded this window" |
| "urgent — fix immediately" | Severity chip plus "Week 1" in the Action Plan |

---

## The validator

An automated gate runs before anything is shared. It checks:

- Client schema
- Recorded cycles
- Recurrence consistency
- Posture-score arithmetic
- Structured-export schema, client/date agreement, and information integrity
- A tone phrase scan (hard-fail list and warn list)
- Competitor-citation scans
- Pinned model assignments for each step of the AI pipeline
