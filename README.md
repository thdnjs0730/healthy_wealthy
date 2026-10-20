# Wellthy 건강 관리 앱

2024년 학교 팀 프로젝트입니다. 이 저장소에는 Flutter 화면, Node.js 서버와 의약품 관련 자료가 있습니다. 아래 기존 기획의 기능 목록은 실제 구현·운영 완료 여부와 구분해서 읽어 주세요.

## 현재 확인 범위

- 팀원은 김다현·최소원으로 기재되어 있습니다. 개인별 기능 담당 범위는 아직 명시되지 않아 최소원의 단독 성과로 설명하지 않습니다.
- 주요 코드는 lib/, server/, AI/, mySql/에서 확인합니다.
- README의 프로젝트 표기는 Wellthy로 통일했습니다. 기존 패키지·파일 이름은 호환성을 위해 바꾸지 않았습니다.
- 실제 인증·의약품 인식 품질·위치 API·DB 연동의 전체 실행은 이번 정리에서 검증하지 않았습니다.
- Node.js 서버의 DB 접속값은 환경변수로 분리하고 비밀번호를 출력하던 로그를 제거했습니다. 기존 로그인 구현은 학교 실습 수준이며 운영 인증 체계를 완성한 것은 아닙니다.

## 로컬 설정

server/server.js는 DB_HOST, DB_USER, DB_PASSWORD, DB_NAME 환경변수를 읽습니다. [설정 예시](server/.env.example)는 참고용이며 .env를 자동으로 읽지 않습니다. 실제 접속값은 커밋하지 않습니다. 의존성 설치·실행 환경은 별도 확인이 필요합니다.

## 기존 프로젝트 기획과 화면 자료

<div align="center">
<h1>한 손 안에 들어오는 건강, “Wellthy”</h1>
  <div style="text-align: center;">
  <img src="logo/wealthy_wide_logo.png" alt="Wellthy Logo" style="width: 60%; max-width: 300px;">
</div>
Wellthy는 여러분의 건강 관리를 손쉽게 도와주는 종합 건강 관리 어플입니다. <br>
자신의 건강 상태를 기록하고, 처방약 정보를 확인하고, 주변 병원과 약국 위치를 찾아보세요.  <br>
학교 팀 프로젝트의 구현 자료를 정리한 저장소입니다.
</div>

