# Posture Score

A directional 0–100 score that shows the client which way their environment is moving between cycles. It is not an audit grade. If a client questions the number, the component table is the answer: every input ships in their spreadsheet.

The score is always computed by script. A language model never does the arithmetic.

---

## Components

| Component | Weight | Basis |
|---|---|---|
| **Containment** | 25 | 
| **Verdict hygiene** | 15 |
| **Noise trend** | 20 |
| **Follow-through** | 20 |
| **Exposure** | 20 |

---

## Worked example (fictional client)

### Cycle 1: baseline

| Component | Input | Points |
|---|---|---|
| Containment | 18 of 20 High/Critical true positives contained | 22.5 |
| Verdict hygiene | 8% of alerts undefined | 13.8 |
| Noise trend | First cycle | 10.0 |
| Follow-through | First cycle, so excluded | — |
| Exposure | 1 Confirmed-critical, 2 High/Probable open | 11.0 |
| **Sum** | | **57.3 of 80** |
| **Score** | 57.3 ÷ 0.8 = 71.6 | **72** |

### Cycle 2

| Component | Input | Points |
|---|---|---|
| Containment | 30 of 30 contained | 25.0 |
| Verdict hygiene | 5% undefined → 14.25 | 14.3 |
| Noise trend | Noise share fell from 70% to 56%, a 20% relative reduction | 12.0 |
| Follow-through | 10 prior actions open: 4 closed, 2 in progress | 10.0 |
| Exposure | The Confirmed-critical item closed; 1 High/Probable still open | 18.0 |
| **Score** | | **79 ▲ +7** |

---

## Reading the trend

The score is most useful as direction of travel. Two cautions apply:

- **Fuller measurement can lower a score.** When follow-through starts counting after the first cycle, or a new exposure finding is confirmed, the score can drop even though nothing in the environment got worse. Trend commentary says so.
