# AI Local Review Protocol

Run this before opening a PR or declaring the task done.

## Inputs

- current task goal
- detected scope
- relevant standards
- touched files and diff

## Review Order

1. Inspect the changed files and nearby call sites.
2. Check behavior first: correctness, regressions, and edge cases.
3. Check contracts and types.
4. Check permissions, security, and data handling where relevant.
5. Check layering and architecture if the task touched boundaries.
6. Check tests and validation coverage.
7. Run targeted validations, then broaden if needed.

## Severity Model

- **P0:** data loss, security failure, or severe production risk
- **P1:** major correctness or contract break
- **P2:** important reliability or maintainability issue
- **P3:** minor quality improvement

## Pass Criteria

- no unresolved P0 or P1 issues
- relevant validations passed, or failures are clearly explained
- residual risks are documented
- the task meets the Definition of Done
