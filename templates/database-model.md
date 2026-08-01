# Database Model

## Objective

Describe the data entities, relationships, constraints, and access assumptions that a system needs to persist and manage safely.

## When to use it

Use this template when designing or evolving a storage model, relational pattern, or persistence contract for a feature or product area.

## Responsible

- CTO or technical lead: domain and architecture fit
- FullStack: persistence implementation ownership
- QA: integrity and regression validation support
- DevOps: migration and release safety

## Required fields

- Entity or table name
- Purpose of the model
- Core attributes
- Relationships
- Constraints or invariants
- Index or query strategy
- Migration or versioning note
- Owner

## Optional fields

- Data sensitivity classification
- Audit fields
- Soft-delete behavior
- Historical or archival expectations
- Sample usage examples

## Complete example

```md
# Database Model: Workspace Membership

## Objective

Capture and enforce membership relationships between workspaces and users.

## When to use it

Use when a feature relies on tracked collaboration ownership and role-based access.

## Responsible

- CTO: approves domain boundaries and key constraints.
- FullStack: owns schema and application access path.
- DevOps: owns migration and release sequencing.

## Required fields

- Entity or table name: workspace_memberships
- Purpose of the model: represent user membership and role within a workspace
- Core attributes: id, workspace_id, user_id, role, created_at, updated_at
- Relationships: many-to-one to workspace and users
- Constraints or invariants: one user role per workspace membership, role must be validated against an allowed policy
- Index or query strategy: index on workspace_id and user_id, unique composite constraint for membership
- Migration or versioning note: add table within release v1.4.0 migration path
- Owner: Platform Data Engineer
```

## Checklist

- [ ] business meaning of the model is clear
- [ ] relationships and constraints are explicit
- [ ] migration plan is defined if the model changes
- [ ] performance and data integrity concerns are addressed

## Common errors

- modeling around UI needs rather than domain meaning
- storing repeated information with no clear relationship strategy
- leaving migration or rollback plan implicit

## Best practices

- prefer stable domain naming over UI-oriented naming
- document indexes based on actual query patterns
- align the model with the operating release and data integration path

## Related playbooks

- [playbooks/database-design.md](../playbooks/database-design.md)
- [playbooks/api-design.md](../playbooks/api-design.md)
- [playbooks/deployment.md](../playbooks/deployment.md)
