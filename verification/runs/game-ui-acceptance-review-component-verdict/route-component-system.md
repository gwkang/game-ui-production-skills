# component acceptance identity-route pressure

Phase: `FINAL-ROUTE`
Source SHA-256: `e4a3c3bc563d0bbbf1df7f641bad650102ff408b3fc4175eea292b594e4e051e`
Input fixture: `tests/fixtures/game-ui-acceptance-component-pressure.md#locked-identity-conflict-scenario`
Input fixture SHA-256: `0bf32fd5cf3c1fb931620f55dded9d75beb68c13149a611a0a10692c3849d40f`

## Response

Component acceptance matrix
binding | catalog artifact fingerprint | build fingerprint | consumer | declared adapter | required states | runtime evidence IDs | protected-property verdict | open severity | component verdict
reuse:primary-action@2.1.0 | catalog-abc | build-123 | reward-screen | ui-components/PrimaryButton | default, pressed | cap-390-default, cap-320-default, cap-390-pressed, manifest-component-identity-build-123 | not established under conflicting identity | P1 | REJECTED
Decision: REJECT UI
The current runtime identity is catalog-def, which conflicts with catalog-abc.
Next route: game-ui-component-system
Feature-review status: BLOCKED

## Score

PASS: locked binding identity conflict routes to component-system.
