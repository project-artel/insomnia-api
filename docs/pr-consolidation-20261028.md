# 내 Insomnia PR 2개 통합 기록

2026-10-28 `dev-yunseong`의 [#21](https://github.com/project-artel/insomnia-api/pull/21)과 [#23](https://github.com/project-artel/insomnia-api/pull/23)을 통합했다. 실제 remote에는 `develop`이 없고 원본 PR과 기본 branch가 `master`여서 통합 PR도 `master` 기준이다. `master`에는 merge하지 않았다.

- #21의 씬 명세 조회와 원격 스캔 API collection을 유지했다.
- #23의 model slug 갱신을 유지했다.
- 두 PR은 충돌 없이 merge됐고 source head 두 개가 모두 통합 HEAD의 ancestor임을 확인했다. 원본 branch와 commit·작성자 이력을 유지했다.
- root YAML 2개의 syntax·Insomnia v5 collection 형식·metadata ID 중복 검사를 통과했다. agent collection은 15개, orchestrator collection은 69개 ID가 고유하다. root JSON 2개의 parsing도 통과했다. `git diff --check`가 통과했다.
- 새 인증 정보는 추가하지 않았다. 실제 서버 호출과 Insomnia UI import는 이번 통합에서 실행하지 않았다.
- 원본 PR의 리뷰와 검증 기록은 원본 링크에 보존한다. 다른 작성자 PR과 원본 branch는 변경하거나 종료하지 않는다. 통합 PR을 닫고 원본 PR을 reopen하면 이전 리뷰 구조로 복원할 수 있다.
