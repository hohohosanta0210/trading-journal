# 매매 일지 (Trading Journal)

개인용 매매 일지 — 단일 HTML 파일, localStorage 기반, GitHub Pages 배포용.

## 사용법

배포된 URL로 접속 → 폰 브라우저에서 "홈 화면에 추가"하면 PWA처럼 사용 가능.

## 기능

- 매매 진입/청산 기록 (모바일 우선)
- 누적 손익 / 월별 손익 차트
- 감정별 / 손절선 유무 / 시장별 / 보유기간별 / 비중별 패턴 분석
- JSON 내보내기/불러오기 (백업/복원)
- 다크 모드, 한국 시장 색상 컨벤션 (빨강=수익, 파랑=손실)

## 데이터 저장

브라우저 `localStorage`에만 저장 (서버 없음).
**중요**: 브라우저 데이터 청소 시 매매 기록이 사라집니다. 설정 → 데이터 내보내기로 정기 백업하세요.

기기/브라우저별로 데이터가 분리되므로 PC와 폰 간 동기화는 수동 (JSON 내보내기/불러오기).

## 로컬에서 보기

단순 정적 HTML이므로 아무 정적 서버로 열면 됩니다:

```bash
npx serve .
# or
python -m http.server 8080
```

## 기술 스택

- Vanilla HTML/CSS/JavaScript (프레임워크 없음)
- Chart.js 4.4 (CDN)
- Pretendard 폰트 (CDN)
- localStorage
