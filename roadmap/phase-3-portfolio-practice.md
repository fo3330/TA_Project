# Phase 3 — AI+Cloud 결합 실전/포트폴리오 구축

## 목표

- Phase 1·2에서 쌓은 역량을 하나의 실전 프로젝트/포트폴리오로 통합
- 아키텍처 설계 문서를 실제로 작성해보며 TA 직무에 요구되는 산출물 형태에 익숙해지기

> **ai_3 연동**: 이 Phase의 상당 부분이 `~/project/ai_3`(로컬 경로, 별도 저장소)의 "AI 인프라 아키텍트" 홈랩 프로젝트로 이미 진행됨. `[ai_3]` 표시 항목 참고, 근거는 `~/project/ai_3/PROGRESS.md`, `~/project/ai_3/homelab/phase4-integration/architecture.md`.

## 체크리스트

- [x] 포트폴리오용 프로젝트 주제 선정 (AI 워크로드를 Cloud 위에 설계·배포하는 형태)
  - `[ai_3]` "홈랩(Colima+k3d) → Terraform으로 클라우드 확장 → K8s 오케스트레이션 → GPU 노드에서 소형 오픈소스 LLM 서빙 → Prometheus/Grafana 모니터링"으로 이미 주제 확정 및 구현
- [x] 아키텍처 설계 문서(ADR, 시스템 다이어그램 등) 작성 연습
  - `[ai_3]` ADR 3건(Colima+k3d 선택, NFS 트러블슈팅, LocalStack 대체) + 통합 아키텍처 다이어그램 작성 완료
  - 자료: ADR 템플릿 — GitHub에서 "architecture-decision-record" 검색, 다이어그램 기법: [C4 model](https://c4model.com)
- [ ] 선정 프로젝트를 실제로 클라우드에 배포 (비용/가용성/보안 트레이드오프 문서화)
  - 지금까지는 로컬(Colima/k3d)과 LocalStack(가상 AWS)로만 진행됨 — **실제 AWS 계정으로의 재검증이 아직 남은 과제**
  - 방법: [AWS Free Tier](https://aws.amazon.com/free) 한도 내에서 진행, 예산 초과 방지를 위해 AWS Budgets 알림 설정
- [x] 현재 업무 프로젝트의 AI 활용 경험을 포트폴리오 스토리로 재구성
  - KORUS 프로젝트 기준으로 이미 작성 완료
  - 참고: [docs/current-project-ai-usage.md](../docs/current-project-ai-usage.md) 및 대시보드 입력 내용
- [ ] 포트폴리오/블로그/GitHub 형태로 외부 공개 가능한 산출물 정리
  - ai_3는 로컬 git init만 되어 있고 **원격 저장소 push가 아직 안 됨** — 가장 먼저 처리할 만한 항목
  - 배포: GitHub Pages 또는 Netlify
  - README 작성 참고: GitHub에서 "awesome-readme" 검색
- [ ] 자격증 취득 진행 (해당 시)
  - `[ai_3]` CKA, AWS SAA(또는 AZ-305)를 목표로 설정했으나 아직 응시 전
  - 참고: [docs/learning-resources.md](../docs/learning-resources.md)의 자격증 후보 표

## 메모

<!-- 프로젝트 진행 중 겪은 설계 고민, 트레이드오프 판단 근거 등을 기록 -->

- 2026-07-07: ai_3가 사실상 이 Phase의 실전 프로젝트 그 자체임을 확인. 남은 핵심 과제 3가지: (1) ai_3를 GitHub 원격 저장소에 push, (2) LocalStack이 아닌 실제 AWS 계정으로 재검증, (3) CKA/AWS SAA 응시.
