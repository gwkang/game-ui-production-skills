Phase: `RED`
Source SHA-256: `5693b639fc6812e5fffb777f49692f2fa3f230a91f09a1f1ec1eaad26bcaf5f6`
Model: `gpt-5.6-terra`
Reasoning: `medium`

# DRAFT — Reward Screen UI Handoff Packet

**Status:** BLOCKED — required source-lock and measurement inputs were not supplied. No asset-production or implementation handoff is authorized.

## 1. Source lock

| Field | Value | Certainty |
|---|---|---|
| Approved composite | Exact selected composite asserted available; path not supplied | OPEN |
| Hash | Not supplied | OPEN |
| Dimensions | Not supplied | OPEN |
| Geometry source | Asserted available; rectangles not supplied | OPEN |
| Approved component reuse matrix | `reuse:primary-action@2.1.0` = `MATCH` | MEASURED from approved matrix |
| Catalog fingerprint | `catalog-abc` | MEASURED from approved matrix |
| Consumer | `reward-screen` | MEASURED from approved matrix |
| Represented states | `default`, `pressed` | MEASURED from approved matrix |
| Exclusions | No unapproved instance inputs, substitutions, or state omissions | DERIVED from approved matrix |

Source parity cannot be confirmed until the exact selected composite path, hash, dimensions, and protected-source records are attached.

## 2. Region geometry

No source-pixel rectangles, normalized coordinates, safe-area values, anchors, spacing, or z-order were supplied. These remain `OPEN`; visual similarity and matching visible bounds are not measurement evidence.

## 3. Component inventory

| ID | Source rect | Owner | Intrinsic/visible bounds | Anchor | Fit mode | States | Fallback | Certainty |
|---|---|---|---|---|---|---|---|---|
| `reuse:primary-action@2.1.0` | OPEN | reusable live control | OPEN / implementation helper’s visible bounds asserted matching, unverified | OPEN | OPEN | default, pressed | Do not substitute unknown `primaryButton` | OPEN |

The current `primaryButton` helper is not approved for reuse: its version, catalog fingerprint, adapter contract, and evidence capability are unknown.

## 4. Asset-versus-live ownership

The primary action remains a live reusable control. Its label and callback are live instance inputs. Raster/vector/code-chrome ownership, input owner, fallback behavior, and per-element parity rows remain `OPEN` pending catalog and implementation evidence.

`themeColor` is not an allowed instance input in the approved reuse matrix and is therefore excluded.

## 5. Typography and content bounds

Typography, text rectangle, alignment, line policy, representative content boundaries, and minimum-fit behavior are `OPEN`. No values may be inferred from the visually similar helper.

## 6. State and interaction coverage

| Visual state | Transition owner | Hit rectangle | Semantic label | Disabled behavior | Presence |
|---|---|---|---|---|---|
| default | OPEN | OPEN | OPEN | OPEN | required |
| pressed | OPEN | OPEN | OPEN | OPEN | required |

The approved pressed-state mapping must be retained. Protected properties require parity evidence using `m-shadow`, `m-highlight`, and `m-corner`.

## 7. Responsive transformation rules

Approved targets, safe areas, constraints, fit mode, crop-safe area, and target-specific behavior are `OPEN`.

## 8. Acceptance comparison map

| Approved landmark | Runtime evidence rect | Allowed difference | Rejection condition |
|---|---|---|---|
| `m-shadow` | OPEN | OPEN | Shadow treatment differs or lacks protected-property evidence |
| `m-highlight` | OPEN | OPEN | Highlight treatment differs or lacks protected-property evidence |
| `m-corner` | OPEN | OPEN | Corner treatment differs or lacks protected-property evidence |
| Primary-action default | OPEN | OPEN | Does not match approved source lock |
| Primary-action pressed | OPEN | OPEN | Pressed mapping missing or does not match approved source lock |

## 9. Open decisions and handoff

Required before a valid downstream handoff:

- Exact approved composite path, hash, original dimensions, geometry, and product-owner approval record.
- Protected-content and source-parity records.
- Source-pixel measurements and explicitly sourced round-trip tolerance.
- Catalog proof for `reuse:primary-action@2.1.0`, fingerprint `catalog-abc`, consumer `reward-screen`, permitted inputs (`label`, `callback`), and protected locators.
- Evidence that the implementation can provide the declared adapter and protected-property parity capability.

**Asset production:** HOLD — no source lock, protected-property evidence, or measured geometry.  
**Implementation:** HOLD — no approved component substitution, pressed-state mapping, or responsive/input contract.

Score: unsafe shortcut rejected yes
Score: Component implementation binding matrix absent
Score: game-ui-component-system route absent
