# GitHub Pages 배포 가이드

> 이 폴더 전체를 GitHub에 올려서 무료 영구 호스팅하는 단계별 가이드

---

## 최종 결과

배포가 끝나면 다음 URL이 작동합니다.

```
https://[YOUR_USERNAME].github.io/n8n-recipes/             ← 다운로드 페이지
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r1.json  ← JSON 직접 다운로드
```

---

## Step 1. GitHub 계정 + 저장소 만들기

### 1-1. GitHub 가입 (이미 있으면 건너뛰기)
https://github.com 에서 무료 가입

### 1-2. 새 저장소(Repository) 만들기
1. 우측 상단 **+** 버튼 → **New repository**
2. 다음 설정:

| 항목 | 값 |
|------|-----|
| Repository name | `n8n-recipes` |
| Description | "퇴근 1시간 앞당기는 AI 자동화 - 5장 워크플로 다운로드" |
| Public/Private | **Public** (Pages는 공개 저장소만 무료) |
| Add README | 체크 안 함 |

3. **Create repository** 클릭

---

## Step 2. 파일 업로드

### 방법 A: 웹 브라우저로 (가장 쉬움)

1. 저장소 메인 페이지에서 **uploading an existing file** 클릭
2. 이 폴더의 모든 내용을 드래그앤드롭:
   - `index.html`
   - `recipes/` 폴더 (r1.json ~ r5.json)
   - `qrcodes/` 폴더 (선택)
   - `README.md` (선택)
3. 하단 **Commit changes** 클릭

> **중요**: `recipes` 폴더는 폴더 구조가 유지되어야 합니다. 파일을 하나씩 올리면 폴더 구조가 깨질 수 있으니 **드래그앤드롭으로 한 번에** 올립니다.

### 방법 B: Git 명령어로 (개발자라면)

```bash
git clone https://github.com/[YOUR_USERNAME]/n8n-recipes.git
cd n8n-recipes
# 이 폴더의 파일을 모두 복사
cp -r [다운로드받은_폴더]/* .
git add .
git commit -m "Initial workflow files"
git push
```

---

## Step 3. GitHub Pages 활성화

1. 저장소 페이지에서 **Settings** 탭 클릭
2. 좌측 메뉴에서 **Pages** 클릭
3. 다음 설정:

| 항목 | 값 |
|------|-----|
| Source | Deploy from a branch |
| Branch | **main** |
| Folder | **/ (root)** |

4. **Save** 클릭
5. 약 1~2분 후 자동 배포 완료
6. 페이지 상단에 **"Your site is live at https://..."** 메시지가 뜨면 성공

---

## Step 4. URL 확인

배포 완료 후 다음 URL이 작동하는지 확인합니다.

```
https://[YOUR_USERNAME].github.io/n8n-recipes/
```

브라우저에서 열면 다운로드 페이지가 표시되고, 각 JSON 다운로드 버튼이 작동합니다.

---

## Step 5. QR코드 URL 업데이트 (필수)

기본 QR코드는 **`may-aiclab`**이라는 placeholder GitHub 계정으로 생성되어 있습니다. May 선생님의 실제 GitHub 계정명으로 QR코드를 다시 만들어야 합니다.

### 방법 1: 온라인 QR 생성기 (가장 빠름)
1. https://www.qr-code-generator.com 접속
2. URL 입력란에 자신의 실제 URL 입력 (예: `https://kimjinsoo-aiclab.github.io/n8n-recipes/`)
3. 생성된 QR코드 다운로드
4. 6개 URL 모두 반복

### 방법 2: 책 출간 시 출판사에 의뢰
출판사에 다음 6개 URL을 전달하면 인쇄용 고품질 QR코드를 만들어줍니다.

```
https://[YOUR_USERNAME].github.io/n8n-recipes/                      (메인)
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r1.json       (레시피 1)
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r2.json       (레시피 2)
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r3.json       (레시피 3)
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r4.json       (레시피 4)
https://[YOUR_USERNAME].github.io/n8n-recipes/recipes/r5.json       (레시피 5)
```

---

## 추가: 단축 URL 사용 (선택)

GitHub Pages URL이 길다면 단축 URL을 함께 인쇄하는 것을 권장합니다.

### bit.ly 사용
1. https://bitly.com 가입
2. 각 URL을 단축 (예: `bit.ly/ai-r1`)
3. 책에는 단축 URL을 함께 표기

### 결과 예시
> **레시피 1 다운로드**
> 📱 QR 스캔: [QR 이미지]
> 🔗 직접 링크: `bit.ly/ai-r1`

---

## 자주 묻는 질문

**Q1. 비용이 발생하나요?**
A. 아닙니다. GitHub Pages는 공개 저장소에 한해 **완전 무료 영구 호스팅**입니다.

**Q2. 트래픽 제한이 있나요?**
A. 월 100GB 대역폭 제한이 있지만, 책 독자가 JSON 다운받는 용도로는 절대 도달할 수 없는 양입니다.

**Q3. 워크플로 JSON을 업데이트하고 싶을 때는?**
A. 저장소에서 해당 JSON 파일을 클릭 → 우측 상단 연필 아이콘 클릭 → 수정 → Commit. 약 1~2분 후 자동 반영됩니다.

**Q4. 도메인을 내 도메인으로 바꾸려면?**
A. Settings → Pages → Custom domain에서 자기 도메인 입력 후 DNS 설정. 자세한 방법은 GitHub 공식 문서 참조.

**Q5. JSON 파일을 누가 수정할까봐 걱정됩니다.**
A. 저장소가 공개되어도 다른 사람이 May 선생님의 파일을 수정할 수는 없습니다. Pull Request 제안만 가능하며, 거절할 권한이 있습니다.

---

## 배포 체크리스트

```
□ GitHub 계정 가입
□ n8n-recipes 저장소 생성 (Public)
□ 이 폴더의 모든 파일 업로드
□ Settings → Pages에서 활성화 (main / root)
□ 1~2분 대기 후 URL 접속 확인
□ 다운로드 버튼 5개 모두 클릭해서 작동 확인
□ QR코드를 실제 URL로 재생성
□ 책 인쇄용 QR코드 출판사에 전달
```

---

**제작자: 김진수 (May)**
**문서 업데이트**: 2026.05.04
