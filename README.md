# works

업무 과정에서 사용하는 웹 기반 도구와 검증용 유틸리티를 모아 관리하는 저장소입니다.

## GitHub Pages

이 저장소는 `main` 브랜치의 `/ (root)`를 GitHub Pages 소스로 사용하는 것을 기준으로 구성합니다.

- Repository: `mycodehive/works`
- Pages base URL: `https://mycodehive.github.io/works/`
- Launcher: `index.html`

## Applications

### Cross-verification-of-labor-cost-payment-plan

연구인력 월별 인건비 지급계획과 계약관리 데이터를 교차 검증하는 웹 도구입니다.

주요 기능:

- `contractsubject` 연구원계약과제별현황 업로드
- `joinlist` 연구인력현황조회(월별인건비) 업로드
- `ingcontract` 진행중인 연차과제 현황 업로드
- `currentemp` 재직자 현황 업로드
- 진행중 과제 및 재직자 기준 필터링
- 직번·과제번호·지급년도 기준 교차 검증
- 월별 지급액/예정액 불일치 확인
- 계약정보 누락 및 참여인력 미등록 확인
- 검증 결과 CSV / Excel 다운로드

실행 주소:

`https://mycodehive.github.io/works/Cross-verification-of-labor-cost-payment-plan/`

폴더 구조:

```text
works/
├── README.md
├── index.html
└── Cross-verification-of-labor-cost-payment-plan/
    ├── index.html
    └── xlsx.full.min.js
```

## 운영 원칙

각 업무 도구는 독립된 하위 폴더에 배치하고, 브라우저에서 바로 실행할 수 있는 경우 해당 폴더의 `index.html`을 진입점으로 사용합니다. 새로운 도구가 추가되면 루트 `index.html` 런치페이지에도 함께 등록합니다.
