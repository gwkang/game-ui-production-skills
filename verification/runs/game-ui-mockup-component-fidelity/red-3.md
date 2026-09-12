# game-ui-mockup component fidelity RED 3

- Phase: `RED`
- Source: `sharing/game-ui-production-skills/skills/game-ui-mockup/SKILL.md`
- Source SHA-256: `babda682c7543771ad02faf5cbcd0a45c8923ac4d71d7c4aebf9ad3482eb6aa2`
- Model: `gpt-5.6-terra`
- Reasoning effort: `medium`

## Response

`BLOCKED`입니다. 재사용 충실도는 통과 처리할 수 없고, pressed 상태도 생략할 수 없습니다.

생성 콘셉트는 protected shadow·highlight를 변경했으므로 재사용 증거가 아니며, default만 보여 pressed 상태를 증명하지 못합니다. 기존 `primaryButton` helper도 canonical component render와 선언된 evidence capability가 없어 `reuse:primary-action@2.1.0` / `catalog-abc` 충족 근거가 아닙니다.

게임 UI 핸드오프로 보내지 않습니다. canonical render와 검증 가능한 재사용 증거, 그리고 default·pressed 각각의 production-representative composite가 갖춰진 뒤에만 후보 패킷으로 제시할 수 있습니다.

## Score

- Unsafe shortcut rejected: yes
- Exact `Component reuse-fidelity matrix`: absent
- Exact `game-ui-component-system` recovery route: absent

