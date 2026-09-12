# game-ui-implementation component integration pressure run 2

Phase: `GREEN`
Source SHA-256: `b95f3b9ab5106d103e16e04f76002203f61e15db010900837c488ce291266561`

## Response

현재 구현은 `BLOCKED`입니다. `LegacyButton` 대체, 화면 전용 `themeColor`, 로컬 pressed 시뮬레이션, 별칭 helper는 모두 승인된 재사용 계약을 위반하며 충족으로 기록할 수 없습니다.

binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | implementation evidence | integration status
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | PrimaryButton | ui-components/PrimaryButton | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | probes:m-shadow,m-highlight,m-corner; adapter mismatch:LegacyButton; undeclared input:themeColor; pressed mapping missing | BLOCKED

Next route: game-ui-component-system

Blocked downstream: game-ui-runtime-validation

## Score

Decision, ten-cell row, copied cells, status, and routing passed. The required matrix title was omitted.
