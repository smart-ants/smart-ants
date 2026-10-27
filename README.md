# SAQ Windows 자동 실행기 배포

[자동 시작 파일 다운로드](https://github.com/smart-ants/smart-ants/raw/refs/heads/saq-delivery-20261027/SAQ_START.cmd)

[설치 ZIP 다운로드](https://github.com/smart-ants/smart-ants/raw/refs/heads/saq-delivery-20261027/SAQ_INSTALLER.zip)

실행 파일을 Windows에서 한 번 열면 기본 폴더 `C:\SAQ_AUDIT\DOWNLOADS`를 만들고
내장 ZIP 저장, 탐색기 열기, 압축 해제, 실행 화면 열기와 흩어진 SAQ ZIP 정리를 진행합니다.
저장 위치는 화면에서 변경하고 기억할 수 있습니다.

- ZIP은 복사 후 해시를 확인한 뒤 원래 위치에서 제거하며 중복은 별도 이름으로 보존합니다.
- 인증키·DB·백업·V7 운영 폴더는 제외합니다. 접근/검색 제한은 미확인으로 기록합니다.
- 1 TEST → PASS → 2 자동 백업·독립 API 코드 적용 → 3 결과 확인 순서입니다.
- 실패 시 자동 원복하고 검증하며, 복구를 완료하지 못하면 복구 필요 상태를 표시합니다.
- 원본 Stage10, 운영 DB, 차트·CSS와 P9/P10 보관 패치는 적용하지 않습니다.

Python 3.11 이상(Tk 포함)이 필요하며 전체 TEST에는 실행 중인 Docker Linux 엔진과
PyPI/Docker Hub 연결이 필요합니다. 전역 Python/Docker를 자동 설치하지 않습니다.
준비 미완료·실패·건너뜀은 STOP이며 적용 버튼이 열리지 않습니다.

검증: Linux 실행기 39개 통과, 실제 임시 PostgreSQL 백엔드 56개 통과(별도 두 실행),
신규 설치·적용 실패 시 정확한 백업/원복, 업로드 원본을 보존한 P9·HF1 임시 복사본 이동 확인.
Windows PowerShell/탐색기/Tk UI는 아직 실행 검증하지 않았습니다. 사용자 PC에도 아직 미적용입니다.
실데이터 수집·운영 DB 연결·운영 배포 완료를 의미하지 않습니다.

SHA-256은 `SAQ_INSTALLER_SHA256.json`, 상세 근거는 `TEST_REPORT.md`에 있습니다.
이 브랜치는 배포 파일만 포함한 독립 이력이며 기존 main과 작업 디렉터리는 변경하지 않았습니다.
저장소가 비공개이면 이 저장소에 접근 가능한 GitHub 계정으로 로그인해서 받으세요.
