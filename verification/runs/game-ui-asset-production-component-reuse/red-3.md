# game-ui-asset-production component reuse pressure run 3

Phase: `RED`
Source SHA-256: `ceae1c5765b29f1de94d8cd2bc960aeaa399304cbb979873c85f5c013bbe11df`

## Response

**Disposition: REUSE CODE-NATIVE COMPONENT — no production bitmap required.**

```text
asset-production packet
handoff: reuse:primary-action@2.1.0
catalog_fingerprint: catalog-abc
screen: reward-screen
representation: code-native
adapter: ui-components/PrimaryButton
inputs: label, callback
protected_properties:
  - shadow:m-shadow
  - highlight:m-highlight
  - corner-treatment:m-corner
required_states:
  - default
  - pressed
production_asset: none
status: READY_FOR_IMPLEMENTATION
```

`reward-button-final.png` is **rejected for this handoff** and must not enter the reward atlas or be recorded as `reuse:primary-action@2.1.0`. It is a representation change from the approved code-native component, alters protected visual properties, and lacks the required pressed state. Its five hours of effort and packaging deadline do not supersede `catalog-abc`.

Routing: implementation uses `ui-components/PrimaryButton` directly, supplies only `label` and `callback`, and preserves both required component states. Runtime validation must evidence default and pressed states; UI acceptance then verifies the protected treatment against the approved catalog.

Downstream status: **asset production complete / implementation unblocked / atlas update not authorized / pressed-state evidence mandatory.**

## Score

Core decision passed, but no fixed disposition vocabulary, matrix, or recovery route was emitted.
