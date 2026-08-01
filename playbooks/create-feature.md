# Create Feature

## Objective

Define the official workflow for turning a business idea into a validated, documented, and releasable feature.

## When to use it

Use this playbook when a new user-facing or system-facing capability must be planned, implemented, verified, and released.

## Responsible

- Product Manager: feature framing and acceptance criteria.
- CTO: technical feasibility and architecture decision.
- FullStack: implementation and evidence.
- QA: functional validation.
- Security: risk validation.
- DevOps: deployment readiness.
- Documentation: release knowledge update.

## Inputs

- product or business idea
- user story or problem statement
- rollout or release assumptions
- available technical context

## Preconditions

- the problem is understood by the business owner
- a priority exists
- the expected customer or internal value is stated
- the primary risk or dependency is identified

## Steps

### 1. Idea intake

- capture the business intent
- define target user or system consumer
- document expected value and risk

Checklist:
- business problem is specific
- success measure is named
- scope boundary is rough but clear

### 2. Product Manager refinement

- transform the idea into a user story or epic
- define acceptance criteria
- identify constraints, dependencies, and risks

Checklist:
- acceptance criteria are objective
- priority is set
- dependencies are listed

### 3. CTO review

- confirm technical fit
- decide architecture, trade-offs, and constraints
- approve or conditionally reject the path

Checklist:
- architecture concerns are named
- security and maintainability are included
- ADR or design note is created if needed

### 4. Technical design

- define endpoints, schema, UI interaction, error handling, and observability
- record decisions in design documentation

Checklist:
- contract is explicit
- data model assumptions are visible
- edge cases are considered

### 5. Implementation

- implement only what is required by the approved acceptance criteria
- keep logic separated by responsibility
- maintain testability and traceability

Checklist:
- code follows applicable [standards](../standards/README.md)
- the implementation is reviewable
- the delivery does not hide complexity in UI or controllers

### 6. QA validation

- validate happy path and edge cases
- create or update regression coverage
- confirm the release candidate behaves as expected

Checklist:
- unit and integration coverage exists where needed
- E2E or user flow is validated
- defects are recorded and triaged

### 7. Security validation

- review auth, permissions, secrets, logs, and input paths
- confirm risk is acceptable or unresolved items are explicitly tracked

Checklist:
- no critical access issue remains
- secrets are not exposed
- error handling does not leak internals

### 8. Deploy readiness

- confirm environment, rollout plan, and rollback path
- check documentation and observability

Checklist:
- deployment owner is clear
- rollback is documented
- monitoring hooks are active

### 9. Documentation update

- update user-facing or internal docs
- record operational notes and dependencies

Checklist:
- required docs are updated in the correct location
- release notes are aligned with behavior

### 10. Release

- ship under the approved versioning policy
- communicate user impact and support ownership

Checklist:
- release scope is traceable
- communication is clear
- support owner is named

## Common errors

- starting development before approval
- skipping architecture review for new patterns
- documenting after release instead of before
- relying on manual QA without evidence

## Risks

- business ambiguity
- architectural overreach
- release hidden defects
- undocumented security impact

## Best practices

- keep the workflow evidence-based
- define the entry criteria before engineering starts
- avoid “hidden” handoffs between teams
- maintain a single source of truth for delivery state

## Deliverables

- approved story or epic
- technical design evidence
- implemented feature
- QA evidence
- security review evidence
- deployment note
- documentation update
- release communication

## Definition of Done

The feature is done when it is implemented, reviewed, validated, secured, documented, and proven releasable through evidence and traceable release ownership.

## KPIs

- feature cycle time
- defect escalation rate
- review turnaround time
- release rollback rate

## Recommended tools

- project management board
- issue tracker
- code review platform
- CI/CD pipeline
- test reporting
- observability dashboards

## Estimated time

- 1 to 5 days for small features
- 1 to 3 weeks for cross-team or architecture-heavy features

## Practical example

A “project sharing” feature enters the workflow as a Product Manager story, is reviewed by the CTO for access and data boundary concerns, implemented with a shared API contract, validated in QA, confirmed for security, and finally rolled out with release notes and docs.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [standards/api.md](../standards/api.md)
- [standards/testing.md](../standards/testing.md)
- [standards/security.md](../standards/security.md)
- [agents/ProductManager.md](../agents/ProductManager.md)
- [agents/CTO.md](../agents/CTO.md)
- [agents/QASecurity.md](../agents/QASecurity.md)
- [agents/DevOps.md](../agents/DevOps.md)
