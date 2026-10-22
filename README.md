# 모먼트 — 나의 작은 작업실

계산기와 실시간 날씨가 있는 작은 생산성 대시보드입니다. HTML 파일 하나로 동작하며 별도의 빌드 과정이나 서버가 필요하지 않습니다.

## 기능

- 키보드 입력과 사칙연산을 지원하는 계산기
- 지역 선택 및 현재 위치 기반 실시간 날씨 (Open-Meteo)
- 브라우저에 자동 저장되는 할 일 목록
- 25분·50분 집중 타이머와 5분 휴식 타이머
- 실시간 시계와 모바일 대응 화면

## 실행

`index.html`을 브라우저에서 열면 됩니다. 날씨와 웹 폰트를 불러오려면 인터넷 연결이 필요합니다. 현재 위치 기능은 HTTPS 및 브라우저 위치 권한이 필요할 수 있습니다.

할 일은 사용 중인 브라우저의 로컬 저장소에만 보관됩니다. 기기 간 동기화는 지원하지 않으며, 로컬 파일과 배포 사이트의 저장 공간은 서로 다릅니다.

## GitHub Pages 배포

이 저장소의 **Settings → Pages → Build and deployment**에서 다음과 같이 설정합니다.

- Source: **Deploy from a branch**
- Branch: **main**
- Folder: **/ (root)**

## 수정한 내용을 다시 올리기

이 폴더에서 터미널을 열고 아래 명령을 순서대로 실행합니다.

```powershell
git status
git add index.html README.md .gitignore
git diff --cached
git commit -m "Update moment app"
git push
```

첫 배포 이후에는 `index.html`을 수정하세요. 상위 폴더의 `productivity.html`은 최초 원본이며 자동으로 동기화되지 않습니다.

## 외부 서비스

- 날씨: [Open-Meteo](https://open-meteo.com/)
- 웹 폰트: Google Fonts (DM Sans, Noto Sans KR)

GitHub CLI로 저장소 생성과 인증을 관리하고, Git으로 변경 사항을 커밋·푸시합니다.
