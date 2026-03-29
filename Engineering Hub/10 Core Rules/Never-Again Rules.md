# Never-Again Rules

This is the short list of mistakes that must not repeat.

Read it at the start of every engineering session.

Use this file for stable, high-confidence rules that deserve permanent placement in the core handbook.

If you want to add a new rule quickly without editing the core handbook, add it to `Engineering Hub/15 Dynamic Rules` instead.

## How To Add A Rule

Each rule should describe a repeatable pattern, not just a one-off bug.

Template:

### [RULE-ID] - Short Title

- **Scope:** `frontend` | `backend` | `both`
- **Rule:** One sentence
- **Why:** One sentence
- **Caught in:** task, PR, or incident reference
- **Date added:** YYYY-MM-DD

## Active Rules

### RULE-003 - Do Not Treat Project Memory As A File Path Convention

- **Scope:** both
- **Rule:** Refer to the project memory system using whatever form the current workflow expects, instead of assuming a specific export path or storage format.
- **Why:** Export formats change. The workflow should survive tooling changes.
- **Caught in:** hub cleanup
- **Date added:** 2026-03-27

### RULE-002 - Detect Scope Before Loading Standards Or Writing Code

- **Scope:** both
- **Rule:** Determine whether the task is frontend, backend, or both before loading detailed standards or editing code.
- **Why:** Scope controls which rules apply and prevents wrong-layer changes.
- **Caught in:** workflow design
- **Date added:** 2026-03-27

### RULE-001 - Keep Logic In The Correct Layer

- **Scope:** backend
- **Rule:** Do not place business logic, mapping, orchestration, and transport concerns in the same layer.
- **Why:** Blurred layer ownership makes changes harder to test and easier to break.
- **Caught in:** architecture review
- **Date added:** 2026-03-27
