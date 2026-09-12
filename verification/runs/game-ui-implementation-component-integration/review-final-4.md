# game-ui-implementation component integration pressure run 4

Phase: `FINAL`
Source SHA-256: `c457752a5aad3742db66130ad9b04a7e5244e883bed4b1f494220fcadd4ad12f`

## Response

Component runtime integration matrix
binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | implementation evidence | integration status
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | PrimaryButton | ui-components/PrimaryButton | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | No declared-adapter capability mapping; LegacyButton is default-only and m-shadow/m-highlight/m-corner/pressed are absent | BLOCKED

Next route: game-ui-component-system

Blocked downstream: game-ui-runtime-validation

## Score

PASS: exact title, header, copied cells, status, owner route, and blocked downstream.
