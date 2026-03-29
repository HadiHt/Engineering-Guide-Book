# Engineering Hub

This folder is an LLM-ready engineering handbook.

It is designed for coding assistants that can read files directly, but it also works as a paste-friendly rule set for chat tools.

## Start Here

- [START](Engineering%20Hub/START.md)
- [Shortest Prompt](Engineering%20Hub/00%20Start%20Here/Shortest%20Prompt.md)
- [Minimal Starter Prompt](Engineering%20Hub/00%20Start%20Here/Minimal%20Starter%20Prompt.md)
- [Recommended Usage Pattern](Engineering%20Hub/00%20Start%20Here/Recommended%20Usage%20Pattern.md)
- [Hub Index & LLM Fetching Guide](Engineering%20Hub/00%20Start%20Here/Hub%20Index%20%26%20LLM%20Fetching%20Guide.md)

## Folder Layout

- `START.md`: single company entrypoint
- `00 Start Here`: entry points, starter prompt, loading guide
- `10 Core Rules`: rules every coding session should load first
- `15 Dynamic Rules`: add new rules here without changing the core handbook
- `20 Standards`: stack-specific and architecture standards
- `30 Workflow`: execution, review, and completion flow
- `40 Operations`: incident, release, and rollback procedures
- `50 Memory`: optional durable task and architecture memory

## Default Loading Order

1. Read `START.md`.
2. Load core rules and the dynamic rules index.
3. Detect scope: `frontend`, `backend`, or `both`.
4. Load only the relevant standards and workflow pages.
5. Add memory or operations pages only if the task needs them.
