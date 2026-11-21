---
document_id: DOC-003
document_type: screen_description
feature_id: FEAT-001
update_id: UPD-003
version_policy: legacy
version: "v.3.9"
wireframe_version: "v.3.9"
---

# 직무 찾기 화면 설명

- 원문: [직무 찾기 Section](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4112)
- 선택 페이지: `v.3.9 (26.09.23)`
- 화면 연결: [wireframe.json](wireframe.json) · [elements.json](elements.json)

## 진입 경로와 권한

### 진입 경로

[랜딩페이지] > ‘테스트 시작하기’ 버튼 클릭 시
네비바 ‘직무 찾기’ 탭 클릭 시
Footer ‘직무 찾기’ 버튼 클릭 시

[원문](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4679)

### 권한

로그인 상태의 사용자: 모든 권한
비로그인 상태의 사용자: [직무 찾기 - 결과] 페이지 내 일부 콘텐츠 조회 불가

[원문](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4681)

## 화면 목록

| 화면 ID | 화면 | Figma |
| --- | --- | --- |
| `SCR-001` | 직무 찾기 - 메인 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4410) |
| `SCR-002` | 직무 찾기 - 전공 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4113) |
| `SCR-003` | 직무 찾기 - 흥미 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4235) |
| `SCR-004` | 직무 찾기 - 가치관 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4184) |
| `SCR-005` | 직무 찾기 - 대기 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4213) |
| `SCR-006` | 직무 찾기 - 결과 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4436) |
| `SCR-007` | 직무 찾기 - 결과 공유 | [화면](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4700) |

## SCR-001 · 직무 찾기 - 메인

### 0. 기능 진입 시 표시할 페이지

저장된 테스트 결과가 있는 로그인 상태의 사용자
: [직무 찾기 - 결과]
비로그인 또는 저장된 테스트 결과가 없는 로그인 상태의 사용자
: [직무 찾기 - 메인]

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4605)

### 1. ‘테스트 시작하기’ 버튼

클릭 시 [직무 찾기 - 전공] 페이지로 이동한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4612)

## SCR-002 · 직무 찾기 - 전공

### 1. 전공 태그

클릭 시 해당 태그가 선택 상태로 전환되며,
선택된 태그를 다시 클릭하면 해당 태그가 미선택 상태로 전환된다.
선택된 태그가 있는 상태로 다른 태그를 클릭하면
기존에 선택된 태그는 미선택 상태로 전환되고,
새로 선택된 태그가 선택 상태로 전환된다. 
최대 1개의 태그를 선택할 수 있다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4620)

### 2. ‘다음 단계로 →’ 버튼

클릭 시 [직무 찾기 - 흥미] 페이지로 이동한다.

선택된 태그가 존재하는 경우 버튼이 활성화되며,
모든 태그가 미선택 상태인 경우 버튼이 비활성화된다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4627)

## SCR-003 · 직무 찾기 - 흥미

### 1. 흥미 테스트 문항

각 문항이 가지는 5단계의 응답 중 하나씩만 선택 가능하다.
해당 문항에 선택된 응답이 있는 상태로 다른 응답을 클릭하면
기존에 선택된 응답은 미선택 상태로 전환되고,
새로 선택된 응답이 선택 상태로 전환된다.

한 문항에 응답한 직후, 응답이 없는 상태인 문항 중 가장 상단에 위치한 문항으로 자동 스크롤 한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4651)

### 2. ‘다음 단계로 →’ 버튼

클릭 시 [직무 찾기 - 가치관] 페이지로 이동한다.

모든 문항에 대한 응답이 존재하는 경우 버튼이 활성화되며,
하나의 문항이라도 응답이 존재하지 않는 경우 버튼이 비활성화된다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4659)

## SCR-004 · 직무 찾기 - 가치관

### 1. 가치관 밸런스게임 카드

클릭 시 해당 카드가 선택되며, 다음 문항을 표시한다.
마지막 문항의 카드 클릭 시 [직무 찾기 - 대기] 페이지로 이동한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4636)

### 2. ‘이전 문항’ 텍스트 버튼

첫 번째 문항에는 표시하지 않고, 두 번째 문항부터 마지막 문항까지 표시한다.
클릭 시 이전 문항을 표시하며, 해당 문항의 모든 카드를 미선택 상태로 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4643)

## SCR-005 · 직무 찾기 - 대기

### 0. 페이지 이탈

로그인한 사용자가 [직무 찾기 - 대기] 페이지에서 이탈해도 작업을 계속하고, 저장한다.

[직무 찾기 - 전공], [직무 찾기 - 흥미], [직무 찾기 - 가치관] 페이지에서 사용자가 이탈하면 로그인 여부와 관계 없이 내용을 저장하지 않는다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4668)

## SCR-006 · 직무 찾기 - 결과

### 결과 저장

로그인 사용자의 결과는 저장한다.
사용자가 테스트를 다시 시작하는 경우 이전의 결과를 폐기한다.
비로그인 사용자의 결과는 저장하지 않는다.
[직무 찾기 - 결과] 페이지 내의 ‘로그인하고 결과 확인하기’ 버튼을 통해 로그인을 진행하고 이전 페이지로 돌아오는 경우, 이전의 결과를 저장하여 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4845)

### 0. 결과 텍스트

결과에 따라 달리 표시하는 텍스트는 직무 찾기 DB를 따른다.
(직무 찾기 DB 바로가기)

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4851)

### 1. 사용자 이름

