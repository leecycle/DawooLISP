# DawooLISP

DawooLISP는 토목·CAD 실무에서 반복되는 작업을 빠르고 일관되게 처리하기 위한 통합 LISP 도구 모음입니다. 하나의 배포 파일로 AutoCAD와 ZWCAD 2024를 모두 지원하며 설치, 자동 로드, 업데이트까지 간편하게 사용할 수 있도록 구성했습니다.

## 지원 환경

- AutoCAD 2015~2024 (Windows)
- ZWCAD 2021~2024 (Windows)
- 설치 폴더: `C:\DAWOO\CADLISP`

## 주요 기능

- 토목 도면 작성 및 편집 보조 명령
- 레이어·색상·블록 정리 기능
- 치수와 다중지시선 관련 도구
- 거리와 축척 계산 도구
- 자주 사용하는 CAD 명령 단축키 (PGP등록)
- 프로그램 내 자동 업데이트 확인
- PDF 도움말 제공

## 설치 방법

1. [Releases](https://github.com/leecycle/DawooLISP/releases/latest)에서 최신 `DawooLISP.*.zip`을 내려받습니다.
2. 압축을 푼 뒤 `Install_DawooLISP.cmd`를 실행합니다.
3. AutoCAD 또는 ZWCAD를 다시 시작합니다.
4. 명령창에서 `DWHELP`를 입력하면 PDF 도움말이 열립니다.

설치 프로그램은 다음 설정도 자동으로 처리합니다.

- 기존 설치 파일 백업 후 최신 파일로 교체
- `C:\DAWOO\...`를 CAD의 신뢰할 수 있는 경로에 추가
- `C:\DAWOO\CADLISP\DawooLISP.lsp`를 APPLOAD 시작하기 세트에 등록
- AutoCAD와 ZWCAD 사용자 프로파일에 중복 없이 적용
