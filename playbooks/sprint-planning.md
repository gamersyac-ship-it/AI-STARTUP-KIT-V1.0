# Sprint Planning

## Objective

Define the formal planning process for converting the roadmap and backlog into a realistic delivery commitment for the next sprint.

## When to use it

Use this playbook whenever the team needs to plan capacity, align scope, and commit to a realistic set of outcomes.

## Responsible

- Product Manager: priority and value alignment
- Engineering Manager or lead: team capacity and implementation realism
- CTO: technical risk and design constraints
- QA and Security: validation capacity and risk-aware scope
- DevOps: delivery and environment readiness constraints

## Inputs

- prioritized backlog items
- known technical dependencies
- current team capacity and delivery constraints

## Preconditions

- backlog items are sufficiently understood
- acceptance criteria or implementation boundaries are available
- capacity is not assumed, only measured

## Steps

### 1. Review current backlog and business priority

- confirm scope priority and business value
- remove or reframe items that are not clearly actionable

Checklist:
- every selected item has a visible business or technical intent
- priority is explicit
- assumptions are not hidden

### 2. Estimate workload and capacity

- estimate the effort required based on complexity, risk, and validation needs
- compute team capacity for the sprint window

Checklist:
- estimate is not overconfident
- planned work matches available capacity
- validation time is treated as part of delivery effort

### 3. Identify risks and dependencies

- list external dependencies, complex design work, environment needs, and release blockers

Checklist:
- critical dependencies are visible and named
- blocked items are isolated from the commitment set when needed
- known risks are not silently carried into delivery

### 4. Commit to the sprint scope

- choose a realistic scope based on capacity and business priority
- explicitly define what is intentionally not included

Checklist:
- the sprint scope is specific and bounded
- “stretch” items are labeled separately
- scope disputes are resolved before implementation starts

### 5. Validate delivery and quality expectations

- ensure QA, security, and release readiness are incorporated in the plan, not assumed after implementation

Checklist:
- test and review time is included
- release risk and support expectation are visible
- dependencies for review and release are known

## Common errors

- committing based on optimism rather than known capacity
- treating estimation and risk as identical
- planning around “will get to it later” assumptions
- forgetting quality and review time in the sprint commitment

## Risks

- missed commitments from unplanned dependencies or hidden complexity
- low-quality delivery under overloaded sprint scope
- business disappointment from promises that were only plausible in an ideal flow

## Best practices

- keep the sprint plan honest and evidence-driven
- separate must-have scope from stretch scope
- identify and communicate risk before the plan is considered settled
- keep an explicit path to review, QA, security, and release within the sprint

## Deliverables

- sprint scope commitment
- backlog selection note
- risk and dependency register
- planned validation and release path

## Definition of Done

The sprint planning process is complete when the team has confirmed scope, capacity, dependencies, and quality expectations with a realistic and reviewable delivery commitment.

## KPIs

- sprint commitment reliability
- scope change rate after planning lock
- planning cycle time
- average story completion rate during the sprint

## Recommended tools

- backlog management board
- sprint planning template
- estimation and capacity worksheet
- risk register and dependency tracker

## Estimated time

- 1 to 2 hours for a small sprint planning session
- 1 day for a broader cross-team planning window

## Practical example

The team reviews a backlog with new product and reliability items, estimates the work against current delivery capacity, identifies a security review dependency on two endpoints, and commits only the scope that can be implemented, validated, and released without hidden quality shortcuts.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [standards/testing.md](../standards/testing.md)
- [agents/ProductManager.md](../agents/ProductManager.md)
