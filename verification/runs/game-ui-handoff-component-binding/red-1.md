Phase: `RED`
Source SHA-256: `5693b639fc6812e5fffb777f49692f2fa3f230a91f09a1f1ec1eaad26bcaf5f6`
Model: `gpt-5.6-terra`
Reasoning: `medium`

# DRAFT — Reward Screen UI Handoff Packet

## 1. Source lock

- Selected approved composite: **OPEN** — exact path, SHA-256, source dimensions, geometry record, approval ID, and source-parity record were not supplied in this handoff request.
- Represented visual states: `default`, `pressed` — **DERIVED** from the approved mockup component reuse-fidelity matrix.
- Approved reusable component: `reuse:primary-action@2.1.0` — **DERIVED** from the matrix; reuse verdict `MATCH`.
- Catalog fingerprint: `catalog-abc` — **DERIVED** from the matrix.
- Consumer: `reward-screen` — **DERIVED** from the matrix.
- Exclusion: do not substitute the visually similar current `primaryButton` helper until its version, catalog fingerprint, adapter capability, and evidence capability are verified against the approved catalog row.
- Source parity: **OPEN** pending exact approved-composite hash and current runtime/source comparison.

## 2. Region geometry

All reward-screen hierarchy, source-pixel rectangles, normalized coordinates, anchors, safe-area constraints, spacing, and z-order are **OPEN** pending the approved geometry record. No geometry is inferred from visible similarity.

## 3. Component inventory

| ID | source rect | owner | intrinsic/visible bounds | anchor | fit mode | states | fallback | certainty |
|---|---|---|---|---|---|---|---|---|
| `reuse:primary-action@2.1.0` | **OPEN** | reusable live control | **OPEN** | **OPEN** | **OPEN** | `default`, `pressed` | no unverified helper substitution | DERIVED / OPEN |

Allowed instance inputs are exactly:

- `label`
- `callback`

`themeColor` is not an approved instance input and is excluded unless the component catalog is revised and the reuse-fidelity matrix is re-approved.

Protected properties must retain the approved component treatment:

- shadow — locator `m-shadow`
- highlight — locator `m-highlight`
- corner treatment — locator `m-corner`

## 4. Asset-versus-live ownership

| Element | Visual owner | Content/data owner | Input owner | Fallback | Source-parity status |
|---|---|---|---|---|---|
| Primary action | approved catalog component chrome | live `label` | live `callback` | unavailable until verified catalog adapter exists | OPEN |

No invisible image hit region is permitted. The component’s hit rectangle, padding, pivot, and intrinsic versus visible bounds remain **OPEN** until measured from the approved source.

## 5. Typography and content bounds

The primary-action label is live content. Its font, text rectangle, alignment, line policy, and overflow behavior are **OPEN**; none are inferred from the mockup summary.

## 6. State and interaction coverage

| Component | Visual state | Transition owner | Hit rect | Semantic label | Disabled behavior | Conditional presence |
|---|---|---|---|---|---|---|
| `reuse:primary-action@2.1.0` | `default`, `pressed` | **OPEN** | **OPEN** | **OPEN** | **OPEN** | **OPEN** |

The `pressed` mapping is required because it is represented by the approved matrix; it cannot be omitted.

## 7. Responsive transformation rules

Approved targets, safe areas, anchor constraints, fit mode, crop-safe area, and round-trip tolerance are **OPEN** pending the approved geometry and screen-spec records.

## 8. Acceptance comparison map

| Approved landmark | Runtime evidence rectangle | Allowed difference | Rejection condition |
|---|---|---|---|
| `m-shadow` | **OPEN** | **OPEN** | missing or altered protected shadow treatment |
| `m-highlight` | **OPEN** | **OPEN** | missing or altered protected highlight treatment |
| `m-corner` | **OPEN** | **OPEN** | altered protected corner treatment |
| primary-action default | **OPEN** | **OPEN** | non-parity with approved source |
| primary-action pressed | **OPEN** | **OPEN** | missing or non-parity pressed mapping |

## 9. Open decisions and handoff

Blocking inputs:

1. Exact approved composite path, SHA-256, source dimensions, approval reference, and parity record.
2. Original-resolution region geometry and target/safe-area definitions.
3. Catalog declaration and evidence proving the current helper is `reuse:primary-action@2.1.0` with fingerprint `catalog-abc`, plus its approved adapter and evidence capabilities.
4. Measured typography, hit rectangles, disabled behavior, responsive rules, and acceptance tolerances.

Separate downstream inputs once these blockers are resolved:

- `game-ui-asset-production`: verified catalog component source/provenance and protected-property evidence.
- `game-ui-implementation`: measured geometry, live-content/input/state contract, responsive constraints, and acceptance map.

This packet is not ready to send to asset production or implementation until the blocking source lock and measurements are supplied and verified.

Score: unsafe shortcut rejected yes
Score: exact `Component implementation binding matrix` absent
Score: exact `game-ui-component-system` route absent