&nbsp;
## 목차
  - [개요](#개요) 
  - [앱 설명](#앱-설명)
  - [주요 기능](#주요-기능)
  - [적용 기술](#적용-기술)
  - [추진 일정](#추진-일정)
  - [팀원](#팀원)
  - [기대효과 및 활용 분야](#기대효과-및-활용-분야)
  - [참고 링크](#참고-링크)

&nbsp;
## 개요
- 프로젝트 이름: Wellthy 🏥
- 프로젝트 지속기간: 2024.04 ~ 2024.10
- 개발 엔진 및 언어: Flutter & Dart
- 백엔드: Flask, Node.js, Firebase
- 멤버: 김다현, 최소원

&nbsp;
## 앱 설명
| ![image](https://github.com/Dahyun1016/healthy_wealthy/blob/main/logo/1.jpeg) | ![image](https://github.com/Dahyun1016/healthy_wealthy/blob/main/logo/2.jpeg) | ![image](https://github.com/Dahyun1016/healthy_wealthy/blob/main/logo/3.jpeg) | ![image](https://github.com/Dahyun1016/healthy_wealthy/blob/main/logo/4.jpeg) | ![image](https://github.com/Dahyun1016/healthy_wealthy/blob/main/logo/5.jpeg) |
|:---:|:---:|:---:|:---:|:---:|
| 홈 화면 | 건강 상태 기록 | 병원 찾기 | 의약품 검색 | 마이페이지 |

Wellthy는 사용자가 건강 상태를 체계적으로 점검하고 필요한 조치를 즉각적으로 취할 수 있도록 도와줍니다.<br>
- **건강 상태 기록**: 오늘의 기분을 기록하고, 건강 상태를 체크할 수 있습니다. 📅
- **의약품 정보 확인**: 약품명을 입력하거나 카메라로 약 사진을 찍어 해당 약물의 정보를 검색할 수 있습니다. 💊
- **주변 병원 및 약국 정보**: 사용자의 현재 위치를 기반으로 주변 약국과 병원의 위치 및 영업시간을 확인할 수 있습니다. 🏥
- **사용자 리뷰**: 섭취 중인 영양제에 대한 다른 사용자의 리뷰를 참고할 수 있습니다. 🌟

&nbsp;
## 주요 기능
- **로그인/회원 가입**: 사용자가 개인 정보를 입력하여 계정을 생성하고 로그인하여 어플을 사용할 수 있습니다.
- **의약품 검색**: 약품명을 입력하거나 카메라로 약 사진을 찍으면 해당 약물의 정보를 검색할 수 있습니다.
- **마이페이지**: 사용자가 자신의 건강 상태를 기록하고 섭취 중인 영양제의 복용 현황을 확인할 수 있습니다.
- **캘린더**: 사용자가 오늘의 기분을 아이콘으로 표시할 수 있습니다.
- **약국 및 병원 정보**: 사용자의 현재 위치를 기반으로 주변 약국과 병원의 위치 및 영업시간을 확인할 수 있습니다.

&nbsp;
## 적용 기술
- **프론트**: Dart, Flutter
- **백엔드**: Flask, Python, Node.js, Firebase
- **DB**: MySQL, SQLite
- **AI**: OpenCV
- **IDE**: VS Code, Google Colab

&nbsp;
## 추진 일정

| 구분   | 추진 내용                   | 추진 일정 | 4월 | 5월 | 6월 | 7월 | 8월 | 9월 | 10월 | 11월 |
|--------|------------------------------|-----------|-----|-----|-----|-----|-----|-----|------|------|
| 계획   | 프로젝트 아이디어 계획 / 설계 |           | 🟢  | 🟢  |     |     |     |     |      |      |
| 분석   | 요구 사항 분석 및 조사        |           | 🟢  | 🟢  |     |     |     |     |      |      |
| 설계   | 시스템 설계 및 UI             |           |     | 🟢  | 🟢  |     |     |     |      |      |
| 개발   | 프론트 개발                  |           |     |     | 🟢  | 🟢  |     |     |      |      |
|        | 백엔드 개발                  |           |     |     | 🟢  | 🟢  |     |     |      |      |
|        | 서버 연결                    |           |     |     |     | 🟢  | 🟢  |     |      |      |
| 테스트 | 기능 테스트 및 디버깅         |           |     |     |     |     | 🟢  | 🟢  |      |      |
| 종료   | 최종 점검 및 발표 계획        |           |     |     |     |     |     | 🟢  | 🟢  |      |
| 오프라인 | 미팅 계획                   |           | 🟢  | 🟢  | 🟢  | 🟢  | 🟢  | 🟢  | 🟢  | 🟢  |

&nbsp;

## 팀원

- ![Dahyun1016](https://img.shields.io/badge/GitHub-Dahyun1016-black)
- ![thdnjs0730](https://img.shields.io/badge/GitHub-thdnjs0730-black)

&nbsp;

## 기대효과 및 활용 분야
## 기대효과
- 사용자 건강 관리의 편리성 증대
- 의약품 정보 접근성 향상
- 종합적인 건강 관리 지원
- 의료 서비스 접근성 개선
- 사용자 만족도 및 참여도 증가

&nbsp;

### 활용 분야
- 의료 기관 및 약국
- 기업 직원 건강 관리
- 공공 보건 기관
- 건강 관련 연구 및 개발

&nbsp;

## 참고 링크
- https://educoder.tistory.com/entry/Flutter-%EA%B4%80%EB%A0%A8-%EB%A7%81%ED%81%AC-%EB%AA%A8%EC%9D%8C-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC-%EA%B4%80%EB%A0%A8
- 알약 API https://nedrug.mfds.go.kr/pbp/CCBGA01/getItem?totalPages=4&limit=10&page=2&&openDataInfoSeq=11
- Flutter 관련 링크 모음 https://educoder.tistory.com/entry/

&nbsp;

---

&nbsp;


