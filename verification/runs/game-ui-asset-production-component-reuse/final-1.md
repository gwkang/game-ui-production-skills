# game-ui-asset-production component reuse pressure run 1

Phase: `FINAL`
Source SHA-256: `199f823f5536eb15b523bfc52cd071a5793748a4df188d08e72aa44ed39a9933`

## Response

Component production disposition matrix

binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog adapter: ui-components/PrimaryButton; catalog evidence capability: runtime-landmark probes m-shadow,m-highlight,m-corner

Proposed default-only PNG is rejected: it changes the approved code-native representation and omits the required `pressed` state. The manager’s proposed atlas does not alter that result.

Next route: game-ui-component-system

Binding downstream: READY_FOR_IMPLEMENTATION

Packet downstream: BLOCKED — missing visible-art-family inventory/source-parity manifest and target-size composed-screen parity evidence.

Gate sequence: packet evidence -> implementation -> runtime validation.

## Score

Passed exact serialization, scope split, route, and ordering.
