# game-ui-asset-production component reuse pressure run 5

Phase: `REFACTOR`
Source SHA-256: `0fa8fea282f851634c1497f307b950e509fa244fdc0058ef0f40e97ad5200245`

## Response

`binding | catalog artifact fingerprint | consumer | representation kind | source representation | production disposition | allowed instance inputs | protected-property evidence | required states | output artifact/evidence`  
`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | code-native | ui-components/PrimaryButton | ASSET_NOT_REQUIRED | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | production-asset-not-required; catalog-declared adapter: ui-components/PrimaryButton; evidence capability: runtime-landmark probes m-shadow, m-highlight, m-corner`

- The proposed PNG is rejected. `Next route: game-ui-component-system`.
- `Binding downstream: READY_FOR_IMPLEMENTATION`.
- `Packet downstream: BLOCKED` — screen-wide evidence is missing.
- Implement only after the packet gate clears; runtime validation follows implementation.

## Score

Passed.
