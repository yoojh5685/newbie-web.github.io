# NEWbiE GitHub Pages 설정

이 폴더의 파일들을 GitHub Pages에 업로드하면 Universal Link가 작동합니다.

## 파일 구조
```
├── index.html                              # 메인 페이지
├── article/
│   └── index.html                         # 기사 페이지 (/article/{id} 경로용)
├── .well-known/
│   └── apple-app-site-association         # Universal Link 설정 파일
└── README.md                              # 이 파일
```

## GitHub Pages 설정 방법

1. GitHub에서 새 저장소 생성 (예: `newbie-app`)
2. 이 폴더의 모든 파일을 저장소에 업로드
3. Settings → Pages → Source를 "Deploy from a branch"로 설정
4. Branch를 "main"으로 선택
5. URL이 `https://username.github.io/newbie-app` 형태로 생성됨

## 중요 수정사항

### apple-app-site-association 파일에서:
```json
"appID": "TEAMID.com.yourcompany.NEWbiE"
```
- `TEAMID`: Apple Developer 팀 ID로 변경
- `com.yourcompany.NEWbiE`: 실제 Bundle ID로 변경

### 앱 다운로드 링크:
현재 `https://apps.apple.com/kr/app/newbie/id6736697572`로 설정되어 있음
실제 App Store ID로 변경 필요

## 사용법
GitHub Pages 배포 후 다음과 같이 사용:
- `https://username.github.io/newbie-app/article/123?title=기사제목`
