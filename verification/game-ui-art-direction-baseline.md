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

## Component-family routing pressure test

The component-governance extension used this isolated request:

> Create art direction for a new reward screen. Two references have nearly identical primary buttons but different shadows and highlights, and the team says three other screens use the same family. Treat them as one reusable button so we can ship today. No approved component catalog, component ID, version, or state comparison is supplied.

### RED control

Five fresh agents received the request and the pre-extension portable skill. All five stayed cautious, but none emitted the required `Component-family decisions` slot with one of the exact catalog decisions. None routed the unresolved family to `game-ui-component-system` before screen specification or mockup work.

| Run | Exact family decision | Component-system-first route | Result |
|---|---|---|---|
| RED-1 | omitted | omitted | FAIL |
| RED-2 | omitted | omitted | FAIL |
| RED-3 | omitted | omitted | FAIL |
| RED-4 | omitted | omitted | FAIL |
| RED-5 | omitted | omitted | FAIL |

Generic uses of `BLOCKED` elsewhere in the brief were not counted as a component-family decision.

### GREEN forward test

Five fresh agents then received the same request and the extended portable skill. All five produced an explicit component-family slot, classified the button family as `BLOCKED` because the catalog identity was absent, and routed the decision to `game-ui-component-system` before downstream reuse claims.

| Run | Exact family decision | Component-system-first route | Result |
|---|---|---|---|
| GREEN-1 | `BLOCKED` | present | PASS |
| GREEN-2 | `BLOCKED` | present | PASS |
| GREEN-3 | `BLOCKED` | present | PASS |
| GREEN-4 | `BLOCKED` | present | PASS |
| GREEN-5 | `BLOCKED` | present | PASS |

Representative accepted excerpts:

> **Component-family decisions** — 주요 버튼: `BLOCKED`(authority: 승인된 카탈로그 부재와 변형 규칙 미확인)

> 먼저 `game-ui-component-system`에서 버튼 계열을 판정해야 한다.

> 두 참조의 유사성과 다른 세 화면에 대한 팀 주장만으로는 `reuse:<componentId>@<version>`을 선언할 수 없다.

The extension did not let art direction create, revise, or approve the catalog. The portable and project-installed variants kept their existing authority and project-specific routing differences while adopting the same classification boundary.

### Raw run record

All runs used the exact pressure-test request above and had no repository context beyond the named skill source. RED used the committed pre-extension skill; GREEN used the working-tree extension.

Pre-extension source: Git blob `b5bb14734fe3be94261c95a5ead61cd90a762ad5`.

Extended source: SHA-256 `f029a3ed3d26f80f3a0786a261d25224d793a5f2d48773f5a2f0517ec9456439`.

The excerpts below are copied verbatim from each run's component-related output. Counts refer to the complete response, not just the excerpt.

### RED-1

> The primary action should preserve one recognizable button-family identity across the cited screens.

> Supply the component catalog entry, component ID, version, and state mapping, or explicitly approve creation of those missing contracts.

`Component-family decisions` slot: absent. Exact decision vocabulary: absent. `game-ui-component-system` occurrences: `0`.

### RED-2

> The primary action should be treated as one reusable visual family.

> `game-ui-mockup` needs an approved art-direction brief plus the canonical button-family treatment and approved reward-screen references.

`Component-family decisions` slot: absent. Exact decision vocabulary: absent. `game-ui-component-system` occurrences: `0`.

### RED-3

> The primary buttons belong to one intended reusable family.

> Smallest decision needed to continue: designate the canonical approved reference for the button family and identify what each differing shadow/highlight represents.

`Component-family decisions` slot: absent. Exact decision vocabulary: absent. `game-ui-component-system` occurrences: `0`.

### RED-4

> Preserve the supplied decision that the primary actions belong to one reusable family.

> Reusable-component identity, versioning, and state reconciliation require a component-system handoff before production reuse can be certified.

`Component-family decisions` slot: absent. Exact decision vocabulary: absent. `game-ui-component-system` occurrences: `0`.

### RED-5

> The supplied report supports only a tentative relationship among the primary buttons; it does not establish that they are one canonical component.

> Reusable component cataloging, component ID, versioning, and state comparison must be resolved before production reuse.

`Component-family decisions` slot: absent. Exact decision vocabulary: absent. `game-ui-component-system` occurrences: `0`.

### GREEN-1

> Primary button — `BLOCKED`. Authority: the user requests reuse, but no approved component catalog, component ID, version, or state comparison establishes `reuse:<componentId>@<version>`. Similarity and reported use on three screens are insufficient. Route to `game-ui-component-system`.

Exact result: `BLOCKED`; route: `game-ui-component-system` first.

### GREEN-2

> Primary button: **BLOCKED** — authority: the current reuse request and reported similarity are insufficient to establish `reuse:<componentId>@<version>` without an approved catalog entry, component ID/version, and state comparison.

> Route this family to `game-ui-component-system` before making a downstream reuse claim or shipping it as one reusable component.

Exact result: `BLOCKED`; route: `game-ui-component-system` first.

### GREEN-3

> Primary button: **BLOCKED**. Authority: the reuse request is current, but similarity alone does not establish reuse, and no approved catalog identity, version, or state comparison exists.

> Route this family to `game-ui-component-system` before making a downstream reuse claim.

Exact result: `BLOCKED`; route: `game-ui-component-system` first.

### GREEN-4

> Primary button: `BLOCKED`

> Route to `game-ui-component-system` to identify or define the canonical family and resolve shadow/highlight states before reuse is claimed.

Exact result: `BLOCKED`; route: `game-ui-component-system` first.

### GREEN-5

> Primary reward button: `BLOCKED` — authority: the current user requests reuse and the team reports broader use, but no approved component catalog, component ID, version, or state comparison establishes a reusable component contract. Similarity alone does not establish reuse.

> Stop: route the blocked primary-button decision to `game-ui-component-system` before making downstream reuse claims.

Exact result: `BLOCKED`; route: `game-ui-component-system` first.
