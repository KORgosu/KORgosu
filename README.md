<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=16&pause=1000&color=378ADD&center=true&vCenter=true&width=500&lines=Cloud+%2F+DevOps+Engineer;Infrastructure+Automation;Container+Orchestration+%26+GitOps)](https://git.io/typing-svg)

# 박수환 · Park Su Hwan

![Sejong](https://img.shields.io/badge/Sejong_University-003893?style=flat-square)
![AutoEver](https://img.shields.io/badge/Hyundai_AutoEver_Cloud_Track-0076A8?style=flat-square)

</div>

---

### 🎓 Education & Career

| 구분 | 활동 | 비고 | 기간 |
|------|------|------|------|
| ![B.S.](https://img.shields.io/badge/B.S.-378ADD?style=flat-square&logoColor=white) | 세종대학교 지능기전공학부 스마트기기공학 | Smart Device Engineering | 2019.03 ~ 2025.02 |
| ![군복무](https://img.shields.io/badge/군복무-5F5E5A?style=flat-square&logoColor=white) | 대한민국 공군 — 군사경찰 · 보안관제 | ROKAF Military Police | 2019.08 ~ 2021.05 |
| ![융합전공](https://img.shields.io/badge/융합전공-7F77DD?style=flat-square&logoColor=white) | 엔터테인먼트 소프트웨어 | Entertainment Software | 2021.06 ~ 2025.02 |
| ![교육](https://img.shields.io/badge/교육-D24939?style=flat-square&logoColor=white) | 현대오토에버 Mobility SW School — Cloud Track | Cloud Engineering | 2025.04 ~ 2025.11 |

---

### 🚀 Projects

#### 💱 MSA 실시간 환율 웹 서비스
> 4인 팀 프로젝트 · DevSecOps/PM 담당 · 2025

실시간 환율 데이터 파이프라인을 MSA + EKS 기반으로 설계·운영.  
5개 서비스(Frontend + Backend 4개), Kafka 이벤트 스트리밍, Redis 캐싱.  
보안을 설계 초기부터 내재화한 DevSecOps 파이프라인 구축.  

**CI/CD · GitOps**
  - Jenkins Golden AMI 도입 → Worker 프로비저닝 60초 → 20초 (66% 단축)
  - Master-Worker 분리 + AutoScaling → 월 비용 $60 → $30 (50% 절감)
  - ArgoCD GitOps (ServerSideApply + selfHeal) — 클러스터 상태를 git이 단일 진실 원천으로 관리

**공급망 보안 (Supply Chain Security)**
  - Jenkins 파이프라인에 Trivy SBOM(CycloneDX) 생성 + CRITICAL 취약점 자동 차단 스테이지 추가
  - ECR Enhanced Scanning (AWS Inspector v2 CONTINUOUS_SCAN) — 전 레포지토리 상시 스캔

**제로트러스트 네트워크**
  - Calico NetworkPolicy 12개 (default-deny 기반 최소 권한) — 서비스 간 허용 트래픽만 명시
  - PSA enforce:restricted — API 서버 레벨 비준수 파드 배포 차단

**컨테이너 보안 하드닝**
  - 전 워크로드에 runAsNonRoot, readOnlyRootFilesystem, capabilities.drop:ALL, seccompProfile:RuntimeDefault 적용
  - IRSA(IAM Roles for Service Accounts) — 파드 단위 최소 권한 IAM, 노드 IAM 미사용

**시크릿 관리**
  - ESO(External Secrets Operator) + AWS Secrets Manager — DB 엔드포인트·API 키 git 미노출
  - GitOps 파이프라인 전 구간에서 평문 시크릿 없음

**관측성 · 위협 탐지**
  - GuardDuty 8종 탐지 활성화 (CloudTrail, EKS Audit, Runtime Monitoring 포함)
  - Prometheus PrometheusRule 16개 (안정성 8 · 보안 4 · Kafka 4) + AlertManager Slack 연동
  - Grafana 대시보드 3종 (Stability / Security / Kafka) — 이상 Egress·CPU Throttle 보안 지표 포함
  - Fluent Bit → CloudWatch Logs 4계층 수집 (애플리케이션 30일 / 인프라·호스트 14일)

**인프라 최적화**
  - VPC CNI Prefix Delegation → 노드당 Pod 17 → 110개 (6.5배 확장)
  - EKS 컨트롤 플레인 로깅 5종 전체 활성화 + API 서버 CIDR 제한
  - Prometheus 기반 메트릭 리소스 최적화 (메모리 여유 2.6Gi 확보)

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/KORgosu/trip-currency)

---

#### 🎮 언리얼엔진5 인터랙티브 소프트웨어
> 개인 프로젝트 · 2024.05 ~ 2024.06

Cinema4D 3D 모델링 + Unreal Engine 5 실시간 이펙트 + TouchDesigner OSC 통신 연동.  
Xbox 패드로 실시간 디스플레이 제어 가능한 인터랙티브 파이프라인 구현.

- UDP 기반 OSC 프로토콜로 Unreal Engine ↔ TouchDesigner 클라이언트 통신 구현
- 렌더링 거리 및 에셋 최적화로 주사율 드롭 문제 해결

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/KORgosu/Unreal_IATD)

---

#### 🕹 뱀서라이크 게임 개발 (웅진씽크빅 챌린지)
> 3인 팀 프로젝트 · 개발/PM 담당 · 2023.06 ~ 2023.08

Unity 기반 뱀서라이크 장르 게임 기획 및 개발.  
Jira/Confluence 기반 스크럼 운영, GitHub 버전 관리, C# 스크립트 작성.

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/KORgosu/UnityProject_TeamNJPD)

---

### 🛠 Tech Stack

**Cloud & DevOps**  
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat-square&logo=argo&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![OpenStack](https://img.shields.io/badge/OpenStack-ED1944?style=flat-square&logo=openstack&logoColor=white)

**Embedded & Systems**  
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-003153?style=flat-square)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white)

**Languages & Etc.**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![Unreal](https://img.shields.io/badge/Unreal%20Engine-0E1128?style=flat-square&logo=unrealengine&logoColor=white)

---

### 🏅 Certifications

![AWS SAA](https://img.shields.io/badge/AWS_SAA-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![정보처리기사](https://img.shields.io/badge/정보처리기사-0076A8?style=flat-square)
![SQLD](https://img.shields.io/badge/SQLD-003B57?style=flat-square)
![네트워크관리사 2급](https://img.shields.io/badge/네트워크관리사_2급-5F5E5A?style=flat-square)

---

### 📊 GitHub Stats

<div align="center">

![GitHub stats](https://github-readme-stats.vercel.app/api?username=KORgosu&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Streak](https://streak-stats.demolab.com?user=KORgosu&theme=tokyonight&hide_border=true)

</div>

---

### 📫 Contact

[![Tistory](https://img.shields.io/badge/Tistory-FF6B00?style=flat-square&logo=tistory&logoColor=white)](https://nexon25.tistory.com)
[![Velog](https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@nexon257/series)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/korgosu/)
[![Email](https://img.shields.io/badge/nexon257@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white)](mailto:nexon257@naver.com)
