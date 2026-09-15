# works

업무 과정에서 사용하는 웹 기반 도구와 검증용 유틸리티를 모아 관리하는 저장소입니다.

## GitHub Pages

이 저장소는 `main` 브랜치의 `/ (root)`를 GitHub Pages 소스로 사용하는 것을 기준으로 구성합니다.

- Repository: `mycodehive/works`
- Pages base URL: `https://mycodehive.github.io/works/`
- Launcher: `index.html`

## 공통 상단 메뉴

모든 하위 애플리케이션은 `/common/`의 공통 내비게이션을 사용합니다.

- `common/header.html` — 메뉴 마크업 및 앱 링크
- `common/header.css` — PC/모바일 공통 메뉴 스타일
- `common/header.js` — 메뉴 로딩, 현재 페이지 활성화, 모바일 메뉴 동작

하위 애플리케이션의 공개 `index.html`은 공통 메뉴와 기존 앱 화면을 결합하는 진입점이며, 기존 앱 본체는 각 폴더의 `app.html`에 보존합니다. 따라서 공통 메뉴는 한 곳에서 관리하고 각 앱의 기존 기능은 그대로 유지할 수 있습니다.

## Applications

### 1. Cross-verification-of-labor-cost-payment-plan

연구인력 월별 인건비 지급계획과 계약관리 데이터를 교차 검증하는 웹 도구입니다.

주요 기능:
- `contractsubject`, `joinlist`, `ingcontract`, `currentemp` Excel 업로드
- 진행중 과제 및 재직자 기준 필터링
- 직번·과제번호·지급년도 기준 교차 검증
- 월별 지급액/예정액 불일치 확인
- 계약정보 누락 및 참여인력 미등록 확인
- 검증 결과 CSV / Excel 다운로드

실행 주소: `https://mycodehive.github.io/works/Cross-verification-of-labor-cost-payment-plan/`

### 2. excel-merge

같은 레이아웃을 가진 여러 Excel 파일을 브라우저에서 하나의 XLSX 파일로 병합하는 도구입니다.

주요 기능:
- `.xls`, `.xlsx` 파일 병합
- 여러 줄 헤더 및 셀 스타일·병합 셀 최대한 보존
- `0`으로 시작하는 문자열 열의 앞자리 0 보존
- 사용자 지정 다운로드 파일명 + 자동 `.xlsx`
- 서버 업로드·저장 없음

실행 주소: `https://mycodehive.github.io/works/excel-merge/`

### 3. image-optimizer-pro

이미지를 브라우저에서 변환·리사이즈·압축하고 결과를 내려받는 이미지 최적화 도구입니다.

주요 기능:
- JPG / PNG / WebP 변환
- 이미지 리사이즈 및 품질 압축
- 목표 파일 용량 기준 압축
- 개별 다운로드 및 ZIP 일괄 다운로드
- 서버 업로드·저장 없이 브라우저 내부 처리

실행 주소: `https://mycodehive.github.io/works/image-optimizer-pro/`

## 폴더 구조

```text
works/
├── README.md
├── index.html
├── common/
│   ├── header.html
│   ├── header.css
│   └── header.js
├── Cross-verification-of-labor-cost-payment-plan/
│   ├── index.html
│   ├── app.html
│   └── xlsx.full.min.js
├── excel-merge/
│   ├── index.html
│   └── app.html
└── image-optimizer-pro/
    ├── index.html
    └── app.html
```

## 운영 원칙

각 업무 도구는 독립된 하위 폴더에 배치합니다. 공통 상단 메뉴는 `common`에서 중앙 관리하고, 새로운 도구가 추가되면 공통 메뉴와 루트 `index.html` 런처에 함께 등록합니다.
