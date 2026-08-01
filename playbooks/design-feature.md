# Design Feature

## Objective

Translate a product requirement into a technically reviewable design that can be implemented safely and measured for quality.

## When to use it

Use this playbook before implementation when the change has a material technical boundary, dependency, interface change, or quality-risk exposure.

## Responsible

- Product Manager: outcome and acceptance alignment
- CTO: architecture and approval authority
- FullStack: technical draft and implementation feasibility
- Security: risk analysis for sensitive flows
- QA: testability and validation expectations

## Inputs

- story or epic
- business objective
- known constraints and release expectations

## Preconditions

- the business need is clear
- success criteria are known
- the design owner is named

## Steps

### 1. Scope and constraints

- confirm what is in scope and what is out of scope
- capture dependencies and edges

Checklist:
- scope is explicit
- assumptions are visible
- non-goals are identified

### 2. Domain mapping

- map the feature to existing modules, services, routes, or UI boundaries
- identify where responsibilities should live

Checklist:
- each domain responsibility is assigned to one layer
- coupling is minimized
- reuse opportunities are recognized

### 3. Interface design

- define the API, UI flows, and data exchange boundaries
- capture DTOs, validation, and error response expectations

Checklist:
- interfaces are documented before implementation
- contract changes are intentional and reviewed
- edge cases are listed

### 4. Architecture decision

- document the chosen architectural style and why it is appropriate
- state what is intentionally not being built

Checklist:
- alternatives are considered
- trade-offs are stated
- long-term maintainability is addressed

### 5. Testability and observability

- decide what evidence will prove the feature works
- identify logs, metrics, or traces that matter

Checklist:
- success criteria can be tested
- operational visibility is defined
- rollback or recovery path is considered

### 6. Approval gateway

- present the design to the relevant decision-makers
- require explicit acceptance, not silent continuation

Checklist:
- design ownership is assigned
- architectural risks are listed
- product and engineering alignment are confirmed

## Common errors

- jumping into code before interfaces are stable
- overdesigning for imagined future needs
- leaving test and observability decisions implicit
- allowing design drift between product and engineering

## Risks

- hidden complexity after implementation starts
- poorly bounded feature ownership
- insufficient contract clarity
- deployment-specific assumptions being baked into design

## Best practices

- keep the design factual and reviewable
- make the design small enough to be implemented safely
- record decisions with rationale
- tie design to a release or operational expectation

## Deliverables

- technical design note
- interface definition
- architecture decision summary
- QA validation plan
- security review inputs
- implementation readiness statement

## Definition of Done

The design is done when it is explicit enough for implementation, reviewable by the responsible engineering leaders, and aligned with quality, security, and operational requirements.

## KPIs

- design review cycle time
- rework after implementation begins
- number of architecture decisions documented
- defect rate caused by ambiguous design

## Recommended tools

- ADR or decision record templates
- architecture diagrams
- API schema tooling
- ticketing and review workflow

## Estimated time

- 0.5 to 1 day for small features
- 2 to 5 days for cross-team or architectural changes

## Practical example

A feature that allows organization-level sharing is designed by mapping the data model, defining a permissions contract, writing the API boundaries, and documenting a fallback path if the security review requires a stricter access model.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
- [standards/api.md](../standards/api.md)
- [standards/clean-architecture.md](../standards/clean-architecture.md)
- [agents/CTO.md](../agents/CTO.md)
