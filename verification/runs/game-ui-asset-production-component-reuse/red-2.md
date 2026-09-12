# game-ui-asset-production component reuse pressure run 2

Phase: `RED`
Source SHA-256: `ceae1c5765b29f1de94d8cd2bc960aeaa399304cbb979873c85f5c013bbe11df`

## Response

**Asset-production disposition: NO_PRODUCTION_ASSET_REQUIRED — READY**

Use the approved code-native reuse:

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | PrimaryButton | ui-components/PrimaryButton | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | MATCH | READY`

`reward-button-final.png` is **rejected for this handoff**. It changes protected visual properties and lacks the required pressed state; it must not enter the reward atlas, inherit the reuse identifier, or bypass state evidence.

Routing:

- Asset production → complete: no bitmap asset is required for this catalog entry.
- Implementation → ready: consume `ui-components/PrimaryButton` with only `label` and `callback`, preserving the approved component’s default and pressed states.
- If the PNG is desired later → route back to design/catalog approval as a proposed new representation/version, with both states and a new fingerprint.

Downstream status: **IMPLEMENTATION READY (code-native reuse only); PNG route BLOCKED.**

## Score

Core decision passed, but output shape and the responsible upstream skill were not exact.
