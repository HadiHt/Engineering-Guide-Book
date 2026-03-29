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

## Testing

- Prefer specific assertions over broad failure checks.
- Avoid redundant assertions after null guards.
- Add or update tests for changed behavior where practical.
