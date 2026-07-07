# Technical Architect / Solutions Architect 이직 로드맵 & 학습관리

AI 및 Cloud 환경 설계를 중심으로 하는 **Technical Architect(TA)** 및 **Solutions Architect(SA)** 직무로 이직하기 위한 개인 준비 저장소입니다. 두 직무는 요구 기술 스택이 70~80% 이상 겹치는 것으로 확인되어(→ [docs/role-definition.md](docs/role-definition.md) §2) 함께 준비합니다.
문서 기반으로 학습 로드맵, 주간 기록, 역량 격차, 참고자료를 한 곳에서 관리합니다.

## 목표 요약

- **목표 직무**: Technical Architect **및** Solutions Architect (AI + Cloud 환경 설계 중심, 두 직무 모두 지원 대상)
- **학습 기간**: 별도 마감 없음 — **TA/SA 직종으로 이직할 때까지** 지속
- **현재 상태**: 시스템 엔지니어 5년차 (시스템 운영 3년 + 인프라 구축 사업 2년)
- **핵심 취약점**: (1) Cloud 환경 구조 자체가 생소함 (2) AI를 활용한 개발 경험이 초급 수준 — 상세는 [docs/skill-gap.md](docs/skill-gap.md)
- **TA vs SA 차이**: 기술 스택은 거의 동일, 방향성만 다름(TA=구현 중심, SA=고객/비즈니스 중심) — 상세는 [docs/role-definition.md](docs/role-definition.md) §2
- **경력/배경**: [self-intro-draft.md](self-intro-draft.md), 요약은 [reference/career-background.md](reference/career-background.md) 참고

## 폴더 구조

| 폴더 | 용도 |
|---|---|
| [docs/](docs/) | TA 직무 정의, 역량 격차 분석, 학습자료 목록, 현재 프로젝트 AI 활용 기록 |
| [roadmap/](roadmap/) | 단계(Phase)별 로드맵 및 체크리스트 |
| [study-log/](study-log/) | 주간/일일 학습 기록 |
| [reference/](reference/) | 경력 배경 요약, 원본 참고자료 색인 |
| [dashboard/](dashboard/index.html) | 읽기 전용 정적 대시보드 (진행률 관제판) |

## 앱 (대시보드)

[dashboard/index.html](dashboard/index.html)을 브라우저로 열면 이 저장소의 모든 내용(홈 요약, 로드맵, 직무 정의, 역량 격차, 경력 배경, 학습자료, 현재 프로젝트 AI 활용 기록)을 **탭으로 넘겨보는 하나의 앱**으로 확인할 수 있습니다. 서버 없이 파일을 더블클릭해서 열면 됩니다.

- **홈**: 학습 경과일, 전체 로드맵 진행률, 가장 가까운 목표일을 한눈에
- **로드맵**: 학습 경과일 입력, 스스로 설정한 목표일(포트폴리오 완성/첫 지원/이직) D-day, Phase 1~4 체크리스트
- **직무 정의 / 역량 격차 / 경력 배경 / 학습자료**: 각 `docs/`·`reference/` 문서 내용을 보기 좋게 정리해서 표시 (원본 문서 링크 포함)
- **현재 프로젝트 AI 활용**: 프로젝트 개요와 AI 활용 내역을 직접 입력하는 폼 — `docs/current-project-ai-usage.md`를 채우기 전에 여기서 먼저 기록해도 됨
- 입력·체크한 내용은 즉시 저장되고 반영됩니다.
- 데이터는 브라우저의 **localStorage**에 저장됩니다(파일을 다시 열어도 유지, 단 브라우저/기기를 바꾸면 안 남음). 하단 "백업 내보내기"로 JSON 파일을 받아두고, 필요할 때 "백업 가져오기"로 복원하세요.

## 사용법

1. 매주 `study-log/`에 그 주 학습 기록을 새 파일로 추가 (템플릿: [study-log/template.md](study-log/template.md))
2. `roadmap/` 각 phase 파일의 체크리스트를 진행 상황에 맞춰 갱신
3. 현재 진행 중인 프로젝트에서의 AI 활용 사례를 파악되는 대로 [docs/current-project-ai-usage.md](docs/current-project-ai-usage.md)에 상세히 기록
4. 새로운 학습자료·정보를 확인하면 [docs/learning-resources.md](docs/learning-resources.md)와 [reference/source-materials.md](reference/source-materials.md) 갱신

## 주의사항

- 이 저장소는 이직 시점이 고정되어 있지 않은 자기주도 학습 프로젝트입니다. `roadmap/`의 Phase는 순서상 가이드일 뿐 실제 진행 속도와 상황에 맞춰 자유롭게 조정하세요.
- 이 문서들은 2026.7.6 기준으로 작성된 초안이며, 학습을 진행하며 계속 갱신할 것.
