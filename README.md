# .github

MonsterHouseStudio **조직 프로필** 저장소입니다.

`profile/README.md` 의 내용이 조직 페이지(https://github.com/MonsterHouseStudio)
최상단에 그대로 표시됩니다.

```
.
├── profile/
│   ├── README.md      ← 조직 페이지에 노출되는 본문
│   └── assets/        ← 로고 · 화면 스크린샷
└── README.md          ← 이 파일 (저장소 안에서만 보임)
```

## 주의

- 저장소 이름은 반드시 **`.github`** 여야 합니다. 다른 이름이면 프로필로 인식되지 않습니다.
- 저장소가 **public** 이어야 조직 페이지에 표시됩니다.
- 파일 경로는 반드시 `profile/README.md` 입니다. 루트의 `README.md` 는 표시되지 않습니다.

## 스크린샷 갱신

로컬에서 BE·FE를 띄운 뒤 headless Chrome 으로 캡처합니다.

```powershell
$chrome = "C:\Program Files\Google\Chrome\Application\chrome.exe"
& $chrome --headless=new --disable-gpu --hide-scrollbars `
  --window-size=1440,1500 --virtual-time-budget=20000 `
  --run-all-compositor-stages-before-draw `
  --screenshot="profile/assets/home.png" "http://localhost:5173/ko"
```

`--virtual-time-budget` 이 없으면 페이드인 애니메이션과 API 응답이 끝나기 전에 찍혀
화면이 흐리거나 비어 있는 상태로 캡처됩니다.
# .github
