# 정지우 포트폴리오 웹사이트

실물 로봇 시스템 · AMR 자율주행 엔지니어 정지우의 포트폴리오 (정적 단일 페이지).

## 로컬에서 보기

```bash
# 브라우저로 바로 열기
xdg-open index.html
```

## GitHub Pages로 배포하기 (무료 공개 호스팅)

### 방법 1) 새 저장소로 배포 (가장 간단)

1. GitHub에서 새 저장소 생성 (예: `portfolio`, **Public**)
2. 이 폴더(`portfolio_site`)의 파일을 저장소 루트에 올림:

```bash
cd portfolio_site
git init
git add index.html README.md
git commit -m "portfolio site"
git branch -M main
git remote add origin https://github.com/<아이디>/portfolio.git
git push -u origin main
```

3. 저장소 → **Settings → Pages → Build and deployment**
   - Source: `Deploy from a branch`
   - Branch: `main` / `/ (root)` 선택 후 Save
4. 1~2분 뒤 접속: `https://<아이디>.github.io/portfolio/`

### 방법 2) 사용자 메인 페이지로 배포

저장소 이름을 `<아이디>.github.io`로 만들면 주소가 `https://<아이디>.github.io/`가 됩니다. (나머지 과정 동일)

## Notion 페이지로도 쓰려면

이 사이트와 별개로, `../portfolio_draft.md` 파일 내용을 Notion에 붙여넣으면 Notion 웹페이지로도 공유할 수 있습니다.
- Notion에서 `/` → `Import` → Markdown 선택, 또는 마크다운 본문을 복사해 붙여넣기
- 페이지 우상단 `공유 → 웹에서 게시(Publish)`로 공개 링크 생성

## 수정 가이드

- 모든 내용/스타일은 `index.html` 한 파일 안에 있습니다.
- 졸업작품: `id="education"` 섹션의 "졸업작품" 카드에 내용 채우기
- 정량 수치: 각 프로젝트 `<li>` 항목에 추가
- 프로젝트 이미지/영상: 각 `.proj` 블록 안에 `<img src="...">` 또는 영상 링크 추가 권장
- 색상 테마: `:root`의 CSS 변수(`--accent` 등) 수정
