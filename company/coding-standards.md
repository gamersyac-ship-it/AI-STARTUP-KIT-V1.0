# Coding Standards

## Scope

These standards apply to all implementation work produced by the framework across full-stack, backend, frontend, data, testing, automation, and release processes.

## General Rules

- Prefer clarity over cleverness.
- Keep functions and modules small and purpose-specific.
- Avoid hidden side effects.
- Use explicit names and predictable flows.
- Add comments only where behavior is not obvious.

## Quality Expectations

- Write tests for critical business behavior.
- Keep public interfaces predictable.
- Make failure modes observable.
- Keep versioned contracts and migrations traceable.

## Frontend

- Make components reusable and composable.
- Avoid business logic in markup layers.
- Keep accessibility and keyboard support by default.
- Prefer deterministic state handling.

## Backend

- Validate input at boundaries.
- Apply authorization and error handling consistently.
- Never log secrets or sensitive operational data.
- Use structured errors and domain-level exceptions.

## Data

- Document schema intent and migration purpose.
- Use safe defaults and explicit constraints.
- Keep read and write models aligned with business meaning.

## Release Readiness

- Production code must be testable.
- Migrations must be reversible when possible.
- Every deployment must have a documented rollback path.
