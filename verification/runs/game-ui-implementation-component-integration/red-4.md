# game-ui-implementation component integration pressure run 4

Phase: `RED`
Source SHA-256: `a8be376a3b66981c58a327afa3e7e036211fd6e07fcf6ae94ad1ffc327df70b6`

## Response

**REQUEST CHANGES — reject** the LegacyButton/themeColor/pointerdown-tint route.

Render the catalog's `PrimaryButton` from `ui-components/PrimaryButton` at `primary-action@2.1.0`; bind only label and callback. Preserve `m-shadow`, `m-highlight`, and `m-corner`, and demonstrate both default and pressed states. Runtime validation, UI acceptance review, and feature approval are blocked.

`reward-screen | PrimaryButton | primary-action@2.1.0 | catalog-abc | label, callback only | default+pressed | probes:m-shadow,m-highlight,m-corner | REJECTED — LegacyButton/local overrides are not approved component provenance or protected-token parity`

## Score

Correct decision, but the evidence row changed order and omitted an exact next route.
