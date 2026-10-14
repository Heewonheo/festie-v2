# Festie — 페스티벌 준비부터 기록까지

ICT융합디자인과 졸업작품 **Festie** 앱 프로토타입입니다.
처음 실행한 빈 화면부터 페스티벌을 담고, 준비하고, 공연 후 리포트를 만드는 과정까지 실제 앱처럼 직접 눌러볼 수 있어요.

## 써보는 순서

1. **탐색**에서 Grand Mint Festival 2026을 열고 `준비 탭에 추가하기`
2. **준비** 탭 대시보드에서
   - 타임테이블: 보고 싶은 공연 고르기
   - 체크리스트: 챙길 것 모두 체크
   - 플레이리스트: 고른 공연으로 만들어진 셋리스트 내보내기
3. 네 가지를 모두 끝내면 **기록** 탭에 `CREATE REPORT`가 열려요
4. 사진·한 줄 소감·별점·본 공연·감상을 입력하고 `SAVE REPORT` → 내가 쓴 내용으로 리포트 완성, 공유까지

새로고침하면 처음 상태로 돌아가요.

## GitHub Pages로 올리기

1. GitHub에서 새 저장소를 **Public**으로 만들어요 (예: `festie`).
2. 저장소에서 **Add file → Upload files**를 누르고, 이 폴더 안의 파일을 **모두** 끌어다 놓아요.
   - `index.html`, `festie-runtime.js`, `morphdom-umd.min.js`, `manifest.webmanifest`, 아이콘 3개, `images` 폴더, `.nojekyll`
   - `.nojekyll`처럼 점으로 시작하는 파일이 안 보이면 없어도 동작해요.
3. **Commit changes**를 눌러요.
4. **Settings → Pages**에서 Branch를 `main`, 폴더를 `/ (root)`로 고르고 **Save**를 눌러요.
5. 1~2분 뒤 `https://아이디.github.io/festie/` 주소가 생겨요.

## 휴대폰에서 앱처럼 쓰기

- **아이폰**: Safari로 주소를 열고 → 공유 버튼 → **홈 화면에 추가**
- **안드로이드**: Chrome으로 주소를 열고 → 메뉴(⋮) → **홈 화면에 추가**

홈 화면 아이콘으로 열면 주소창 없이 전체화면으로 열리고, 화면이 폰 크기에 꽉 차요.

## 파일 구성

| 파일 | 역할 |
| --- | --- |
| `index.html` | 앱 전체 화면과 동작 |
| `festie-runtime.js` | 화면을 그리고 입력에 반응하게 하는 작은 실행 코드 |
| `morphdom-umd.min.js` | 화면을 바꿀 때 스크롤·입력 상태를 지켜주는 라이브러리 (MIT, `morphdom-LICENSE.txt`) |
| `manifest.webmanifest`, `icon-*.png` | 홈 화면에 추가할 때 쓰는 앱 이름과 아이콘 |
| `images/` | 페스티벌 포스터, 아티스트·현장 사진 |

폰트(Josefin Sans, Hanken Grotesk, Noto Sans KR)는 Google Fonts에서 불러와서, 인터넷이 연결돼 있어야 원래 글꼴로 보여요.
