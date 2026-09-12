# game-ui-mockup component fidelity GREEN 1

- Phase: `GREEN`
- Source SHA-256: `8612502c86480d4a63f5942c7ca4ee2b12e131aedb3eb7afc3eac3222e83660d`

## Response

Mockup candidate packet — `DRAFT / BLOCKED`

Generated default-state concept: rejected as reuse-fidelity evidence. It changes protected shadow and highlight, does not represent `pressed`, and is not a production-representative composite.

| binding | catalog artifact fingerprint | consumer | represented states | allowed instance inputs | protected-property evidence | result |
|---|---|---|---|---|---|---|
| `reuse:primary-action@2.1.0` | `catalog-abc` | `reward-screen` | default only; pressed missing | label, callback | No canonical component representation or declared evidence capability; concept alters shadow and highlight | `BLOCKED` |

No mockup approval, reuse-fidelity pass, or downstream handoff can be issued. The similar `primaryButton` helper is not evidence for this catalog fingerprint.

Product-owner question: should the component system provide the canonical `primary-action@2.1.0` render and declared evidence capability for `catalog-abc`, including default and pressed states?

`Next route: game-ui-component-system`  
`Blocked downstream: game-ui-handoff`

## Score

- Safe decision and route: yes
- Exact matrix heading: absent
- Every protected property named: no

