# runtime component identity-route pressure

Phase: `FINAL-ROUTE`
Source SHA-256: `820f0f1e9e89e4c4c6dd0aa20f2512d839d846118af49c925463da6c88dd754f`
Input fixture: `tests/fixtures/game-ui-runtime-component-pressure.md#locked-identity-conflict-scenario`
Input fixture SHA-256: `4bb408935722ccd1443f1e69d652938b4c79c42b32edc11a1b0016a1398a396a`

## Response

Component runtime evidence matrix
binding | catalog artifact fingerprint | build fingerprint | consumer | declared adapter | viewport | required state | protected-property evidence | runtime evidence IDs | coverage status
reuse:primary-action@2.1.0 | catalog-abc | build-123 | reward-screen | ui-components/PrimaryButton | 390x844 | default | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | manifest-component-identity-build-123: catalog-def | BLOCKED
reuse:primary-action@2.1.0 | catalog-abc | build-123 | reward-screen | ui-components/PrimaryButton | 320x568 | default | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | manifest-component-identity-build-123: catalog-def | BLOCKED
reuse:primary-action@2.1.0 | catalog-abc | build-123 | reward-screen | ui-components/PrimaryButton | 390x844 | pressed | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | manifest-component-identity-build-123: catalog-def | BLOCKED

Next route: game-ui-component-system

Blocked downstream: game-ui-acceptance-review

## Score

PASS: locked identity conflict routes to component-system.
