# Templates

Fictional examples that show the shape of the practice's working artifacts. **Every name, host, number, and case ID here is invented.**

| File | What it shows |
|---|---|
| [`client-memory.example.json`](client-memory.example.json) | The per-client memory file: cycles with score components, findings with stable IDs, recommendations, exposure items, escalations, and notes |

## Action Plan row

| ID | Lane | Action | Owner | Timeline | Expected outcome | Status |
|---|---|---|---|---|---|---|
| ExampleCo-202601-A1 | Client | Enable LSA protection on file servers and rotate the service account seen in the alert | Client IT – Identity | Week 1 | Credential-dumping path closed on the affected server class | Open |
| ExampleCo-202601-A2 | Console | Add a path-scoped exclusion for the in-house backup agent's signed binary | SentinelOne MDR | Week 2–3 | Removes the largest false-positive cluster (about 40% of window volume) | Open |

## Exposure finding card

| Field | Example |
|---|---|
| ID | ExampleCo-202601-E1 |
| Category | Brand abuse |
| Finding | Lookalike domain registered with an active mail (MX) record |
| Evidence | Registration date, current DNS resolution, certificate-transparency entry |
| Source | Public DNS and certificate-transparency logs (passive) |
| Collected | 2026-01-14 |
| Confidence | Probable |
| Linked inside detection | None this window |
| What it means here | A phishing-capable domain that impersonates the client; no clicks observed yet |
| Action | Request a takedown; add the domain to the mail-gateway blocklist (client, Week 1) |

## Chain-stage note

```
chain-stages 2026-01: recon (P3) cred-access (P1) - adjacent, elevated
next stage to watch: remote-management tools appearing on hosts scanned in stage 1
```
