# Architecture Review

## Objective

Define the formal evaluation path for judging whether a technical design is healthy, scalable, secure, and aligned with the system’s real operating constraints.

## When to use it

Use this playbook when a new module, integration, or major technology decision needs formal technical approval.

## Responsible

- CTO: architecture approval and ownership
- Product Manager: business constraint and value context
- FullStack: implementation feasibility and design quality
- Security: review of trust boundaries and exposure risk
- DevOps: operational fit and delivery implications

## Inputs

- feature, initiative, or module scope
- current system and dependency context
- design notes or ADRs

## Preconditions

- the architecture problem is explicit
- the business or technical risk is defined
- the review audience is known

## Steps

### 1. Review business and technical context

- confirm what the architecture is expected to enable
- identify the stability, speed, and scale assumptions behind it

Checklist:
- problem statement is clear
- architectural intent is explicit
- risk and value are linked to a business or operational outcome

### 2. Review structural fit

- confirm the proposed separation of domain, transport, data, and external dependencies
- ensure the design remains maintainable and testable

Checklist:
- the design supports modularity
- responsibilities are not hidden or duplicated
- long-term maintainability receives explicit consideration

### 3. Review security and reliability boundaries

- confirm the decision does not create major trust or failure exposure without mitigation

Checklist:
- security concerns are enumerated
- operational recovery or rollback expectations are named
- important failure modes are known

### 4. Review implementation and delivery implications

- confirm the solution can be built, tested, deployed, and supported by the team in the agreed operating model

Checklist:
- implementation complexity is understandable
- engineering capacity and release constraints are considered
- supportability is not left implicit

### 5. Record the decision

- write the architecture decision, rationale, alternative, and the acceptance criteria that will define whether the design is considered successful

Checklist:
- the decision is traceable and reviewable
- approval or rejection is explicit
- follow-up obligations are named

## Common errors

- approving a design without a traceable decision record
- reviewing only the code shape and not the operating model
- treating architecture as a one-time signoff rather than a durable decision
- ignoring the security and support cost of the chosen pattern

## Risks

- poor long-term maintainability
- hidden operational complexity
- security or data boundary errors in the design
- release difficulty caused by oversized or unstable patterns

## Best practices

- architecture reviews should create durable decisions
- a good review results in explicit constraints and follow-up evidence
- the architecture should be understandable to the people supporting it
- the review should protect delivery from hidden coupling and over-engineering

## Deliverables

- architecture review summary
- approved or rejected design decision
- linked ADR or decision record
- residual risk record and approval criteria

## Definition of Done

The architecture review is complete when a decision is recorded with clear rationale, constraints, implementation implications, and measurable approval criteria.

## KPIs

- architecture decision documentation rate
- number of architecture-led incidents or defects
- review turnaround time
- rework caused by architectural ambiguity

## Recommended tools

- ADR templates and design notes
- diagramming toolchain
- security and dependency review process
- release or implementation evidence repository

## Estimated time

- 0.5 to 2 days for standard design review
- several days for broad architectural changes or platform-level decisions

## Practical example

A platform team proposes a new event-driven integration between multiple services. The architecture review confirms that the boundary design is sound, the data ownership is explicit, the service reliability and recovery model is documented, and the final approval record contains the constraints, risks, and follow-up actions.

## Internal references

- [company/engineering-principles.md](../company/engineering-principles.md)
- [company/workflow.md](../company/workflow.md)
- [standards/clean-architecture.md](../standards/clean-architecture.md)
- [agents/CTO.md](../agents/CTO.md)
