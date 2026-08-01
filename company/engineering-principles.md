# Engineering Principles

The engineering principles in this framework define how the company makes technical decisions under real delivery pressure.

## 1. SOLID

### What it means

A set of design rules that help keep software maintainable, understandable, and extensible.

### When to apply it

When designing classes, services, and organizational boundaries for business logic.

### Example

A service should encapsulate one domain responsibility and expose a clean interface instead of mixing validation, persistence, and presentation concerns.

### Common mistakes

- creating a god service,
- hiding domain rules in controllers or UI layers,
- making entities responsible for everything.

## 2. DRY

### What it means

Do not duplicate logic when it can be expressed once and reused safely.

### When to apply it

For cross-cutting logic, validators, utilities, domain services, and shared integrations.

### Example

A standardized API error formatter should be centralized instead of repeated in each endpoint.

### Common mistakes

- abstracting too early,
- over-generalizing small code paths,
- reducing readability to satisfy the principle mechanically.

## 3. KISS

### What it means

Keep solutions as simple as possible while still meeting the requirement.

### When to apply it

At every stage of design, especially when balancing speed, maintainability, and clarity.

### Example

Choose a direct domain flow over a complex event bus when the business problem does not require asynchronous distribution.

### Common mistakes

- adding premature abstraction,
- using a complicated pattern for a simple workflow.

## 4. YAGNI

### What it means

Do not build features or abstractions that are not currently needed by a real requirement.

### When to apply it

When deciding what to implement in a release or sprint.

### Example

Avoid building a generic plugin system for a single internal service that will never need extension.

### Common mistakes

- speculative architecture,
- building for imagined future use cases too early.

## 5. Clean Architecture

### What it means

Structure the software so business rules are not coupled to frameworks, UI, or infrastructure details.

### When to apply it

When designing a new product or major module.

### Example

Use domain services and ports/adapters so the business flow remains stable even if storage or transport changes.

### Common mistakes

- business logic spread across controllers and repositories,
- direct dependence on framework-specific patterns.

## 6. Separation of Concerns

### What it means

Each part of the system should own a clear, distinct responsibility.

### When to apply it

During component design, API design, and data model evolution.

### Example

UI components should not own persistence logic, and service layers should not build UI structures.

### Common mistakes

- mixing request handling, business rules, and persistence in one layer,
- hiding responsibilities behind broad helper functions.

## 7. Fail Fast

### What it means

Detect invalid assumptions and unsafe conditions early.

### When to apply it

During validation, startup, integration, and service boundary checks.

### Example

Reject invalid request payloads immediately at the API boundary rather than allowing them to propagate deeper.

### Common mistakes

- deferred validation,
- silent fallback behavior that hides broken states.

## 8. Secure by Design

### What it means

Build with secure assumptions from the beginning rather than patching later.

### When to apply it

For every feature that handles user identity, data, secrets, or external systems.

### Example

Use least privilege, strong defaults, and safe error handling in authentication and authorization flows.

### Common mistakes

- trusting client input,
- logging sensitive values,
- exposing internal infrastructure details.

## 9. API First

### What it means

Define interfaces and contracts before implementation details are finalized.

### When to apply it

When designing integrations between systems, frontend and backend, or internal services.

### Example

Draft the request/response schema, auth requirements, and error semantics before building the endpoint implementation.

### Common mistakes

- undocumented contracts,
- mismatched frontend and backend assumptions.

## 10. Testability

### What it means

Code should be written in a way that makes verification straightforward.

### When to apply it

For logic, APIs, business workflows, and release-critical behaviors.

### Example

Keep domain logic pure or service-oriented so it can be executed and validated with tests.

### Common mistakes

- hard-to-isolate side effects,
- tests attached only to happy-path behavior.

## 11. Maintainability

### What it means

A system should be easy to understand, evolve, and operate over time.

### When to apply it

When evaluating architecture, code structure, documentation, and delivery practices.

### Example

A clear module boundary and readable names reduce the operational burden when new contributors join.

### Common mistakes

- over-engineering,
- stale documentation,
- hidden dependencies and unclear ownership.

## Relationship to Other Documents

These principles shape technical decision-making and should be read alongside:

- [vision.md](vision.md)
- [mission.md](mission.md)
- [values.md](values.md)
- [workflow.md](workflow.md)
- [release-policy.md](release-policy.md)
