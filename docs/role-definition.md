# Technical Architect & Solutions Architect (AI + Cloud) 직무 정의

> 2026-07 기준 실제 채용공고·공식 프레임워크 리서치로 보강. 계속 업데이트할 것.

## 1. 직무 개요

전통적으로 온프레미스 조직의 기술 아키텍처 팀은 Technical Architect(인프라), Solutions Architect(소프트웨어), Data Architect, Network Architect, Security Architect로 역할이 나뉘는 경우가 많다. 반면 AWS 등 클라우드 네이티브 조직은 이 역할들을 "Solutions Architect" 한 타이틀로 통합해서 부르는 경향이 있다.

이 저장소는 원래 국내 채용시장에서 실제 쓰이는 **"테크니컬 아키텍트"**(대규모 시스템의 아키텍처 총괄, 안정성·성능·확장성 책임)와 **"AI/클라우드 아키텍트"**(AI/ML 설계·운영, 클라우드 기반 하이브리드 아키텍처)가 합쳐진 하이브리드 포지션을 목표로 시작했다. 2026-07 리서치 결과 TA와 SA는 요구 기술 스택이 70~80% 이상 겹치는 것으로 판단되어(§2 참고), **TA·SA 두 트랙을 함께 준비**하는 것으로 범위를 넓혔다.

## 2. TA vs SA — 무엇이 다른가

같은 기술 기반 위에서 **방향(orientation)이 다른 역할**이다.

| | Technical Architect | Solutions Architect |
|---|---|---|
| 시선 방향 | 내부(구현) 중심 | 외부(고객/비즈니스) 중심 |
| 역할 | 실제로 시스템을 어떻게 구성할지 설계·구현 (예: EC2 구축, 오토스케일링, Redis 캐시, WAF 설정) | 비즈니스 요구에 맞는 솔루션 제안, PoC·데모 리딩, 영업 조직과 협업 |
| 깊이 vs 넓이 | 특정 기술을 깊게 (EA보다 좁고 깊음) | 비즈니스 이해 비중이 큼, 여러 솔루션을 조합 |
| 소속(국내 관례) | 개발팀/구축팀과 밀착 | AWS 등에서는 세일즈 조직 산하인 경우가 많음 (프리세일즈 성격) |
| 산출물 | 구현 표준, 시스템 구성 | 제안서, 데모, 아키텍처 옵션 비교 |

**기술 스킬셋은 70~80% 이상 겹친다.** 다른 건 "누구를 보고 일하느냐"— TA는 시스템/구현을 보고, SA는 고객/비즈니스를 보고 일한다. 실제 채용시장에서는 회사마다 이 구분이 느슨해서(특히 클라우드 벤더는 SA로 통합) 공고 제목만으로 역할을 단정하기보다 본문의 실제 업무 내용을 봐야 한다.

**이 저장소의 결론**: Phase 1~3 로드맵(Cloud 기초·AI 활용·포트폴리오)은 TA·SA 어느 쪽이든 그대로 유효하다. 차이는 Phase 4(이직 준비)에서 SA 쪽에 무게를 둘 경우 "고객 커뮤니케이션·PoC/데모 리딩·프레젠테이션" 역량을 추가로 연습해야 한다는 점뿐이다 → [roadmap/phase-4-job-transition.md](../roadmap/phase-4-job-transition.md) 참고.

## 3. 실제 채용공고 기반 요구 역량

### 국내

- **테크니컬 아키텍트** (금융권 SI 등): 계정계·채널계를 포함한 전사 IT 구조 최적화, 표준 아키텍처 원칙 수립, 클라우드·분산처리·보안 프레임워크 등 신기술 검증·도입
- **AI 클라우드 아키텍트**: AI/ML 분석 모델 설계·구현·운영 경험, 클라우드 기반 AI/ML 분석 경험 3년 이상, 산업공학·컴퓨터공학·전기전자·수학·통계 등 유관 전공 우대
- **클라우드 아키텍트** (대기업): IaaS/PaaS/SaaS + On-Premise 하이브리드 아키텍처 구축 경험, 빅데이터(분산처리·데이터레이크·AI) 구성 경험, 대규모 트래픽·고가용성(HA) 아키텍처 설계·운영 역량
- **솔루션 아키텍트(SA)**: 고객 비즈니스 요구사항 분석 및 솔루션 제안, PoC/데모 리딩, 프리세일즈 지원 (국내 클라우드 벤더는 세일즈 조직 산하인 경우가 많음)

### 해외 (참고)

- **Cloud AI Architect**: AI/ML 시스템 아키텍처 설계(데이터 파이프라인, 모델 배포 전략), 도구·플랫폼 선정, ML 모델 개발·훈련 총괄, 엔터프라이즈 시스템 통합. 최근에는 AI 파이프라인 보안(모델 훈련 권한 관리, 추론 엔드포인트 보호, AI 연동 데이터 저장소 보안)까지 책임 범위가 확장되는 추세
- **AI/LLM Solutions Architect**: RAG·스트리밍 파이프라인 등 시스템 아키텍처 설계, 프롬프트 엔지니어링, 외부 도구·API 통합, 평가·모니터링(트레이싱, 드리프트 감지)

## 4. 요구 기술 스택 정리

