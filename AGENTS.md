# Project Agent Instructions

## Scope and Precedence

This file is the repository-level entrypoint for coding agents.

Read `.agents/docs/project.md` before non-trivial
work. Repository-specific commands, constraints, and narrower instructions take
precedence over these template defaults.

## What This Repo Is

Artel API 테스트 컬렉션 저장소. Insomnia REST Client v5 형식의 YAML
export 파일을 버전 관리한다.

구조:
- `agent-server.yaml` — Agent Server API (시나리오 QA 세션, /health)
- `orchestrator-server.yaml` — Orchestration Server API (인증, 프로젝트, 게임빌드·인스턴스, SDK·Agent·TestScenario)

Insomnia YAML 컬렉션을 `import`할 때 workspace ID, request ID 등은
Insomnia가 재할당한다. 저장소는 기기 간 공유를 위한 익스포트 형식이며,
환경변수는 `Insomnia Base Environment` + 서브 환경으로 관리한다.
비밀값은 절대 이 저장소에 포함하지 않는다.

## Project Workflow

For non-trivial work, follow:

- `.agents/docs/workflow.md`
- `.agents/docs/testing.md`

For tracked Git work, follow:

- `.agents/docs/issue.md`
- `.agents/docs/commit.md`
- `.agents/docs/pull-request.md`

Use project-local skills when installed and applicable. Skill instructions
define their own triggers, formats, and output paths.
