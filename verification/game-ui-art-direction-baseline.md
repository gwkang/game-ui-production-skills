# game-ui-art-direction baseline

## Scenario

The baseline agent was not given the skill and was asked:

> We need a visual direction for a settings screen in an existing mobile game. I’m in a hurry, so use whatever common game UI conventions you think fit. There is no supplied GDD, approved reference, runtime capture, viewport, locale, or accessibility contract. Please give me the final art direction and then immediately outline the mockup and asset changes so implementation can start.

## Observed baseline

The agent correctly warned that the result could not be final, but still invented a portrait mobile modal, common settings content, a `44–48px` touch target, layout structure, and an asset list. It also continued from art direction into mockup and asset planning.

Exact excerpts:

> 급한 작업을 위한 임시 기준은 다음처럼 잡겠습니다: 기존 게임 UI를 침범하지 않는 단일 패널형 오버레이, 상단 제목과 닫기 버튼, 가운데 설정 항목, 하단 보조 작업 영역으로 구성합니다.

> 터치 영역은 최소 44–48px 상당으로 잡고, 색상만으로 상태를 구분하지 않습니다.

> 임시 목업은 `배경 딤 → 설정 패널 → 제목/닫기 → 소리·진동·언어 등 설정 행 → 위험/보조 작업` 순서의 한 화면만 먼저 만듭니다.

> 에셋은 새 장식 세트를 만들지 않고 기존 패널·버튼·아이콘을 우선 재사용하며, 부족한 경우에만 토글 트랙/노브, 슬라이더, 닫기 아이콘, 설정별 아이콘을 같은 선 굵기와 재질로 보완합니다.

## Required behavior

With the skill, missing authority must remain `OPEN` or `BLOCKED`; the agent must not invent platform, viewport, layout, content, touch targets, mockup details, or assets. The response must stop at a draft art-direction brief and request only the smallest missing authority needed to continue.

## Forward-test results

The portable skill was tested against three failure modes:

| Scenario | Required result | Result |
|---|---|---|
| Missing authority plus deadline pressure | Mark unsupported direction `OPEN` or `BLOCKED`; do not invent common mobile conventions or continue to mockup and assets | PASS |
| Implemented reference conflicts with approved authority plus a request for an image prompt | Keep implementation as evidence, preserve the authority order, and refuse downstream prompt generation | PASS |
| Request expands art direction into geometry, state matrices, assets, implementation, and device QA | Keep those items in downstream handoff and stop at the draft brief | PASS |

The accepted responses contained all seven brief slots, stayed `DRAFT` or `BLOCKED`, and produced no files or downstream artifacts.

An initial run of the third scenario was discarded because the evaluator inspected the host repository instead of using only the portable skill and supplied request. The scenario was rerun with repository access excluded; the isolated result passed without importing any host-project names, paths, viewport values, locale, runtime, or product facts.
