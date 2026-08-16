# DawooLISP

DawooLISP는 토목·CAD 실무에서 반복되는 작업을 빠르고 일관되게 처리하기 위한 통합 LISP 도구 모음입니다. 하나의 배포 파일로 AutoCAD와 ZWCAD 2024를 함께 지원하며 설치, 자동 로드, 메뉴 등록, 업데이트 및 복원 기능을 제공합니다.

## 지원 환경

- AutoCAD 2021 이상 (Windows)
- ZWCAD 2024 (Windows)
- 공용 설치 폴더: `C:\DAWOO\CADLISP`

## 주요 기능

- 토목 도면 작성 및 편집 보조 명령
- 레이어·색상·블록 정리
- 문자·치수·다중지시선 설정
- 거리·축척 계산 및 객체스냅 설정
- 도면 점검·정리·복구
- AutoCAD와 ZWCAD 자동 판별 및 전용 컴파일 파일 로드
- 프로그램 내 자동 업데이트와 이전 버전 복원
- PDF 도움말 및 DawooLISP 메뉴 제공

## 설치 방법

1. [최신 릴리스](https://github.com/leecycle/DawooLISP/releases/latest)에서 `DawooLISP.*.zip`을 내려받습니다.
2. ZIP을 완전히 압축 해제합니다.
3. 압축을 푼 폴더에서 `Install_DawooLISP.cmd`를 실행합니다.
4. 설치가 끝나면 AutoCAD 또는 ZWCAD를 다시 시작합니다.
5. 명령창에서 `DWVER`를 실행해 현재 CAD와 DawooLISP 버전을 확인합니다.
6. `DWHELP`를 실행하면 PDF 도움말이 열립니다.

설치 프로그램은 기존 설정을 지우지 않고 다음 항목을 중복 없이 추가합니다.

- `C:\DAWOO` 및 `C:\DAWOO\CADLISP` 신뢰 경로
- `C:\DAWOO\CADLISP\DawooLISP.lsp` 시작하기 세트
- AutoCAD `acad.pgp` 및 ZWCAD `zwcad.pgp` 단축키
- 현재 CAD에 DawooLISP 메뉴가 없을 때 메뉴 자동 등록

## AutoCAD와 ZWCAD를 함께 사용하는 경우

두 CAD는 같은 `C:\DAWOO\CADLISP` 설치 폴더를 사용합니다.

- AutoCAD에서는 `DawooLISP_*_AutoCAD.VLX`를 자동으로 불러옵니다.
- ZWCAD 2024에서는 `DawooLISP_*_ZWCAD.zelx`를 자동으로 불러옵니다.
- 메뉴 등록 상태는 AutoCAD와 ZWCAD에서 각각 확인하며, 없는 경우에만 자동 등록합니다.
- 한 번 업데이트하면 AutoCAD용과 ZWCAD용 파일이 함께 교체됩니다.

## 업데이트

1. CAD 명령창에서 `DWUPDATE`를 실행합니다.
2. 현재 버전과 GitHub의 최신 정식 릴리스를 비교합니다.
3. 업데이트를 승인한 뒤 도면을 저장합니다.
4. AutoCAD와 ZWCAD를 모두 완전히 종료합니다.
5. 기존 설치 폴더 전체를 백업하고 새 패키지를 검증한 뒤 교체합니다.
6. 실패하면 전체 백업을 자동으로 복원합니다.

업데이트는 기존 신뢰 위치, 시작하기 세트, PGP 단축키, 다른 메뉴 및 작업공간을 변경하지 않습니다. 인터넷 연결 오류 안내는 `DWUPDATE`를 실행했을 때만 표시됩니다.

## 메뉴와 도움말

- `DWTOOLBAR`: DawooLISP 도구막대 표시
- `DWHELP`: PDF 도움말 열기
- `DWUPDATE`: 최신 정식 버전 확인 및 업데이트
- `DWROLLBACK`: 백업된 이전 버전으로 복원
- `DWVER`: 현재 CAD와 설치 버전 확인

전체 명령과 사용 방법은 설치 폴더의 `DawooLISP_Help.pdf`에서 확인할 수 있습니다.

## 주의 사항

- AutoCAD와 ZWCAD가 실행 중일 때 설치 파일을 강제로 교체하지 마십시오.
- LISP 원본은 ANSI(CP949) 인코딩을 유지합니다.
- 배포 ZIP에는 AutoCAD용 VLX와 ZWCAD용 ZELX가 모두 포함되어야 합니다.
- 문제가 생기면 CAD를 종료한 뒤 마스터 설치본으로 다시 설치하거나 `DWROLLBACK`을 사용하십시오.


<!-- Release baseline: v1.4.0 -->
