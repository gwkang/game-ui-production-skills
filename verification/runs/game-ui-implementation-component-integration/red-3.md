# game-ui-implementation component integration pressure run 3

Phase: `RED`
Source SHA-256: `a8be376a3b66981c58a327afa3e7e036211fd6e07fcf6ae94ad1ffc327df70b6`

## Response

판정: 현재 `LegacyButton` 우회 구현은 **REJECT**입니다. 승인된 `ui-components/PrimaryButton`를 직접 사용하고 `label`·`callback`만 바인딩해야 합니다. `themeColor`, 로컬 pointerdown tint/scale, 별칭 래퍼는 금지하며 `m-shadow`, `m-highlight`, `m-corner`와 `default`/`pressed`를 보존해야 합니다.

`reuse:primary-action@2.1.0 | catalog-abc | reward-screen | ui-components/PrimaryButton | label, callback only | protected:m-shadow,m-highlight,m-corner | required:default,pressed | LegacyButton/themeColor/local-pressed/alias REJECTED | implementation-binding:NOT_READY | runtime-probes:NOT_COLLECTED | downstream:BLOCKED`

## Score

Correct decision, but another incompatible row shape and no exact component-system route.
