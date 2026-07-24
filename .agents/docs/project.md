# Project: Insomnia API Collections

## Overview

Artel API 테스트 컬렉션을 Insomnia v5 YAML 형식으로 버전 관리하는
단일 목적 저장소다. 동일 통합 테스트 workflow를 모든 기기에서 재현할 수
있게 한다.

## Repositories & Ownership

- `agent-server.yaml` — Agent Server API (시나리오 QA 세션, /health)
- `orchestrator-server.yaml` — Orchestration Server API (인증, 프로젝트, 게임빌드/인스턴스, SDK/Agent/TestScenario)

## External Systems

### Jira

프로젝트 `ARTEL`, Epic `ARTEL-14` (Infra / 공통 운영).

저장소 고유 Jira 이슈는 `작업 유형=chore` 또는 `infra`, `레포지토리=없음`으로
생성한다. 새 endpoint 추가·변경은 구현 저장소(agent-server/orchestrator-server)의
개발 흐름에 따르며, 이 저장소는 구현이 완료된 endpoint의 Insomnia export만
추가한다.

자격 증명은 `~/.hermes/.env`에서 `GITHUB_TOKEN`을 사용한다.

## Commands & Constraints

- Insomnia 컬렉션은 Export → "Insomnia v5 (YAML)" 포맷으로 내보낸다.
- 환경변수는 `Insomnia Base Environment` (stage) + `local` 서브 환경으로 관리한다.
- 비밀값(JWT, API Key)은 절대 YAML에 포함하지 않고 Insomnia private environment에서 관리한다.
- 브랜치: `chore/<issue summary>-<ISSUE KEY>` 규칙을 따른다.
- PR: `develop` 브랜치를 대상으로 한다(다른 저장소와 일관성 유지).

## Directory Layout

```
.
├── agent-server.yaml          # Agent Server API 컬렉션
├── orchestrator-server.yaml   # Orchestration Server API 컬렉션
├── .agents/docs/              # 에이전트 문서 (issue.md, workflow.md, ...)
├── AGENTS.md                  # 저장소 진입점 (CLAUDE.md 심링크)
└── CLAUDE.md                  # → AGENTS.md
```
