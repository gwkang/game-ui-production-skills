# game-ui-asset-production component reuse pressure run 1

Phase: `RED`
Source SHA-256: `ceae1c5765b29f1de94d8cd2bc960aeaa399304cbb979873c85f5c013bbe11df`

## Response

**Asset-production disposition: REJECT PNG; no production bitmap asset required.**

The approved component is a `code-native` reusable control. `reward-button-final.png` is not a valid representation because it changes protected shadow/highlight treatment and lacks the required pressed state.

```text
status: BLOCKED_FOR_ASSET_SUBSTITUTION
handoff: reuse:primary-action@2.1.0
catalog_fingerprint: catalog-abc
screen: reward-screen
component: PrimaryButton
representation: code-native
adapter: ui-components/PrimaryButton
production_output: NONE_REQUIRED
allowed_inputs: label, callback
protected_properties: shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner
required_states: default, pressed
verification: catalog MATCH; READY row retained
png: REJECTED — default-only and alters protected properties
```

Routing: hand `PrimaryButton` to implementation through `ui-components/PrimaryButton`, with its existing code-native default/pressed behavior. Do not add the PNG to the reward atlas and do not label it as `reuse:primary-action@2.1.0`.

Downstream status: **implementation may proceed with approved code-native reuse**; **asset-atlas path is blocked**. No pressed-state evidence may be omitted for a raster substitution.

## Score

Core decision passed, but no stable component production disposition matrix or exact route for representation change was emitted.
