# Phase 1 — Cloud 환경 구조 기초 다지기

## 목표

- Cloud 환경 자체에 대한 생소함 해소 (최대 취약점)
- 최소 1개 클라우드 벤더의 핵심 서비스를 스스로 설명할 수 있는 수준 도달

> **ai_3 연동**: 이 Phase의 실습 상당 부분이 별도 저장소 `~/project/ai_3`(홈랩 프로젝트, 로컬 경로 — 별도 git 저장소라 GitHub에서는 링크가 열리지 않음)에서 이미 진행됨. 아래 체크 항목에 `[ai_3]` 표시된 것은 그쪽 실습 결과를 근거로 완료 처리. 상세 근거는 `~/project/ai_3/PROGRESS.md`.

## 체크리스트

- [x] 학습 우선 벤더 선정 (AWS / GCP / Azure 중 1개, 근거는 [docs/role-definition.md](../docs/role-definition.md)에 기록)
  - `[ai_3]` AWS로 결정 (LocalStack으로 VPC/EC2/S3 실습, AWS SAA를 목표 자격증으로 설정)
  - 자료: [AWS Free Tier](https://aws.amazon.com/free), [GCP 무료 프로그램](https://cloud.google.com/free), [Azure 무료 계정](https://azure.microsoft.com/free)
- [ ] IaaS/PaaS/SaaS 개념 및 클라우드 공동 책임 모델 학습
  - 자료: AWS Skill Builder의 **Cloud Practitioner Essentials**(무료, [skillbuilder.aws](https://skillbuilder.aws)) 또는 Google Cloud **Cloud Digital Leader** 학습경로([cloudskillsboost.google](https://www.cloudskillsboost.google))
  - 아직 이론 학습은 진행 전 — ai_3는 실습 위주로 먼저 진행됨, 개념 정리가 남은 과제
- [x] 컴퓨트(VM/컨테이너/서버리스) 핵심 서비스 학습
  - `[ai_3]` Colima+Docker로 컨테이너 실습 완료(nginx 볼륨, Compose 웹앱), LocalStack으로 EC2 개념 실습
  - 자료: [AWS 공식 Getting Started 가이드](https://aws.amazon.com/getting-started/)로 EC2/Lambda/ECS 직접 실습
  - 선행: 컨테이너 개념이 낯설면 [Docker 공식 튜토리얼](https://docs.docker.com/get-started/)부터
- [x] 네트워크(VPC, 서브넷, 로드밸런서, DNS) 핵심 개념 학습
  - `[ai_3]` LocalStack VPC 실습 + k3d 클러스터에 Calico CNI 설치, NetworkPolicy로 트래픽 차단까지 실증
  - 자료: [AWS VPC 사용 설명서](https://docs.aws.amazon.com/vpc/)
  - 방법: 기존 실무 네트워크 지식(서브넷팅, 방화벽 등)과 1:1로 매핑해서 정리하면 습득이 빠름
- [x] 스토리지(오브젝트/블록/파일) 및 데이터베이스 서비스 개요 학습
  - `[ai_3]` S3(LocalStack), MinIO(오브젝트 스토리지 실제 구축), PV/PVC(local-path StorageClass)까지 실습
  - 자료: S3/EBS/EFS, RDS/DynamoDB — [AWS 공식 Getting Started 가이드](https://aws.amazon.com/getting-started/)의 각 서비스 페이지
- [ ] IAM/보안 기초 (권한, 정책, 네트워크 보안그룹)
  - 아직 미진행 — ai_3에서도 NetworkPolicy 수준만 다뤘고 IAM 자체는 다루지 않음
  - 자료: [AWS IAM 모범사례](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html), [AWS Well-Architected Framework — Security Pillar](https://aws.amazon.com/architecture/well-architected/)
- [x] IaC 개념 및 Terraform 등 도구 하나 맛보기 실습
  - `[ai_3]` Terraform으로 Docker Compose 스택 코드화 + LocalStack 대상 VPC/EC2/S3 생성·삭제 실습 완료
  - 자료: [Terraform 공식 튜토리얼](https://developer.hashicorp.com/terraform/tutorials)
  - 책: 『Terraform: Up & Running』(Yevgeniy Brikman)
- [ ] 선택한 벤더의 입문 자격증 취득 여부 결정 및 진행
  - AWS SAA로 방향은 정했으나(`[ai_3]` ROADMAP.md) 아직 응시 전 — 남은 과제
  - 자료: [AWS Certified Cloud Practitioner 시험 가이드](https://aws.amazon.com/certification/certified-cloud-practitioner/)

## 메모

<!-- 학습하며 알게 된 사실, 막힌 개념, 온프레미스 경험과의 비교 등을 기록 -->

- 2026-07-07: ai_3 홈랩 프로젝트(Colima+k3d+Terraform+LocalStack)로 실습 상당수 완료 확인. 남은 것은 이론 학습(IaaS/PaaS 개념, IAM)과 실제 AWS 계정으로의 재검증, AWS SAA 응시.
