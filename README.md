# AutoRoutine 공지 (`notices.json`)

앱 공지사항은 이 JSON을 읽습니다. **파일을 고치고 GitHub에 올리면** 스토어 업데이트 없이 글이 바뀝니다.

- 공개 저장소: https://github.com/babohoil-lab/AutoRoutine-notices
- 앱이 여는 주소: https://raw.githubusercontent.com/babohoil-lab/AutoRoutine-notices/main/notices.json

소스 저장소(`AutoRoutine`)는 비공개라 앱이 못 읽습니다. 공지 파일만 위 공개 저장소에 둡니다.

## 글 수정

1. `C:\AI_Android\notices\notices.json` 을 고친다.
2. 프로젝트 루트에서 `.\scripts\sync-notices.ps1` 을 실행한다.

`id`를 **새 문자열**로 주면 앱에 미읽음 숫자가 다시 뜹니다. 같은 `id`는 이미 읽은 사용자에게 다시 표시되지 않습니다.

루트 필드:
- `latestAppVersion`: Play에 올린 최신 `versionName` (예: `"1.9.60"`). 설치 버전보다 높으면 도움말에 배지가 뜨고, **앱을 그 버전으로 올리기 전까지** 유지됩니다.
- `latestAppSummary`: 언어별 한 줄 요약 (업데이트 공지 카드에 표시).

`title` / `body`는 언어 코드(`ko`, `en`, `zh`, `ja`, `hi`, `es`, `pt`, `de`)별 문자열입니다. 없는 언어는 `en` → `ko` 순으로 대체합니다.
