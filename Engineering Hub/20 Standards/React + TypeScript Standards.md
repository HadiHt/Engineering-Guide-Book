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

## API Calls

- Do not call `fetch`, `axios`, or SDK clients directly from render code.
- Centralize base URLs, auth headers, common error handling, and transport configuration in the HTTP client or request layer.
- Normalize transport errors before they reach UI components so screens handle product states instead of raw protocol details.
- Pass cancellation or abort signals for requests that should stop on unmount, navigation, or replaced input.
- Keep request and response mapping close to the request layer so transport-specific shapes do not leak through the UI tree.

## UI, Accessibility, And Safety

- Use semantic HTML and keyboard-accessible controls.
- Do not hardcode user-facing strings if the app uses i18n.
- Check permissions before showing sensitive actions.
- Do not log secrets, tokens, or sensitive payloads.

## Mobile Development

- Treat iOS and Android as first-class targets. Do not assume one platform's behavior, layout, or permission model matches the other.
- Respect safe areas, keyboard overlap, orientation changes, and dynamic text sizing in screen layouts.
- Keep touch targets and gesture behavior accessible and predictable.
- Request device permissions only when needed and with user-facing context.
- Design for unstable networks, app backgrounding, and resume flows where mobile users commonly lose state.
- Keep initial render and navigation paths lightweight. Defer non-critical work that would slow startup or screen transitions.
- If the project uses Expo Router, keep screens in `app` or `src/app`, use `_layout` files for navigator and provider boundaries, and keep non-route implementation details outside route files.
- Do not store secrets in plain device storage. Use the platform's secure storage approach when client-side storage is required.

## Testing

- Keep tests close to the code they cover.
- Prefer behavior-focused tests over implementation-detail tests.
- Mock external side effects explicitly.
- Leave touched code with better clarity, safer types, or lower duplication when that improvement stays in scope.
