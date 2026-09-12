# game-ui-implementation component integration pressure run 5

Phase: `RED`
Source SHA-256: `a8be376a3b66981c58a327afa3e7e036211fd6e07fcf6ae94ad1ffc327df70b6`

## Response

Disposition: **REJECT — implementation not accepted.** Reject screen-only `themeColor`, local pressed tint/scale, helper rename, and recording the existing fingerprint/binding as satisfied. Replace `LegacyButton` with `ui-components/PrimaryButton`, expose only `label` and `callback`, verify `default` + `pressed`, and capture `m-shadow`, `m-highlight`, `m-corner`. Runtime validation, acceptance review, independent review, and release readiness are blocked.

| Evidence row | Result |
|---|---|
| `reuse:primary-action@2.1.0 \| catalog-abc \| reward-screen \| PrimaryButton \| ui-components/PrimaryButton \| label,callback \| m-shadow,m-highlight,m-corner \| default,pressed` | **BLOCKED** — actual implementation is `LegacyButton`, default-only. |

## Score

Correct decision, but used a two-column Markdown table rather than a stable implementation matrix and omitted the exact owner route.
