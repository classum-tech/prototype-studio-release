# prototype-studio-release

CLASSUM 프로토타입 스튜디오(데스크톱 앱)의 **새 버전 알림**이 읽는 버전 정보만 두는 **공개** 저장소입니다.

- `version.json` — 최신 버전(빌드한 날짜, 예: `2026.1026.0` = 2026-10-26 첫 판) · 받는 곳 링크 · 짧은 메모. 설치된 앱이 로그인 없이
  `https://raw.githubusercontent.com/classum-tech/prototype-studio-release/main/version.json` 을 읽어, 더 새 판이면 알립니다.
- 앱 파일은 여기 두지 않습니다 — 사내 전용 위치에 있고, `downloadUrl` 이 그곳을 가리킵니다.
- 새 판 올리기: classum-frontend 저장소에서 `pnpm -F @repo/prototype-studio desktop:build` → 앱 파일을 사내 위치에 올림 →
  `pnpm -F @repo/prototype-studio desktop:release-info --download <그 위치 주소>` → 만든 `desktop/out/release-info/version.json` 을 여기
  main 에 올립니다. 설계는 `tooling/prototype-studio/DESIGN.md` §6-5.

> 🔴 공개 저장소입니다. 버전 · 받는 곳 링크 · 짧은 메모 말고는 올리지 마세요.