- **공통 인프라 (TA/SA 공통)**: 멀티클라우드(AWS/Azure/GCP) 실무 경험, Python, Terraform 등 IaC, Docker/Kubernetes, 네트워킹, 보안
- **AI/ML 특화 (TA/SA 공통)**: 데이터 파이프라인 설계, 모델 서빙/배포, RAG 아키텍처, LLM 생태계 이해, MLOps 기초
- **소프트 스킬 (공통)**: 이해관계자 커뮤니케이션, 설계 문서화(ADR 등), 의사결정 근거 제시, 비즈니스 요구사항 ↔ 기술 구조 번역 능력
- **SA 특화 차별점**: 고객 대상 프레젠테이션·데모 리딩, PoC 기획·진행, 제안서 작성, 프리세일즈 커뮤니케이션

## 5. 강점으로 연결되는 지점

- 시스템 운영 3년 + 인프라 구축 사업 2년 → 온프레미스 인프라·네트워크·스토리지 구조에 대한 실무 감각은 Cloud 아키텍처 학습의 기반
- U2L(Unix to Linux) 전환 트러블슈팅 경험 → 이기종 시스템 마이그레이션 설계 역량과 연결
- 경력 상세: [../reference/career-background.md](../reference/career-background.md)

## 6. 참고할 수 있는 페이지

### 공식 아키텍처 프레임워크

- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/) — AWS 기준 아키텍처 설계 원칙(운영 우수성, 보안, 안정성, 성능, 비용, 지속가능성)
- [Google Cloud Architecture Framework](https://docs.cloud.google.com/architecture/framework) — GCP 기준 5대 원칙(운영 우수성, 보안/프라이버시/컴플라이언스, 안정성, 비용 최적화, 성능 최적화)
- [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/) — Azure 기준 설계 패턴·모범사례 모음
- [TOGAF](https://www.opengroup.org/togaf) — 전통적 엔터프라이즈 아키텍처 표준 프레임워크 (국내 대기업 채용공고에서 종종 언급됨)

### 학습 로드맵

- [roadmap.sh — AWS](https://roadmap.sh/aws)
- [roadmap.sh — AI Engineer](https://roadmap.sh/ai-engineer)
- [roadmap.sh — AI Agents](https://roadmap.sh/ai-agents)

### 직무 이해 아티클

- [Coursera — Cloud Architect Career Guide](https://www.coursera.org/articles/cloud-architect)
- [Coursera — What Is an AI Architect?](https://www.coursera.org/articles/ai-architect)
- [Medium — What is the role of an AI Solutions Architect?](https://medium.com/ai-ml-genai-solution-architecture/what-is-the-role-of-an-ai-solutions-architect-in-2025-a417446a3d8f)
- [Indeed — Solution Architect vs. Technical Architect: Key Differences](https://www.indeed.com/career-advice/finding-a-job/solution-architect-vs-technical-architect)
- [Interview Kickstart — Enterprise vs Solution vs Technical Architect](https://interviewkickstart.com/blogs/articles/enterprise-architect-vs-solution-architect-vs-technical-architect)
- [이랜서 블로그 — TA, DA, QA, BA, SA 소프트웨어 아키텍처의 역할별 차이 이해하기](https://www.elancer.co.kr/blog/detail/829)

### 자격증 공식 페이지

- [AWS Certified Solutions Architect – Associate](https://aws.amazon.com/certification/certified-solutions-architect-associate/)
- [Google Cloud — Professional Cloud Architect](https://cloud.google.com/certification/cloud-architect)
- [Microsoft — Azure Solutions Architect Expert](https://learn.microsoft.com/en-us/credentials/certifications/azure-solutions-architect/)

### 국내 채용공고 탐색 (실제 요구사항 직접 확인용)

- [원티드](https://www.wanted.co.kr)
- [사람인](https://www.saramin.co.kr)
- [잡코리아 — "클라우드아키텍트" 검색](https://www.jobkorea.co.kr/Search/?stext=%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C%EC%95%84%ED%82%A4%ED%85%8D%ED%8A%B8)

> 링크는 2026-07 기준으로 확인한 공식/안정적 페이지입니다. 세부 페이지 구조는 시간이 지나며 바뀔 수 있으니, 안 열리면 도메인에서 직접 검색하세요.

## 7. 검증이 필요한 질문 (남은 과제)

- [x] "AI Solutions Architect"류 직무와 전통적 TA의 차이 정리 — §2에서 정리 완료 (2026-07-07)
- [ ] 실제 채용공고 5~10건(TA + SA 모두 포함)을 직접 수집해 요구 스킬·자격증·경력 연차를 표로 정리
- [ ] AWS/GCP/Azure 중 우선 학습할 벤더 선택 근거 마련 (국내 채용공고에서는 AWS/네이버클라우드 비중이 높은 편 — 실제 통계로 재확인 필요)
- [ ] 목표 회사/업계군 후보 리스트업 (스타트업 vs 대기업 vs 클라우드 벤더 vs 금융권 SI, TA·SA 포지션 모두 포함)
- [ ] SA 쪽을 병행할 경우 포트폴리오/자기소개서에 "고객 커뮤니케이션·PoC 리딩" 사례를 어떻게 넣을지 결정
