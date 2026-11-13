# 이도훈

**Android Developer | 신입 개발자**

[GitHub](https://github.com/0rchid241) · [Resume](https://github.com/0rchid241/resume)

---

## Profile | 소개

서경대학교 소프트웨어학과 재학 중이며 Kotlin 기반 Android 앱 개발을 경험했습니다. AI 도구를 활용한 개인 캡스톤에서 금융 알림 수집·Room 저장·Compose 화면 연동을 진행하고, 실제 기기에서 동작을 확인했습니다.

## Skills | 프로젝트 사용 기술

| 분류 | 기술 |
| --- | --- |
| **Android** | Kotlin · Android SDK · Jetpack Compose · Room · Coroutines · DataStore · 홈 화면 위젯 |
| **Web / CI·CD** | Java · Spring Boot · Docker · GitLab CI/CD |
| **Tools** | Android Studio · Git · GitHub |

## Projects | 프로젝트 경험

### 01. 금융 알림 기반 개인 지출 관리 시스템

**개인 캡스톤 · 2026.09 - 2026.10 (MVP 개발 완료)**

**Kotlin / Room / Jetpack Compose / Android SDK**

금융 앱의 입출금·결제 알림을 거래 데이터로 변환해 지출 내역을 관리하는 Android 앱입니다.

- **알림 수집 및 정규화:** 카카오뱅크 입출금 알림을 수집하고, 거래 유형·금액·상대방·잔액 등을 추출해 Room에 저장하는 기능을 구현했습니다.
- **거래 관리 및 규칙:** 거래 조회·추가·수정·삭제, 중복·내부이체·취소/환불 후보 검토, 금액·상대방 조건의 소비 규칙 기능을 구성했습니다.
- **삼성 월렛 파서:** 실제 결제 알림 형식의 금액·가맹점을 추출하고, 포인트 적립 알림을 거래에서 제외하는 처리를 추가했습니다.
- **실기기 확인:** 카카오뱅크 입출금 및 삼성 월렛 결제 알림을 직접 확인하고, 앱의 거래 저장·표시 흐름을 검증한 뒤 기능을 병합·업데이트했습니다.

**GitHub:** [finance-notification-expense-manager](https://github.com/0rchid241/finance-notification-expense-manager)

### 02. 커뮤니티 웹 서비스 및 CI/CD 파이프라인 구축

**SW 인재양성 프로그램 · 팀 프로젝트**

**Java / Spring Boot / React / Docker / GitLab CI/CD**

- **사용자 인증:** Spring Boot 기반 회원가입·로그인과 JWT 인증, Google·Naver·Kakao 소셜 로그인 및 계정 관리 API를 담당했습니다.
- **게시판 API 개선:** 게시글 검색·카테고리·조회수 정렬·페이지네이션을 구현하고, 댓글 작성 권한 확인 과정에 캐싱을 적용했습니다.
- **CI/CD 구축:** Backend·Frontend GitLab CI 설정을 공통 배포 저장소와 연결하고, Docker 이미지 빌드·Registry·Compose 배포 흐름을 구성했습니다.
- **배포 문제 해결:** Runner·Registry 인증, 서버 경로와 줄바꿈, OAuth 콜백·Nginx 설정 문제를 다루고 Blue/Green 배포 연동에 참여했습니다.

### 03. 로스트아크 생명의 기운 계산 및 위젯 앱

**개인 프로젝트 · 2026.11 ~**

**Kotlin / Android / Jetpack Compose / DataStore**

로스트아크의 생명의 기운 회복 상태와 완충까지 남은 시간을 확인할 수 있는 Android 앱입니다.

- **회복량 계산:** 사용자가 입력한 생명의 기운과 마지막 갱신 시각을 기준으로 경과 시간에 따른 회복량을 계산하고 최대치 제한을 적용했습니다.
- **완충 예상 시간:** 현재 상태를 바탕으로 생명의 기운이 가득 차는 예상 시간을 계산했습니다.
- **설정 유지:** DataStore에 입력 정보를 저장해 앱 종료 후에도 상태를 유지하도록 했습니다.
- **홈 화면 위젯:** 앱을 열지 않아도 생명의 기운을 확인할 수 있도록 위젯을 구성하고 자동 갱신을 적용했습니다.
- **문제 해결:** 앱에서는 값이 갱신되지만 위젯에 이전 값이 남는 문제를 확인하고, 회복량 계산과 위젯 상태 갱신의 역할을 분리해 자동 갱신 동작을 수정했습니다.

**GitHub:** [loa-energy](https://github.com/0rchid241/loa-energy)

## Education | 학력

**서경대학교 소프트웨어학과** · 학사과정 재학 · 졸업예정
