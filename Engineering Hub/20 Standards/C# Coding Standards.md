# C# Coding Standards

Apply these rules to backend changes.

## Naming And Readability

- Use standard .NET naming conventions.
- Use braces for control flow blocks.
- Remove unused `using` directives.
- Prefer string interpolation over concatenation.
- Keep classes and methods focused and clearly named.

## `var` Usage

Use `var` when the type is obvious from the right-hand side or when the explicit type adds noise.

Avoid `var` when it hides intent.

## Layering

Preferred backend flow:

`Controller -> Facade -> Manager -> Repository`

- **Controller:** HTTP boundary only
- **Facade:** orchestration and cross-cutting checks
- **Manager:** business logic, validation, and mapping
- **Repository:** persistence only

## Rules

- Do not put business logic in controllers.
- Do not put mapping in facades.
- Do not put persistence logic outside repositories.
- Use domain-specific exceptions and let the HTTP layer map them consistently.
- Make authorization explicit for new endpoints.

## Outbound API Calls

- Use `IHttpClientFactory` for outbound HTTP clients. Do not create and dispose `HttpClient` instances ad hoc.
- Keep integration-specific base addresses, headers, timeouts, and resilience behavior in a dedicated client or service.
- Keep I/O asynchronous end-to-end. Do not block on `Task.Result`, `Task.Wait`, or wrap synchronous I/O in `Task.Run`.
- Pass `CancellationToken` through outbound calls and long-running operations when the caller provides one.
- Map remote DTOs at the integration boundary so transport contracts do not leak through business logic.

## SignalR

- Use SignalR for real-time server push, notifications, dashboards, or collaboration flows. Do not use it as a general replacement for normal request-response APIs.
- Treat hubs as transient. Do not store per-connection or shared state in hub instance fields or properties.
- Always `await` asynchronous hub sends and client invocations that must complete before the hub method returns.
- Use strongly typed hubs when the client contract is important enough to benefit from compile-time checking.
- Send messages from controllers, managers, or background services through `IHubContext`; do not instantiate hubs directly.

## Concurrency, Background Work, And Loops

- Keep hot paths asynchronous and non-blocking.
- Do not access `HttpContext` from multiple threads or capture it for work that continues after the request boundary.
- Use `BackgroundService` or `IHostedService` for long-running or queued background work instead of keeping work inside HTTP requests.
- Keep `StartAsync` short. Put long-running execution in `ExecuteAsync`.
- When a background service needs scoped dependencies, create a scope explicitly.
- Long-running loops must honor `CancellationToken`, await their delays with the same token, and avoid tight polling loops.

## Logging

- Use `ILogger<T>` and structured message templates with named placeholders.
- Log enough identifiers and state to diagnose a problem, but never log secrets, tokens, or sensitive payloads by default.
- Configure log levels in configuration and keep noisy framework categories tighter than app categories in production.
- Prefer source-generated `LoggerMessage` patterns in hot or high-volume code paths.

## Testing

- Prefer specific assertions over broad failure checks.
- Avoid redundant assertions after null guards.
- Add or update tests for changed behavior where practical.
