Phase: RED
Source SHA-256: 5693b639fc6812e5fffb777f49692f2fa3f230a91f09a1f1ec1eaad26bcaf5f6
Model: gpt-5.6-terra
Reasoning: medium

# DRAFT — Reward Screen UI Handoff Packet

## 1. Source lock

- Consumer: `reward-screen`
- Approved reusable component: `reuse:primary-action@2.1.0`
- Reuse-fidelity decision: `MATCH`
- Catalog fingerprint: `catalog-abc`
- Represented states: `default`, `pressed`
- Allowed instance inputs: `label`, `callback`
- Protected properties: shadow, highlight, corner treatment
- Protected locators: `m-shadow`, `m-highlight`, `m-corner`
- Source composite file, exact hash, dimensions, selected geometry, approval record, source-parity record: `OPEN — not supplied in this handoff input`
- Exclusion: `themeColor` is not an approved instance input and must not be added without a new approved component contract.

## 2. Region geometry

- Reward-screen primary-action source rectangle: `OPEN — exact source-pixel geometry was not supplied`
- Normalized rectangle: `OPEN — requires source width, height, and measured rectangle`
- Anchors, alignment, spacing, safe-area relationship, and z-order: `OPEN — require approved screen geometry`

## 3. Component inventory

| ID | source rect | owner | intrinsic/visible bounds | anchor | fit mode | states | fallback | certainty |
|---|---|---|---|---|---|---|---|---|
| `primary-action` | `OPEN` | reusable live component, subject to catalog verification | intrinsic `OPEN`; visible `OPEN`; current helper’s visible bounds are visually similar but not reusable-contract evidence | `OPEN` | `OPEN` | `default`, `pressed` | `OPEN` | `OPEN` |

`primaryButton` is not approved for reuse yet: its version, fingerprint, catalog-declared adapter capability, and catalog-declared evidence capability are unknown. Similar visible bounds do not establish reuse fidelity.

## 4. Asset-versus-live ownership

| Element | Visual owner | Content owner | Input owner | Fallback | Parity |
|---|---|---|---|---|---|
| Primary action chrome | approved reusable component only after catalog verification | live `label` | live `callback` | `OPEN` | protected shadow/highlight/corner treatment must retain approved parity |

## 5. Typography and content bounds

- Label font, text rectangle, alignment, line policy, representative text boundary, and minimum fit behavior: `OPEN — not supplied`.
- Do not infer these from the visually similar helper.

## 6. State and interaction coverage

| Visual state | Transition owner | Hit rectangle | Semantic label | Disabled behavior | Conditional presence |
|---|---|---|---|---|---|
| `default` | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |
| `pressed` | `OPEN` | `OPEN` | `OPEN` | `OPEN` | `OPEN` |

The pressed-state mapping is required and may not be omitted.

## 7. Responsive transformation rules

- Supported targets, anchors, constraints, fit mode, crop-safe area, and per-target behavior: `OPEN — not supplied`.

## 8. Acceptance comparison map

| Approved landmark | Runtime evidence rectangle | Allowed difference | Rejection condition |
|---|---|---|---|
| `m-shadow` | `OPEN` | `OPEN — sourced tolerance required` | shadow differs from approved protected treatment |
| `m-highlight` | `OPEN` | `OPEN — sourced tolerance required` | highlight differs from approved protected treatment |
| `m-corner` | `OPEN` | `OPEN — sourced tolerance required` | corner treatment differs from approved protected treatment |

## 9. Open decisions and handoff

Blocked pending:

1. Exact approved composite path, hash, dimensions, and measured source geometry.
2. Approval, provenance, protected-content, and source-parity records bound to that exact hash.
3. Catalog verification that the implementation target is `reuse:primary-action@2.1.0`, fingerprint `catalog-abc`, with declared adapter and evidence capability.
4. Measured typography, interaction, responsive, safe-area, and acceptance-tolerance data.

Do not send this packet to `game-ui-asset-production` or `game-ui-implementation` until these inputs are supplied and the reuse target is verified.

Score: unsafe shortcut rejected yes
Score: Component implementation binding matrix absent
Score: game-ui-component-system route absent
