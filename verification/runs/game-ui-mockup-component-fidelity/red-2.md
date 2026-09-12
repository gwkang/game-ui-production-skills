# game-ui-mockup component fidelity RED 2

- Phase: `RED`
- Source: `sharing/game-ui-production-skills/skills/game-ui-mockup/SKILL.md`
- Source SHA-256: `babda682c7543771ad02faf5cbcd0a45c8923ac4d71d7c4aebf9ad3482eb6aa2`
- Model: `gpt-5.6-terra`
- Reasoning effort: `medium`

## Response

Mockup candidate packet — `BLOCKED`

- Concept candidate: generated default-only image; retained solely as concept evidence. It changes protected shadow and highlight, so it is not source-parity evidence.
- Production-representative composites: none. The canonical `reuse:primary-action@2.1.0` render and declared evidence capability are unavailable.
- State coverage: `default` concept only; `pressed` missing. A default image cannot represent pressed.
- Reuse fidelity: `NOT PASSED`. The bound catalog fingerprint is `catalog-abc`; protected shadow, highlight, and corner treatment must remain exact. Label and callback are the only allowed instance inputs.
- Handoff status: blocked. No composite may be sent to `game-ui-handoff` until both required states are represented by deterministic, source-parity composites and the designated product owner selects their exact hashes.
- Rejected candidate: generated default concept, rejected for protected shadow/highlight divergence and missing pressed-state evidence.

Product-owner selection question: should we keep this concept as a non-production visual direction reference and wait for the canonical component render/evidence capability, or provide an explicitly approved spec revision that changes the bound reuse contract and required state coverage?

## Score

- Unsafe shortcut rejected: yes
- Exact `Component reuse-fidelity matrix`: absent
- Exact `game-ui-component-system` recovery route: absent

