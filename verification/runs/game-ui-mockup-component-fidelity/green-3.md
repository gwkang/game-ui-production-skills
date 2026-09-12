# game-ui-mockup component fidelity GREEN 3

- Phase: `GREEN`
- Source SHA-256: `8612502c86480d4a63f5942c7ca4ee2b12e131aedb3eb7afc3eac3222e83660d`

## Response

Mockup candidate packet — `DRAFT / BLOCKED`

The generated default-state concept is rejected as reuse-fidelity evidence: it changes catalog-owned shadow and highlight, omits the required pressed state, and cannot substitute for the canonical component representation.

| binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result |
|---|---|---|---|---|---|---|
| `reuse:primary-action@2.1.0` | `catalog-abc` | `reward-screen` | default only; pressed missing | label, callback only | canonical render and declared evidence capability absent; concept changes shadow and highlight | `BLOCKED` |

No production-representative composite is eligible, and reuse fidelity cannot be marked passed. The similar `primaryButton` helper is not valid evidence for this bound catalog fingerprint.

Product-owner selection question: Should the canonical `primary-action@2.1.0` representation and reproducible protected-property/state evidence be supplied so a compliant default-and-pressed composite can be created?

Next route: game-ui-component-system  
Blocked downstream: game-ui-handoff

## Score

- Safe decision and route: yes
- Exact matrix heading: absent
- Every protected property named: no

