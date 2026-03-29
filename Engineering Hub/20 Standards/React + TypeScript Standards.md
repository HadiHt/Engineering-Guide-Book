# React + TypeScript Standards

Apply these rules to frontend changes.

## Component Design

- Prefer one component per file.
- Split files when they become hard to scan or reason about.
- Keep business logic and transport concerns out of render code.
- Do not use nested ternaries.
- Prefer precomputed values and early returns over dense JSX branching.
- Avoid inline handlers in reusable components when they hurt readability or stability.

## Hooks And Effects

- Use `useEffect` only for real side effects.
- Clean up timers, subscriptions, observers, and listeners.
- Use memoization only when it solves an actual stability or performance problem.

## TypeScript

- Avoid `any`.
- Prefer precise types, `unknown`, and type guards.
- Reuse shared contracts where possible.
- Prefer `as const` and union types over new enums for local constants.
- Avoid magic numbers and repeated literal config.

## Data Flow

Preferred flow:

`UI -> query or mutation hook -> request module -> HTTP client`

- keep request modules focused on transport
- keep hooks focused on server-state behavior
- centralize cache keys and invalidation patterns

## UI, Accessibility, And Safety

- Use semantic HTML and keyboard-accessible controls.
- Do not hardcode user-facing strings if the app uses i18n.
- Check permissions before showing sensitive actions.
- Do not log secrets, tokens, or sensitive payloads.

## Testing

- Keep tests close to the code they cover.
- Prefer behavior-focused tests over implementation-detail tests.
- Mock external side effects explicitly.
- Leave touched code with better clarity, safer types, or lower duplication when that improvement stays in scope.
