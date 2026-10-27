# SAQ Windows 자동 실행기 1.0.1

[새 자동 시작 ZIP 다운로드](https://github.com/smart-ants/smart-ants/raw/refs/heads/saq-delivery-20261027/SAQ_START_1_0_1.zip)

기존 창을 닫고 ZIP 안의 SAQ_START.cmd를 실행하세요. 지정 폴더 생성, 내장 패키지 저장·압축 해제,
실행 화면 열기가 이어집니다. 기본 저장 폴더는 `C:\SAQ_AUDIT\DOWNLOADS`입니다.

## DOCKER_REQUIRED 수정

이 코드는 ChatGPT/Codex 결제 오류가 아니라 Docker 실행 파일을 찾지 못했다는 뜻입니다.
새 버전은 PATH와 Windows 머신/사용자 기본 설치 경로를 함께 검색합니다.
설치된 Docker Desktop이 꺼져 있으면 정상 실행하고 로컬 Linux 엔진 준비를 기다립니다.

Docker가 없으면 새 화면의 **Docker 준비**를 누르세요. 공식 Windows 아키텍처용 설치 파일을
기억한 폴더에 자동 다운로드하고, Docker Inc의 유효한 Authenticode 서명을 확인한 뒤에만
**공식 설치 실행** 버튼을 활성화합니다. 설치 실행 직전 서명과 해시를 다시 확인합니다.
설치 약관·관리자 권한·WSL·재시작은 공식 화면에서 사용자가 직접 선택해야 합니다.
Docker가 준비되면 원래 창의 **1 실행 TEST**를 다시 누르세요.

1 TEST → 실제 PASS → 2 백업 후 독립 API 코드 적용 → 성공 시 3 결과물 확인 순서입니다.
실패하면 원복하고 확인합니다. 원복까지 실패하면 복구 필요로 표시합니다.
최근 24시간 안에 ZIP 전체 정리가 완료됐으면 과거 기록을 표시하고 반복 검색을 생략합니다.
새 ZIP 전체 검색은 **ZIP 다시 정리**를 누르세요. 동일 이름 ZIP은 덮어쓰지 않습니다.

## 검증과 범위

실행기 검사 53개 통과. 실제 임시 PostgreSQL 백엔드 56개 통과(독립 두 실행), 신규 설치와
고의 실패 시 정확한 원복 검증. 기존 사용자 화면에서는 ZIP 161개 이동과 API 적용 STOP을 확인했습니다.
새 Docker 준비 화면·공식 설치 파일 다운로드·Windows 서명 검증·설치는 아직 Windows에서 실행하지 못했습니다.
클라우드에서 공식 설치 파일 접근은403이었으며 사용자 PC의 다운로드 가능 여부를 의미하지 않습니다.

원본 Stage10, 운영 DB, 키, 차트·CSS, 보관 P9/P10 패치는 적용하지 않습니다.
실데이터 수집이나 운영 DB 연결·배포 완료가 아닙니다. main은 변경하지 않은 별도 배포 브랜치입니다.
SHA-256은 SAQ_INSTALLER_SHA256.json, 상세 근거는 TEST_REPORT.md에 있습니다.
저장소가 비공개이면 접근 가능한 GitHub 계정으로 로그인하세요.
