---
Phase: FORMAT
source_sha256: e844adc4812c05c7cbf87e1e5017db1dfc2b213c7c3430ad2a649146763462ac
score_ten_columns: yes
all_ten_packet_slots: yes
---

DRAFT UI handoff packet

Source lock — BLOCKED: approved reward-screen composite hash, dimensions, exact geometry, source paths, approval record, and source-parity record were not supplied. States: default, pressed. Exclusions: themeColor; no widened inputs.

Region geometry — BLOCKED: exact source-pixel and normalized rectangles, anchors, safe areas, spacing, and z-order are unavailable.

Component inventory — BLOCKED: primary action bounds match visually, but intrinsic/visible bounds, pivot, padding, and verified catalog target are unavailable.

Component implementation binding matrix  
binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | mockup fidelity | handoff status  
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | primaryButton; version and fingerprint unknown | catalog-declared adapter/evidence capability; exact target identity unverified | label, callback | shadow [m-shadow]: reproduce locator; highlight [m-highlight]: reproduce locator; corner treatment [m-corner]: reproduce locator | default, pressed | MATCH | BLOCKED

Asset-versus-live ownership — BLOCKED: ownership and parity rows require the locked composite and geometry.

Typography and content bounds — BLOCKED: no measured font or content bounds supplied.

State and interaction coverage — BLOCKED: preserve default and pressed; hit rectangle, transitions, and disabled behavior are unmeasured.

Responsive transformation rules — BLOCKED: approved targets and measured constraints are unavailable.

Acceptance comparison map — BLOCKED: approved landmarks and runtime evidence rectangles require the source lock.

Open decisions and handoff — Do not add `themeColor`; do not omit catalog fingerprint, protected locators, or pressed state. The exact `primaryButton` version/fingerprint and its evidence against `catalog-abc` must be confirmed before downstream work.

Next route: game-ui-component-system  
Blocked downstream: game-ui-asset-production, game-ui-implementation
