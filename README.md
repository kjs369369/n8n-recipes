# 🚀 GitHub Pages 배포 패키지

> 《퇴근 1시간 앞당기는 AI 자동화》 5장 - n8n 워크플로 다운로드 페이지
> May (김진수) · AICLab

---

## 폴더 구조

```
github-pages/
├── index.html              ← 메인 다운로드 페이지
├── recipes/                ← n8n 워크플로 JSON 5개
│   ├── r1.json
│   ├── r2.json
│   ├── r3.json
│   ├── r4.json
│   └── r5.json
├── qrcodes/                ← QR코드 이미지
│   ├── qr_main.png         ← 통합 페이지용 QR (책 부록 첫 페이지)
│   ├── qr_r1.png ~ r5.png  ← 레시피별 QR (책 본문 각 레시피 옆)
│   └── labeled/            ← 라벨 추가된 인쇄용 버전
├── DEPLOY_GUIDE.md         ← GitHub Pages 배포 단계별 가이드
└── README.md               ← 이 파일
```

---

## 빠른 시작 (3분)

### 1. GitHub에 폴더 통째로 업로드
- 새 저장소 `n8n-recipes` 생성
- 이 폴더 내용물을 드래그앤드롭으로 업로드

### 2. Settings → Pages 활성화
- Source: Deploy from a branch
- Branch: main / root

### 3. URL 확인 (2분 후)
```
https://[YOUR_USERNAME].github.io/n8n-recipes/
```

자세한 단계는 `DEPLOY_GUIDE.md` 참조.

---

## 책에 인쇄할 QR코드

### 본문 각 레시피 옆 (5장 5-3절)
- `qrcodes/labeled/labeled_r1.png` ~ `labeled_r5.png`

### 부록 A 첫 페이지 (통합 안내)
- `qrcodes/labeled/labeled_main.png`

⚠️ **중요**: 현재 QR코드는 placeholder URL(`may-aiclab.github.io`)을 가리킵니다.
May 선생님의 실제 GitHub 계정으로 배포한 후 **QR코드를 다시 생성**하세요.

---

## 다음 단계

1. GitHub 저장소 만들고 업로드 → DEPLOY_GUIDE.md 참조
2. URL 확인 후 QR코드 재생성
3. 출판사에 인쇄용 QR코드 전달

---

**제작자: 김진수 (May)**
- AICLab 소장
- 메이TV (@AI_coach_May)
