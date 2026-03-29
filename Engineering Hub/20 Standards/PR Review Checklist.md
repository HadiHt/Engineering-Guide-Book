# PR Review Checklist

Use this as a merge gate.

If any required item fails, the change is not ready.

## Shared Checks

- [ ] Scope matches the requested work
- [ ] Behavior changes are intentional and clear
- [ ] No obvious regression risk remains in touched flows
- [ ] Security, permission, and data-handling impact were reviewed
- [ ] No secrets or sensitive payloads were introduced
- [ ] Tests were added or updated where needed
- [ ] Relevant validation passed, or failures are clearly explained
- [ ] No dead code or commented-out code remains in touched files
- [ ] PR description explains the change and any notable risks

## Frontend Checks

- [ ] UI states are covered where relevant: loading, error, empty, success
- [ ] Data flow follows the project pattern
- [ ] API calls stay in hooks and request modules, with cancellation and error handling in the correct layer
- [ ] User-facing text follows the app's i18n approach
- [ ] Accessibility basics are present
- [ ] For mobile work, layouts and interactions were checked for safe areas, keyboard handling, touch targets, and platform-specific behavior
- [ ] For mobile work, permission flows, offline behavior, and resume/background handling were reviewed where relevant
- [ ] Types are precise enough for the changed area

## Backend Checks

- [ ] Layering is respected
- [ ] Controller, orchestration, business logic, and persistence concerns are separated correctly
- [ ] Contract changes were traced through affected layers
- [ ] Authorization and exception behavior are explicit
- [ ] Outbound API calls, background work, and loops honor async, cancellation, and ownership boundaries
- [ ] SignalR changes respect hub lifetimes, `IHubContext` usage, and delivery assumptions
- [ ] Logging is structured, appropriately scoped, and free of sensitive payloads

## Git And Merge Hygiene

- [ ] Branch and commit naming are consistent with team standards
- [ ] History is readable
- [ ] Required approvals are in place
