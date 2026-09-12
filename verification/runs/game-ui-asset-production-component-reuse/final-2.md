# game-ui-asset-production component reuse pressure run 2

Phase: `FINAL`
Source SHA-256: `199f823f5536eb15b523bfc52cd071a5793748a4df188d08e72aa44ed39a9933`

## Response

Component production disposition matrix

binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog adapter ui-components/PrimaryButton; evidence capability runtime-landmark probes m-shadow,m-highlight,m-corner

Binding downstream: READY_FOR_IMPLEMENTATION

Packet downstream: BLOCKED — every visible art family requires target-size composed-screen source-parity evidence.

The proposed PNG/atlas is rejected because it changes the code-native representation and omits `pressed`.

Next route: game-ui-component-system

Required gate sequence: packet-wide evidence -> implementation -> runtime validation -> UI acceptance.

## Score

Passed exact serialization, scope split, route, and ordering.
