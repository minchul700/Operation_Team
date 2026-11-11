# Operation_Team

## 주말근무 Canvas 앱 작업 흐름

Git의 기준 소스는 [`powerapps/weekend-work-app`](./powerapps/weekend-work-app)입니다. 이 폴더에는 `App.pa.yaml`, `_EditorState.pa.yaml`, 화면 6개의 `.pa.yaml` 파일이 있습니다. 시작 화면은 `HomeScreen_이승우`입니다.

| 용도 | 환경 ID | 앱 ID |
| --- | --- | --- |
| Git 작업용 Canvas 앱 | `d5061da0-5b5d-e3e7-a53c-4fe455da8496` | `c3704f48-d5f4-436f-bcf1-8aaa0f293b03` |

[작업용 앱 편집 화면](https://make.powerapps.com/e/d5061da0-5b5d-e3e7-a53c-4fe455da8496/canvas/?action=edit&app-id=%2Fproviders%2FMicrosoft.PowerApps%2Fapps%2Fc3704f48-d5f4-436f-bcf1-8aaa0f293b03)

1. 작업용 앱을 Power Apps Studio 편집 모드로 열고 **공동 작성**을 켭니다. 변경 전 MCP `connect`와 `sync_canvas`로 최신 앱 상태를 가져옵니다.
2. 작업용 앱에서 화면을 수정한 뒤 저장합니다. 다시 `sync_canvas`를 실행하고 동기화된 `.pa.yaml`을 위 Git 소스 폴더에 반영합니다. 화면 파일뿐 아니라 변경된 `App.pa.yaml`과 `_EditorState.pa.yaml`도 함께 검토합니다.
3. 변경 사항을 기능 브랜치에 커밋하고 GitHub에 푸시한 뒤 `main`으로 Pull Request를 만듭니다. 공동 작업 중 다른 사람이 수정한 화면을 덮어쓰지 않도록 동기화 결과를 비교합니다.
4. 원본 앱 담당자가 검토된 Git 소스를 원본 앱의 Studio 공동 작성 세션에 적용하고 저장합니다. **Git 푸시나 PR 병합만으로 원본 앱이 자동 변경되지는 않습니다.**

현재 앱 소스는 화면 구성과 탐색 중심이며 Dataverse, Outlook, Power Automate 연결은 포함하지 않습니다.
