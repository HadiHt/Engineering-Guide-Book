# Architecture Rules

Load this page only for new features, major refactors, or boundary changes.

## Purpose

Define stable ownership boundaries so changes land in the correct layer.

## Frontend

### Typical Layering

- `pages` or route-level modules: composition and feature orchestration
- reusable components: presentation and interaction
- query or mutation hooks: server-state integration
- request modules: transport only
- services: long-lived infrastructure logic
- shared types, constants, and utilities: pure support code

### Data Flow

`UI -> hook -> request module -> HTTP client`

Keep transport, state orchestration, and presentation concerns separate.

## Backend

### Typical Layering

`Controller -> Facade -> Manager -> Repository`

### Ownership

- **Controller:** HTTP boundary, request parsing, validation attributes, response shape
- **Facade:** orchestration and cross-cutting checks
- **Manager:** business logic, domain validation, and mapping
- **Repository:** persistence and data access

### Boundary Rules

- do not put business logic in controllers
- do not put mapping in facades
- do not put persistence logic outside repositories
- do not let shared contracts drift across layers without review

## Cross-Layer Rules

- Contract changes must be traced through all affected layers.
- Permission changes must be explicit.
- Durable architecture decisions should be recorded in the ADR log.