로그인 상태: 계정 이름 표시
비로그인 상태: ‘OOO’ 표시

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4858)

### 2. 제목 영역

사용자의 ‘{1순위 근무 조건 텍스트}\n{흥미 유형 1순위 텍스트} 인재’로 구성한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4865)

### 3. 전공 영역

사용자가 선택한 전공 태그 내의 텍스트를 표시한다.
선택한 태그가 ‘전공과 관계없이 찾기’인 경우, ‘무관’으로 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4872)

### 4. 흥미 유형 영역

사용자의 흥미 유형 그래프와 1순위 흥미 유형 설명을 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4879)

### 5. ‘전체 유형별 특성 보기’ 버튼

클릭 시 전체 유형 모달 (3-1)을 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4886)

### 5-1. 전체 유형 모달

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4893)

### 6. 선호 근무 조건 영역

사용자의 선호 근무 조건을 순위대로 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4898)

### 7. 직무 카드

로그인 상태: 전체 내용을 확인할 수 있다.
비로그인 상태: 비로그인 직무 카드 (5-1)와 같이 표시한다.
직무명과 아코디언 내의 내용은 Blur 처리하며, 적합도 태그는 표시한다.
’로그인하고 결과 확인하기’ 버튼 클릭 시 [로그인] 페이지로 이동한다.

아코디언을 통해 전체 내용을 확인할 수 있으며, default는 아코디언이 닫힌 상태로 한다.
적합도 태그 내의 변수에는 해당 직무에 대한 사용자의 최종 점수 x100을 표시한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4905)

### 7-1. 비로그인 직무 카드

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4913)

### 8. 기업 형태 카드

로그인 상태: 전체 내용을 확인할 수 있다.
비로그인 상태: 비로그인 기업 형태 카드 (6-1)와 같이 표시한다.
기업 형태명과 아코디언 내의 내용은 Blur 처리한다.
’로그인하고 결과 확인하기’ 버튼 클릭 시 [로그인] 페이지로 이동한다.

아코디언을 통해 전체 내용을 확인할 수 있으며, default는 아코디언이 닫힌 상태로 한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4918)

### 8-1. 비로그인 기업 형태 카드

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4926)

### 9. 경험 정리 소개 영상

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4931)

### 10. ‘경험 정리 시작하기’ 버튼

로그인 상태로 클릭 시 [경험 정리 - 맵뷰] 페이지로 이동한다.

비로그인 상태로 클릭 시 로그인 안내 모달 (공통 5)을 표시하고, [로그인] 페이지로 이동한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4936)

### 11. ‘결과 공유하기’ 버튼

로그인 상태로 클릭 시 공유 링크를 생성하고, 클립보드에 링크를 복사하며 링크 복사 토스트 메세지 (11-1)을 표시한다.
공유 링크 클릭 시 [직무 찾기 - 결과 공유] 페이지 (11-2)가 표시되며, ‘직무 찾기 테스트 시작하기’ 버튼 (11-3) 이하의 내용은 [직무 찾기- 결과] 페이지와 동일하게 표시한다. 단, 로그인하지 않아도 모든 내용이 표시된다.
‘직무 찾기 테스트 시작하기’ 버튼 (11-3) 클릭 시 [직무 찾기 - 전공] 페이지로 이동한다.

비로그인 상태로 클릭 시 로그인 안내 모달 (공통 5)을 표시하고, [로그인] 페이지로 이동한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4944)

### 11-1. 링크 복사 토스트 메세지

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4952)

### 11-2. [직무 찾기 - 결과 공유] 페이지

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4957)

### 11-3. ‘직무 찾기 테스트 시작하기’ 버튼

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4962)

### 12. ‘테스트 다시 하기’ 버튼

클릭 시 현재 저장된 테스트 결과를 폐기하고, [직무 찾기 - 메인] 페이지로 이동한다.

[Figma 설명](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4967)

## SCR-007 · 직무 찾기 - 결과 공유

표시 범위와 테스트 시작 버튼 동작은 결과 화면의 **11. ‘결과 공유하기’ 버튼** 항목 참조.

## 결과 화면 보조 요소

### 전체 유형 모달

현장형 (R)

분명하고, 체계적인 것을 좋아하고, 도구나 기계를 조작하는
활동이나 기술에 흥미가 있어요.

탐구형 (I)

창작형 (A)

공감형 (S)

추진형 (E)

체계형 (C)

관찰적, 체계적이며 물리적, 생물학적, 문화적 현상의 창조적인
탐구를 수반하는 활동에 흥미가 있어요.

예술적 창조와 표현, 변화와 다양성을 선호하고 틀에 박힌 것을
싫어하며 모호하고, 자유롭고, 상징적인 활동에 흥미가 있어요.

타인의 문제를 듣고, 이해하고 ,도와주고, 함께하는 활동에
흥미가 있어요.

조직의 목적과 경제적인 이익을 얻기 위해 타인을 지도, 계획,
통제, 관리하는 일과 그 결과로 얻어지는 명예, 인정, 권위에
흥미가 있어요.

정해진 원칙과 계획에 따라 자료를 기록, 정리, 조직하는 일을
좋아하고 체계적인 작업환경에서 사무적, 계산적 능력을
발휘하는 활동에 흥미가 있어요.

전체 유형별 특성

[Figma 모달](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-5004)

### 링크 복사 토스트

공유 링크가 복사되었어요.

[Figma 토스트](https://www.figma.com/design/190ub4CA8flVwOniEWAXRd?node-id=1677-4974)
