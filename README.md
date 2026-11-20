# 이도훈

**Android Developer | 신입 개발자**

[GitHub](https://github.com/0rchid241) · [Resume](https://github.com/0rchid241/resume)

---

## Profile | 소개

서경대학교 소프트웨어학과에서 소프트웨어 개발을 공부하며 Kotlin 기반 Android 애플리케이션을 개발해 왔습니다.

금융 앱의 알림을 거래 데이터로 변환하는 지출 관리 앱과 시간 기반 회복량 계산·홈 화면 위젯을 제공하는 앱을 개발했습니다. 알림 처리, 로컬 데이터 저장, 백그라운드 작업, 실제 기기 동작 확인을 경험했습니다.

또한 대학·기업 협력형 SW 아카데미 클라우드/백엔드 교육과정에서 Java·Spring 및 클라우드·DevOps 기술을 학습하고, 팀 프로젝트에서 GitLab CI/CD와 Docker 빌드 환경 구성, 컨테이너 모니터링 작업에 참여했습니다.

## Skills | 기술 스택

| 분야 | 기술 |
| --- | --- |
| Android | Kotlin, Android SDK, Jetpack Compose, Material 3 |
| 데이터·비동기 | Room, SQLite, Preferences DataStore, Kotlin Coroutines, Flow |
| Android 기능 | NotificationListenerService, Jetpack Glance, WorkManager |
| 백엔드·DevOps | Java, Spring Boot, GitLab CI/CD, Docker, Docker Compose, Bash |
| 개발 도구 | Android Studio, Gradle, Git, GitHub |

## Projects | 프로젝트 경험

### 01. 금융 알림 기반 개인 지출 관리 시스템

**개인 캡스톤 프로젝트 | 2026.09 ~ 2026.10 | MVP 개발 완료**

`Kotlin` `Jetpack Compose` `Room` `NotificationListenerService`

금융 앱의 비정형 알림을 거래 데이터로 변환하여 지출 내역을 관리할 수 있도록 개발한 Android 앱입니다.

**주요 구현 내용**

- `NotificationListenerService`를 이용한 카카오뱅크·삼성 월렛 알림 수집
- 앱별 알림 형식에서 거래 유형·금액·상대방 등의 정보를 추출해 공통 거래 모델로 정규화
- 미인식 알림과 제외 대상 알림을 구분하여 잘못된 거래 생성 방지
- Room을 이용한 거래 저장·조회·추가·수정·삭제 및 월간 지출 집계
- 중복·내부이체·환불 가능 거래를 후보로 탐지하고 사용자가 검토하는 기능 구현
- Jetpack Compose 기반 거래 조회·관리 화면 구성

**개발 및 검증 경험**

- 금융 앱마다 다른 알림 형식을 별도 파서로 분리하여 처리
- 파싱 실패 시 원본 알림과 처리 상태를 보존하도록 구성
- 실제 Android 기기에서 지원되는 알림의 수신·거래 저장·화면 표시 과정 확인
- 단위 테스트 및 GitHub Actions를 활용한 빌드 검증

**GitHub:** [finance-notification-expense-manager](https://github.com/0rchid241/finance-notification-expense-manager)

### 02. LOA Energy — 로스트아크 생명의 기운 계산기

**개인 프로젝트 | 2026.11 ~ | 핵심 MVP 구현 완료·안정화 진행 중**

`Kotlin` `Jetpack Compose` `DataStore` `Glance` `WorkManager`

시간에 따라 회복되는 게임 자원의 예상 수치와 완충 시간을 계산하고 Android 홈 화면 위젯에서 확인할 수 있도록 개발한 앱입니다.

**주요 구현 내용**

- 입력한 생명의 기운과 기록 시각을 기준으로 경과 시간에 따른 회복량 계산
- 10분당 30 회복 규칙과 최대치 제한 적용
- 완충까지 남은 자원량·예상 소요 시간·예상 시각 표시
- Preferences DataStore를 이용한 기준 수치 및 기록 시각 저장·복원
- Jetpack Glance 기반 홈 화면 위젯과 WorkManager 주기적 갱신 요청 구현

**개발 및 문제 대응 경험**

- Coroutine을 이용해 앱 화면의 예상 생기 주기적 갱신
- 앱과 위젯이 동일한 DataStore 기록을 사용하도록 구성
- 위젯에 이전 수치가 표시되는 문제에 대응하여 DataStore 변경 감지와 위젯 갱신 흐름 수정
- Android 백그라운드 실행 정책에 따른 갱신 지연을 고려하여 갱신 요청 구조 구성

**GitHub:** [loa-energy](https://github.com/0rchid241/loa-energy)

### 03. 서경인사이드 — 커뮤니티 웹 서비스 CI/CD 구축

**SW 아카데미 팀 프로젝트 | 2026.04 ~ 2026.06**

`Java` `Spring Boot` `React` `GitLab CI/CD` `Docker` `Docker Compose` `Bash`

Spring Boot 백엔드와 React 프론트엔드로 구성된 커뮤니티 웹 서비스의 빌드·배포 환경을 구축하는 팀 프로젝트에 참여했습니다.

**개인 담당 역할**

- GitLab CI에서 백엔드 Docker 이미지 빌드 및 Container Registry 업로드 설정
- Gradle Wrapper 실행 권한 및 CI Runner 아키텍처 설정 변경
- Docker-in-Docker 서비스 선언 구조 수정
- `docker stats` 기반 컨테이너 CPU·메모리 사용률 및 PIDs 수집 스크립트 개발
- Docker Compose 환경의 Redis 접속 주소 및 HikariCP 연결 풀 설정 수정

**팀 프로젝트 전체 구현 범위**

- Spring Boot·React 기반 커뮤니티 웹 서비스 개발
- Docker Compose를 이용한 테스트·서비스 환경 구성
- Nginx 및 Blue/Green 방식의 서비스 전환 스크립트 구성
- 백엔드 헬스체크를 통한 배포 대상 상태 확인

**GitHub:** [서경인사이드 CI/CD 및 배포 환경](https://github.com/0rchid241/SW_Project_CICD_Deploy)

## Education | 학력

**서경대학교 소프트웨어학과** · 학사과정 재학 · 졸업예정

## Training | 전문 교육 이수

### 서경대학교 대학·기업 협력형 SW 아카데미

**클라우드/백엔드 SW 개발자 교육과정 | 2026.01 ~ 2026.06**

- **운영기관:** 서경대학교 산학협력단 · 서경 SW 아카데미 사업단
- **교육기관:** (주)비트컴퓨터
- **교육 형태:** 전일제 집중교육, 코딩테스트 교육 및 기업 제안 과제 기반 팀 프로젝트
- **공식 과정 규모:** 사전교육 포함 20주·780시간 / 필수교육 18주·720시간 (아카데미 안내자료 기준)

**교육 일정**

| 구분 | 기간 | 내용 |
| --- | --- | --- |
| 사전교육 | 2026.01.19 ~ 01.30 | 프로그래밍 기초 |
| 본교육 | 2026.02.02 ~ 04.02 | 클라우드/백엔드 전문 기술 교육 |
| 코딩테스트 교육 | 2026.04.03 ~ 04.09 | 알고리즘 및 문제 해결 |
| 프로젝트 개발·평가 | 2026.04.10 ~ 06.18 | 기업 제안 과제 기반 팀 프로젝트, 최종 평가 및 수료식 |

**주요 교육 내용**

| 분야 | 교육과정 |
| --- | --- |
| 프로그래밍 | Java 프로그래밍, 자료구조 및 알고리즘 |
| 데이터베이스 | MySQL, Oracle, JDBC |
| 백엔드 개발 | Servlet/JSP, Spring Core, Spring MVC, JDBC & JPA |
| 서버 및 네트워크 | Linux 서버 구축, 네트워크, 클라우드 아키텍처 |
| Spring·MSA | Spring Security, Spring Batch, Spring Cloud, MSA 구성 |
| 컨테이너·DevOps | Docker, Kubernetes, 클라우드·DevOps 아키텍처 |
| 코딩테스트 | 알고리즘 문제 해결 및 모의 코딩테스트 |

**팀 프로젝트 경험**

기업 제안 과제를 바탕으로 진행한 커뮤니티 웹 서비스 프로젝트에서 GitLab CI/CD 파이프라인 설정, Docker 빌드 환경 구성, 컨테이너 자원 모니터링 및 서비스 연결 설정을 담당했습니다.

**관련 프로젝트:** [서경인사이드 CI/CD](https://github.com/0rchid241/SW_Project_CICD_Deploy)
