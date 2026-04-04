# 2026 수·과융합영재원 — 가우스 반 학습 가이드

초등 5학년 눈높이의 예습·복습·심화·상상 4단계 에세이 학습 자료

🔗 **사이트**: https://soniceduke.github.io/

---

## 📁 폴더 구조

```
soniceduke.github.io/
├── index.html              ← 메인 허브 페이지
├── css/
│   └── style.css           ← 공통 스타일시트
├── lectures/
│   ├── week-01.html        ← 1주차: 나의 성격과 과학윤리
│   ├── week-02.html        ← 2주차: 물, 너는 누구니?
│   └── ...                 ← (강의별로 추가)
└── README.md
```

---

## 🚀 GitHub Pages 배포 방법

### 1단계: 레포지토리 만들기

1. [GitHub](https://github.com) 로그인
2. 우측 상단 **+** → **New repository** 클릭
3. Repository name에 정확히 `soniceduke.github.io` 입력
   - ⚠️ GitHub 사용자명이 `soniceduke`가 아니면 자기 사용자명으로 변경
4. **Public** 선택
5. **Create repository** 클릭

### 2단계: 파일 업로드

**방법 A — 웹에서 직접 업로드 (가장 간단)**

1. 생성된 레포 페이지에서 **uploading an existing file** 클릭
2. 이 폴더의 모든 파일을 드래그 앤 드롭
3. **Commit changes** 클릭

> ⚠️ 폴더 구조를 유지해야 합니다!
> - `index.html`은 최상위에
> - `style.css`는 `css/` 폴더 안에
> - 강의 파일은 `lectures/` 폴더 안에

**방법 B — Git 명령어 (터미널 사용 가능 시)**

```bash
# 1. 클론
git clone https://github.com/soniceduke/soniceduke.github.io.git
cd soniceduke.github.io

# 2. 파일 복사 (다운받은 파일들을 이 폴더에 넣기)

# 3. 업로드
git add .
git commit -m "Initial site setup"
git push origin main
```

### 3단계: GitHub Pages 활성화

1. 레포 페이지 → **Settings** 탭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. Source를 **Deploy from a branch** 선택
4. Branch를 **main**, 폴더를 **/ (root)** 선택
5. **Save** 클릭
6. 1~2분 후 `https://soniceduke.github.io/` 접속 확인

---

## 📝 새 강의 추가 방법

1. Claude에서 해당 주차의 상세 에세이를 요청
2. 생성된 `week-XX.html` 파일을 `lectures/` 폴더에 업로드
3. `index.html`의 weeks 배열에서 해당 주차의 `status`를 `"ready"`로 변경
4. Git push 또는 웹에서 파일 수정

```javascript
// index.html에서 해당 주차 찾아서 status 변경
{ week:2, ..., status:"ready" },  // "soon" → "ready"로 변경
```

---

## 📖 학습 가이드 구성

| 탭 | 시간 | 수준 | 목적 |
|---|---|---|---|
| 📖 예습 | 10분 | 초5 | 수업 전 핵심 이론 미리보기 |
| 🔬 복습 | 10분 | 초5 | 수업 후 정리 + 실생활 연결 |
| 🚀 심화 | 12분 | 초6~중1 | 선행 개념, 깊은 원리 탐구 |
| 💭 상상 | 자유 | 무제한 | 사고실험 + 자기주도 탐구 |
