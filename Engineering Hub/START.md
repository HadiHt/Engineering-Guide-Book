# START

Read this file first.

This handbook is meant to be easy for both humans and LLMs to use across a company.

## Default Instruction

If you are an LLM working on an engineering task:

1. Read `Engineering Hub/START.md` first.
2. Then read:
   - `Engineering Hub/10 Core Rules/AI Agent Instructions.md`
   - `Engineering Hub/10 Core Rules/LLM Write Boundaries.md`
   - `Engineering Hub/15 Dynamic Rules/Rules Index.md`
3. Detect scope before doing any work: `frontend`, `backend`, or `both`.
4. Load only the standards and workflow files needed for the task.
5. Stay inside task scope unless the user explicitly expands it.
6. Before finishing, run a brief review against the loaded rules and report assumptions and residual risks.

## What To Load By Task

### Always

- `10 Core Rules/AI Agent Instructions.md`
- `10 Core Rules/LLM Write Boundaries.md`
- `15 Dynamic Rules/Rules Index.md`

### Frontend

- `20 Standards/React + TypeScript Standards.md`
- `20 Standards/Git Standards.md`
- `20 Standards/PR Review Checklist.md`

### Backend

- `20 Standards/C# Coding Standards.md`
- `20 Standards/Git Standards.md`
- `20 Standards/PR Review Checklist.md`

### Architecture Or Boundary Changes

- `20 Standards/Architecture Rules.md`
- `50 Memory/Architecture Decisions (ADR).md` only if a durable design decision should be recorded

### Starting Or Resuming Work

- `30 Workflow/Development Workflow.md`
- `30 Workflow/Definition of Done.md`
- `30 Workflow/Session Resume Protocol.md` only when resuming existing work

### Incident Or Release Work

- `40 Operations/Incident & Postmortem Guide.md`
- `40 Operations/Release & Rollback Runbook.md`

## What To Report Before Starting

- detected scope
- files loaded
- assumptions that could affect correctness

## Minimal Company Prompt

Use this as the default company prompt in file-aware tools:

```text
Read `Engineering Hub/START.md` first and follow it before doing the task.
Do not load the entire handbook unless `START.md` tells you to.
Before starting, report scope, loaded files, and assumptions.
```

## Rule Growth Model

- Keep `10 Core Rules` stable and small.
- Add new situational rules in `15 Dynamic Rules`.
- Promote a dynamic rule into the core rules only if it becomes broadly important and repeatedly useful.
