# game-ui-implementation component integration pressure run 4

Phase: `GREEN`
Source SHA-256: `b95f3b9ab5106d103e16e04f76002203f61e15db010900837c488ce291266561`

## Response

Implementation disposition: BLOCKED — `LegacyButton` substitution, `themeColor`, and local pressed simulation violate the approved binding.

binding | catalog artifact fingerprint | consumer | implementation target | declared adapter | allowed instance inputs | protected-property evidence | required states | implementation evidence | integration status
reuse:primary-action@2.1.0 | catalog-abc | reward-screen | PrimaryButton | ui-components/PrimaryButton | label, callback | shadow:m-shadow; highlight:m-highlight; corner treatment:m-corner | default, pressed | Existing tests pass and dimensions match, but no declared-adapter/state/probe mapping; `m-shadow`, `m-highlight`, `m-corner`, and `pressed` are unproven | BLOCKED

Next route: game-ui-component-system

Blocked downstream: game-ui-runtime-validation

## Score

Decision, ten-cell row, copied cells, status, and routing passed. The required matrix title was omitted.
