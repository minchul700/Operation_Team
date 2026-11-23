# Operation_Team

DEX_CRM_LIVE 주말근무 신청 앱과 `LSW_WeekendWork` 비관리형 솔루션의 소스입니다.

## 구성

- `powerapps/weekend-work-app/`: 기존 주말근무 Canvas 앱 `8cbb6cab-e76f-4278-af40-6670d5a29816`에서 동기화한 `.pa.yaml` 파일
- `solutions/LSW_WeekendWork/`: LIVE 솔루션에서 내보내고 풀어낸 Dataverse 및 Flow 구성요소
- `docs/designs/weekend-work.md`: 신청 데이터와 3단계 승인 경로의 구현 계약
- `STATUS.md`: 현재 연결 및 구현 상태

원본 휴가 앱의 `TB_EMPLOYEE`와 `TB_AdminPassword`는 읽기 전용으로 취급합니다. 새 테이블 `TB_EMPLOYEE_WeekendWork`, `TB_AdminPassword_WeekendWork`에 원본 행을 복제하고, 신청은 별도 `TB_WeekendWorkRequest`에 저장합니다. 관리자 비밀번호 행과 직원 데이터는 Git에 넣지 않습니다.

승인 경로는 조직도 SharePoint 목록의 팀 리더 → 지정 본부장 → 지정 경영지원 담당자 순서입니다. 실제 연결 및 검증 상태는 [STATUS.md](STATUS.md)를 확인하세요.
