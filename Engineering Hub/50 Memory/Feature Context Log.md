# Feature Context Log

Use this file as lightweight implementation memory if the team wants durable task context.

If your workflow does not maintain a task log, you can ignore this page.

## When To Use It

- a task spans multiple sessions
- a PR needs historical context
- a change has non-obvious decisions or follow-ups

## Entry Template

### [TASK-ID] - Short Description

- **Date:** YYYY-MM-DD
- **Status:** `in progress` | `shipped` | `follow-up needed` | `hotfix`
- **Scope:** `frontend` | `backend` | `both`
- **Implementation summary:** What changed and why
- **Key decisions:** Important choices or assumptions
- **API/schema changes:** `none` or a concise list
- **Files/modules touched:** primary areas changed
- **PR link:** URL or `none`
- **Risks/follow-ups:** residual risks or next steps

## Log Entries

Add new entries below this line, newest first.

[Ticket Plans](Feature%20Context%20Log/Ticket%20Plans.md)
