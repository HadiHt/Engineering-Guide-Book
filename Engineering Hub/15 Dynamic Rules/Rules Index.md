# Rules Index

This folder is for fast-growing rules that should not immediately bloat the core handbook.

Read this file on every session after the core rules.

## How It Works

- Put new rules in small focused files.
- Group rules by topic, team, system, or risk area.
- Load only the rule files that match the task.
- If a dynamic rule becomes universally important, move or summarize it into `10 Core Rules`.

## Default Files To Consider

Always read this index, then load only the relevant rule files below:

- `Active Rules.md`: short list of currently important cross-cutting rules
- `Anti Gravity Rules.md`: load when work is being done through Anti Gravity and you want tool-specific behavior or guardrails
- any task-specific or domain-specific rule files that match the current work

## Suggested Naming

- `frontend-rules.md`
- `backend-rules.md`
- `payments-rules.md`
- `auth-rules.md`
- `release-rules.md`
- `qa-rules.md`
- `anti-gravity-rules.md`

Use names that make the scope obvious.

## Rule File Template

Each dynamic rule file should start with:

```md
# <Rule Group Name>

## When To Load

- short condition
- short condition

## Rules

### RULE-XXX - Short Title

- **Scope:** `frontend` | `backend` | `both`
- **Rule:** one sentence
- **Why:** one sentence
- **Added:** YYYY-MM-DD
- **Source:** task, PR, incident, or team note
```

## Promotion Rule

Move a rule into the core handbook if it is:

- broadly applicable
- repeatedly important
- safety-critical
- likely to matter in most sessions
