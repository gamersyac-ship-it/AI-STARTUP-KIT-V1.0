# Database Design

## Objective

Define a repeatable process for designing and evolving a database model that is correct, scalable, secure, and maintainable.

## When to use it

Use this playbook when creating a new data model, changing persisted schema, evolving relations, or planning operational performance work.

## Responsible

- CTO: domain and architectural fit
- FullStack: model and migration implementation
- QA: validation of data integrity and regression behavior
- DevOps: environment readiness and migration execution
- Security: access and secret boundary review

## Inputs

- business entity list
- relationships and lifecycle constraints
- migration and deployment assumptions

## Preconditions

- the business domain is understood
- ownership of data model is known
- expected access patterns are identified or approximated

## Steps

### 1. Model the domain

- identify entities and the core business meaning of each one
- define attributes and required invariants

Checklist:
- data model reflects business reality
- required fields are explicit
- model is not shaped by accidental UI representation

### 2. Define relationships

- document cardinality, constraints, and ownership
- decide whether to use reference keys or other relational patterns

Checklist:
- relationship direction is clear
- foreign-key or equivalent guarantees are identified
- edge cases are documented

### 3. Define indexes and access strategy

- choose indexes based on query patterns and risk surface
- avoid indexing every field without evidence

Checklist:
- read-heavy or write-heavy access patterns are documented
- index rationale is visible
- storage and maintenance cost are considered

### 4. Define migrations

- structure schema change as a versioned migration
- create rollback or recovery plan when possible

Checklist:
- migration order is deterministic
- data backfill or data change assumptions are explicit
- rollout is low-risk and reversible when needed

### 5. Define versioning and deployment discipline

- keep schema changes versioned and traceable
- align migration execution with release cutover policy

Checklist:
- migration is tied to a release artifact
- rollout dependency is visible
- environment and rollback owner are known

### 6. Optimize for access and reliability

- optimize for known query patterns
- reduce N+1 and costly scan behavior

Checklist:
- a query strategy exists for important workflows
- any denormalization is justified and documented
- performance and integrity are balanced consciously

### 7. Validate with Prisma or equivalent ORM strategy

- if Prisma is used, align schema, client, and migration flow
- keep the generated contract consistent with the model

Checklist:
- schema and generated client remain in sync
- migration path does not conflict with app assumptions
- data access rules remain safe and explicit

## Common errors

- duplicating data across tables without strong justification
- adding indexes without read-path evidence
- changing schema in manual production steps without migration control
- treating data design as a side effect of UI design

## Risks

- inconsistent schema across environments
- performance degradation due to unplanned query patterns
- data integrity loss from underconstrained relation modeling
- migration failure during high-traffic release windows

## Best practices

- design schema around business meaning first
- use migration discipline, not ad hoc edits
- validate schema with real query patterns before finalizing index strategy
- keep model evolution tied to release evidence

## Deliverables

- domain model description
- relationship map
- index strategy
- migration plan
- versioning note
- optimization rationale
- Prisma schema or equivalent data definition artifact

## Definition of Done

The database design is done when the schema, relations, migration flow, and query optimization decisions are explicit, testable, and aligned with the delivery and release model.

## KPIs

- migration success rate
- query latency for critical paths
- integrity incident rate
- database-related rollback rate

## Recommended tools

- PostgreSQL or approved relational store
- Prisma or equivalent schema-first tooling
- migration runner
- database diagnostics and query explain tools

## Estimated time

- 0.5 to 2 days for a contained model update
- 1 to 3 weeks for a new domain or large schema redesign

## Practical example

A new `projects` domain is modeled with relationships to `users` and `tasks`, a unique constraint on the ownership relationship, a selective index on `updated_at`, and a migration plan that runs as part of controlled deployment.

## Internal references

- [standards/database.md](../standards/database.md)
- [standards/api.md](../standards/api.md)
- [standards/performance.md](../standards/performance.md)
- [company/release-policy.md](../company/release-policy.md)
- [agents/CTO.md](../agents/CTO.md)
