# Phase 2 — AI를 활용한 개발 역량 강화

## 목표

- "AI 앱 개발·배포 초급" 수준에서 벗어나 AI를 실무 도구로 능숙하게 활용
- AI 인프라(모델 서빙, RAG, 에이전트 아키텍처)에 대한 구조적 이해 확보

> **ai_3 연동**: GPU/AI 인프라 실습(Phase 3)이 `~/project/ai_3`(로컬 경로, 별도 저장소)에서 상당 부분 진행됨. `[ai_3]` 표시 항목 참고, 근거는 `~/project/ai_3/PROGRESS.md`.

## 체크리스트

- [x] AI 코딩 도구(Claude Code 등) 매일 실무/사이드 프로젝트에 사용 습관화
  - 완료내용: TA_project 저장소와 ai_3 홈랩 프로젝트 모두 Claude Code로 진행하며 매일 사용하는 습관이 이미 자리잡음.
  - 자료: [Claude Code 공식 문서](https://docs.claude.com/claude-code)
- [ ] LLM 기본 개념 정리 (토큰, 컨텍스트, 임베딩, 파인튜닝 vs 프롬프팅)
  - 아직 이론 정리 전 — ai_3에서도 실습(Ollama 서빙) 위주로 진행되어 개념 정리가 남은 과제
  - 자료: [Anthropic 공식 문서](https://docs.claude.com)의 Prompt engineering 섹션
  - 영상(검색): Andrej Karpathy "Let's build GPT", 3Blue1Brown "But what is a GPT?"
- [x] 간단한 AI 애플리케이션 직접 설계·배포 (API 연동 → 배포까지 1개 이상 완주)
  - 완료내용: Ollama로 소형 LLM(qwen2:0.5b)을 k3d 클러스터에 K8s Service로 서빙하고, 실제 추론 결과까지 검증함.
  - 자료: [Anthropic API 문서](https://docs.claude.com)의 Quickstart
- [ ] RAG(검색증강생성) 파이프라인 구조 학습 및 미니 실습
  - 아직 미진행 — ai_3도 RAG는 다루지 않음, 순수하게 남은 과제
  - 자료: [Anthropic — Building effective agents](https://www.anthropic.com/research/building-effective-agents), [LangChain RAG 튜토리얼](https://python.langchain.com), [Pinecone Learn](https://www.pinecone.io/learn/)
- [ ] AI 에이전트/멀티에이전트 아키텍처 개념 학습
  - 아직 미진행 — 남은 과제
  - 자료: [Anthropic — Building effective agents](https://www.anthropic.com/research/building-effective-agents), [Claude Agent SDK 문서](https://docs.claude.com)
- [x] 모델 서빙/추론 인프라(GPU 리소스, 배치 vs 실시간) 개요 학습
  - 완료내용: NVIDIA GPU Operator는 실제 GPU가 없어 매니페스트 작성 수준의 개념 학습으로 진행했고, Prometheus+Grafana로는 실제 리소스 모니터링 대시보드까지 구축함.
  - 책: 『Designing Machine Learning Systems』(Chip Huyen) — 서빙 관련 챕터
  - 자료: AWS SageMaker 또는 GCP Vertex AI 공식 개요 페이지
- [x] 학습한 내용을 [docs/current-project-ai-usage.md](../docs/current-project-ai-usage.md)와 연결해 실무 사례로 기록
  - 완료내용: KORUS 프로젝트에서의 Claude 활용 사례(DB 마이그레이션 이슈 해결, 애플리케이션 개발 보조, 포트폴리오 작성)를 docs/current-project-ai-usage.md에 작성 완료함.

## 메모

<!-- 사용해본 도구, 막힌 부분, 다음에 시도할 것 등을 기록 -->

- 2026-07-07: ai_3에서 Ollama 기반 LLM K8s 서빙 + 모니터링까지 실습 완료 확인. 남은 것은 LLM 이론 정리, RAG, 에이전트 아키텍처 학습 — 순수 신규 학습 과제.
