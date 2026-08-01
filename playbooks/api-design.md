# API Design

## Objective

Define a clear, safe, versionable, and testable contract for application programming interfaces.

## When to use it

Use this playbook when building or changing an API surface exposed to frontend, internal services, or external consumers.

## Responsible

- Product Manager: business contract expectations.
- CTO: architectural fit and boundary design.
- FullStack: endpoint design and implementation.
- QA: contract validation and regression coverage.
- Security: auth, input safety, and threat review.

## Inputs

- business or product requirement
- expected user or consumer flow
- data model assumptions

## Preconditions

- the resource or capability is known
- consumers and ownership are identified
- the desired response contract has a business or technical rationale

## Steps

### 1. Define resources

- name the domain objects and natural relationships
- determine representation boundaries and ownership

Checklist:
- resources are nouns, not verbs
- relationships are explicit and stable
- scope does not mix unrelated business concepts

### 2. Define endpoints

- set path structure and method semantics
- document pagination, filters, sorting, and idempotency where relevant

Checklist:
- verbs are used appropriately
- path naming is consistent
- pagination and filtering rules are explicit

### 3. Define DTOs and request bodies

- define request and response shapes
- establish validation rules for required fields and field types

Checklist:
- DTOs are explicit
- input constraints are documented
- response shapes are predictable

### 4. Define validation rules

- validate at the trust boundary
- normalize unsafe input before business logic

Checklist:
- validation is consistent in all entry points
- invalid requests return documented errors
- security-sensitive fields are protected

### 5. Define error model

- create a shared, stable error contract
- avoid leaking internal implementation details

Checklist:
- status codes are semantically appropriate
- error shape is predictable
- internal errors are classified safely

### 6. Define Swagger/OpenAPI contract

- document endpoints, request/response types, and examples
- ensure the public contract is reviewable

Checklist:
- the contract can be generated or reviewed by consumers
- examples are realistic and not misleading
- version metadata is present

### 7. Define testing strategy

- cover happy paths, validation failures, auth failures, and error semantics
- include contract tests when cross-team consumers exist

Checklist:
- endpoint coverage is meaningful
- test evidence exists for regression protection
- contract mismatch risk is reduced

### 8. Define versioning policy

- decide whether the contract will be versioned by path, header, or media type
- document breaking changes and compatibility expectations

Checklist:
- versioning is explicit
- publish and deprecation plan is named
- breaking changes are controlled

## Common errors

- using verbs in endpoint naming
- allowing undocumented response drift
- coupling business logic inside routing code
- validating only at the UI or only at the database

## Risks

- contract mismatch between frontend and backend
- unstable consumer release due to undisciplined versioning
- input validation gap leading to security or integrity issues

## Best practices

- start from a contract and keep it readable
- set error semantics before implementation
- treat versioning as a product decision, not a coding shortcut
- keep docs and code aligned

## Deliverables

- API contract definition
- endpoint list
- DTOs and validation schema
- OpenAPI/Swagger definition
- test and regression evidence
- release compatibility note

## Definition of Done

The API design is complete when the contract, validation rules, error behavior, version strategy, and test plan are explicit and reviewable by implementation and consumer teams.

## KPIs

- contract mismatch rate
- API review turnaround time
- consumer integration defects
- error contract consistency rate

## Recommended tools

- OpenAPI/Swagger toolchain
- Postman or equivalent API runner
- schema validation library
- contract test framework

## Estimated time

- 0.5 to 2 days for small APIs
- 1 to 2 weeks for multi-team or external-facing API design

## Practical example

A user profile API is defined with the resource `users`, a GET `/v1/users/:id` endpoint, an explicit DTO contract, stable error responses, OpenAPI documentation, and contract tests that prove validation and auth faults fail predictably.

## Internal references

- [standards/api.md](../standards/api.md)
- [standards/security.md](../standards/security.md)
- [standards/testing.md](../standards/testing.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
- [agents/CTO.md](../agents/CTO.md)
