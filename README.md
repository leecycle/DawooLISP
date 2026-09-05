# DawooLISP

DawooLISP는 토목·CAD 실무에서 반복되는 작업을 빠르고 일관되게 처리하기 위한 AutoLISP 통합 도구입니다. 하나의 설치 파일로 AutoCAD와 ZWCAD 2024를 지원하며 자동 로드, 메뉴·도구막대·리본, 업데이트와 복원 기능을 제공합니다.

## 현재 버전

- 정식버전: [DawooLISP 2.0.0](https://github.com/leecycle/DAWOO-LISP/releases/tag/v2.0.0)
- 공개베타: [DawooLISP 2.0.1](https://github.com/leecycle/DAWOO-LISP/releases/tag/v2.0.1)
- 공용 설치 폴더: `C:\DAWOO\DAWOO-LISP`

## 지원 환경

- AutoCAD 2015~2024 (Windows)
- ZWCAD 2024 (Windows)
- DWVW DLL 빌드 기준: AutoCAD 2021 / ZWCAD 2024 Professional

## 설치

1. [Releases](https://github.com/leecycle/DAWOO-LISP/releases)에서 원하는 버전의 `DawooLISP.*.zip`을 내려받습니다.
2. ZIP을 완전히 압축 해제합니다.
3. AutoCAD와 ZWCAD를 모두 종료합니다.
4. 압축을 푼 폴더의 `Install.exe`를 실행합니다.
5. CAD를 다시 시작하고 `DWOP`에서 설치 버전을 확인합니다.

배포 ZIP에는 `Install.exe`와 `README.txt`만 포함됩니다.

## 설치 모드와 백업

설치기는 현재 상태에 따라 다음과 같이 동작합니다.

- 신규 설치: 새 설치 경로가 없으면 시작세트·신뢰 경로·PGP를 등록합니다.
- 2.x 업데이트: `C:\DAWOO\DAWOO-LISP`가 있으면 기존 CAD 등록과 사용자 UI 배치를 유지합니다.
- 1.x 마이그레이션: 새 경로가 없고 `C:\DAWOO\CADLISP\DawooLISP.lsp`가 있으면 DawooLISP의 시작 경로만 새 경로로 연결합니다.

백업은 서로 섞이지 않게 분리합니다.

- 2.x 업데이트: `%LOCALAPPDATA%\DAWOO\DAWOO-LISP\Backup\2.x`
- 1.x 마이그레이션: `%LOCALAPPDATA%\DAWOO\DAWOO-LISP\Backup\Migration-1.x`

1.x 구버전 폴더는 삭제하거나 덮어쓰지 않습니다. 1.x 백업을 2.x 설치 경로로 자동 복원하지 않으며 DawooCivilLISP와 다른 시작세트 항목도 변경하지 않습니다.

## 주요 기능

- 토목 도면 작성·편집 보조
- 레이어·색상·블록 정리
- 문자·치수·다중지시선 및 주석 축척 설정
- 거리·축척 계산과 객체스냅 설정
- 도면 점검·정리·복구
- 수치지도·연속지적도·지번 정리·SHP 내보내기
- VWorld 위성영상 다운로드 및 CAD 좌표 삽입
- AutoCAD/ZWCAD 자동 판별과 전용 VLX/ZELX 로드
- PDF 도움말, 메뉴·도구막대·리본 제공
- 정식/공개베타 업데이트 채널과 이전 2.x 버전 복원

## 주요 명령

- `DEF`, `DEFST`, `DEFDIM`, `DEFLA`, `DEFSC`, `DEFCTB`: 기본 환경·문자·치수·레이어 설정
- `DWSCL`, `DWOS`, `DWJ`, `DWSTA`: 축척·객체스냅·선 연결·측점 작성
- `DWNUM`, `DWJS`, `DWJI`, `DWJIA`, `DWSHP`, `DWVW`: 공간정보 도구
- `DWCL`, `DWAUD`, `DWPP`, `DWRECOV`: 도면 점검과 복구
- `DWTOOLBAR`, `DWRIBBONLOAD`: 도구막대와 리본 표시
- `DWOP`, `DWUPDATE`, `DWROLLBACK`, `DWHELP`: 설치·업데이트·복원·도움말

전체 명령과 사용법은 설치 폴더의 `DawooLISP_Help.pdf`에서 확인할 수 있습니다.

## 2.0.1 공개베타

- 검증된 2.0.0 정식판 기능을 유지합니다.
- 1.x 기존 사용자의 새 설치 경로 마이그레이션을 지원합니다.
- 시작세트에서는 DawooLISP 구 경로만 새 경로로 교체합니다.
- AutoCAD와 ZWCAD의 신뢰 경로 및 자동 로드 구성을 적용합니다.
- 1.x 마이그레이션 백업과 2.x 업데이트 백업을 완전히 분리합니다.

문제가 발생하면 CAD를 종료한 뒤 설치 폴더와 백업을 보존하고, 공개베타 릴리스 설명과 `README.txt`를 확인해 주세요.
