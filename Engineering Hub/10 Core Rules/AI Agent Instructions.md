# AI Agent Instructions

This file is the execution contract for AI-assisted engineering work in this hub.

If any page conflicts with this one, this page wins.

## Core Operating Rules

1. Detect scope before writing code: `frontend`, `backend`, or `both`.
2. Read the hub index first, then load only the pages required for the current task.
3. Treat loaded standards as active rules for the rest of the session.
4. Stay inside task scope. Do not make unrelated fixes unless explicitly asked.
5. If the task is structurally ambiguous, stop and ask before making changes.
6. Review your changes before claiming the task is done.
7. Update the project memory/log only if this workflow actually uses one.

## What Good Execution Looks Like

- Load minimal context, not the whole hub.
- Follow the standards for the detected scope.
- Prefer small, traceable changes over broad cleanup.
- Document important assumptions and non-obvious decisions.
- Surface risks instead of silently working around them.

## When To Ask Instead Of Guessing

Ask before proceeding if any of these are unclear:

- which layer owns the change
- whether a new API, route, or permission is required
- whether a shared contract can safely change
- whether a migration, config change, or dependency change is allowed

Minor details such as labels, placeholder copy, and low-risk naming choices can be decided locally if documented.

## Negative Guardrails

- Do not start coding before scope is known.
- Do not load architecture guidance for routine tasks.
- Do not treat legacy code as proof that a pattern is acceptable.
- Do not silently fix unrelated bugs.
- Do not edit standards pages during normal feature work.
- Do not declare success without checking tests, risks, and task completion criteria.

## Conflict Handling

If the codebase conflicts with the standards:

- If the conflicting code is already in scope, move it toward the standard.
- If it is outside scope, leave it alone and note the follow-up.
- If changing it would affect multiple layers or contracts, ask first.
