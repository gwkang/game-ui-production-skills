---
Phase: FORMAT
source_sha256: e844adc4812c05c7cbf87e1e5017db1dfc2b213c7c3430ad2a649146763462ac
score_ten_columns: yes
all_ten_packet_slots: yes
---

DRAFT UI handoff packet

Source lock: approved reward-screen composite; selected files, exact hash, dimensions, source parity, and geometry: OPEN/not supplied. States: default, pressed. Approval: approved. Exclusion: do not add `themeColor`.

Region geometry: BLOCKED — exact geometry values were not supplied.

Component inventory: `reuse:primary-action@2.1.0` | primary action | OPEN | OPEN | OPEN | OPEN | default, pressed | none | BLOCKED

Component implementation binding matrix
binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton | missing: catalog declaration and evidence capability not supplied | label, callback | shadow locator m-shadow must be reproduced; highlight locator m-highlight must be reproduced; corner treatment locator m-corner must be reproduced | default, pressed | MATCH | BLOCKED

Asset-versus-live ownership: BLOCKED — ownership and parity rows were not supplied.

Typography and content bounds: BLOCKED — measurements were not supplied.

State and interaction coverage: default and pressed required; semantic label, hit rectangle, transition owner, and disabled behavior: OPEN/not supplied.

Responsive transformation rules: BLOCKED — approved targets and measurements were not supplied.

Acceptance comparison map: BLOCKED — approved landmarks, runtime rectangles, allowed differences, and rejection conditions were not supplied.

Open decisions and handoff: `primaryButton` cannot be used as the implementation target until the catalog declares its exact adapter identity for `catalog-abc`, version/fingerprint, and protected-property evidence capability. `themeColor` is outside the approved allowed inputs.

Next route: game-ui-component-system
Blocked downstream: game-ui-asset-production, game-ui-implementation
