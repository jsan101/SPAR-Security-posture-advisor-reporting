# Metrics

Aggregate figures for the practice from **May 12 to October 7, 2026**. Every number is a total across the whole client book. None can be traced to a single organization, and per-industry breakdowns are deliberately left out because some industry clusters are small enough to identify a client.

---

## Volume

| Measure | Value | Definition |
|---|---|---|
| Client environments | 41 | Distinct environments with a tracked client memory file, across about ten industry clusters and more than one MDR service line |
| Cadence decks delivered | 107 | Call decks produced, including a small number of same-window re-issues |
| Written records / workbooks | 98 / 96 | Companion deliverables (a few early cycles shipped deck-only) |
| Tracked cycles | 105 | Cycles recorded in client memory (re-issues of the same window count once) |
| Alerts analyzed | 1,150,451 | Sum of in-window alerts across tracked cycles |
| MDR escalation cases reconciled | 909 | Cases matched to detections and recorded for recurrence |

## Findings and follow-through

| Measure | Value | Definition |
|---|---|---|
| Priority findings tracked | 324 | Distinct findings with a stable ID |
| Findings that recurred | 108 (33%) | Same host, hash, or external indicator seen again in a later cycle |
| Exposure findings tracked | 386 | Outside-in findings with evidence, source, date, and confidence |
| Action Plan items raised | 928 | Rows with an owner, timeline, and expected outcome |

About one in three priority findings returned in a later cycle. That is the clearest case for keeping a memory between briefs: without it, each recurrence would look like a new, isolated event.

## Service transparency

| Measure | Value | Definition |
|---|---|---|
| Cycles with a computable escalated/absorbed split | 17 | Introduced in late August 2026; requires a ticket column in the export |
| Median share of alerts closed without needing the client | 96% | Across those 17 cycles |
| Range | 10% – 100% | By definition, the low end is a window where most alerts were attached to escalated tickets |

## The practice itself

| Measure | Value |
|---|---|
| Specification versions | 22, each archived with a dated reason |
| Industry threat profiles maintained | 15, refreshed whenever older than 45 days |
| Failure modes documented, each with a gate | 11 |
| Target time per cycle (routed mode) | About 1 hour, against 2–3 hours serial and 6–9 hours manual |

---

## What the book saw

Share of the 41 environments in which each pattern was observed at least once during the period. Only patterns seen in seven or more environments are listed, so no row points to an individual client. These figures are for this portfolio only and never appear in a client deliverable.

| Pattern | ATT&CK (examples) | Environments |
|---|---|---|
| Credential access / harvesting | T1003, T1552, T1555 | 63% |
| Reconnaissance tooling | T1018, T1046, T1482 | 61% |
| Vulnerable-driver loads (BYOVD) | T1068, T1562.001 | 49% |
| Unsanctioned remote-management tools | T1219, T1133 | 46% |
| Social engineering | T1204 | 46% |
| C2 frameworks, implants, droppers | T1071, T1105, T1059 | 41% |
| Tunneling and covert channels | T1572, T1090 | 34% |
| Ransomware precursors and staging | T1053.005, T1490 | 29% |
| Lateral-movement toolkits | T1021.002, T1003.006 | 17% |

Many of these line up with the early stages of the attack chain the brief assesses every cycle, which is why recon, remote-management implants, and credential access get a close watch.

---

## Caveats

- **Totals are sums across cycles.** An environment analyzed monthly contributes each month's alerts.
- **The method changed during the period.** Figures that depend on a corrected rule (for example, containment before and after the blank-mitigation fix) are not compared across the change.
- **The posture score is not reported here.** Many clients' scores moved over the period as follow-through and exposure measurement came online, which reflects fuller measurement rather than worse environments. Averaging those scores would mislead.
