# Active Rules

Use this file for short, high-value dynamic rules that are currently important across multiple tasks.

## When To Load

- always, after reading `Rules Index.md`

## Rules

### RULE-DR-001 - Confirm Shared Contract Changes Before Editing

- **Scope:** both
- **Rule:** Do not change shared request, response, or schema contracts without checking which layers and consumers are affected.
- **Why:** Small contract edits often create silent breakage across services or UI flows.
- **Added:** 2026-03-29
- **Source:** handbook hardening

### RULE-DR-002 - Prefer Small Traceable Changes Over Broad Cleanup

- **Scope:** both
- **Rule:** When multiple valid approaches exist, prefer the smallest change set that solves the task clearly and can be reviewed easily.
- **Why:** Smaller diffs are easier to verify, revert, and trust.
- **Added:** 2026-03-29
- **Source:** handbook hardening
