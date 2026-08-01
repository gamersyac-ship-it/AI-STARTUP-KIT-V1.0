# Develop Feature

## Objective

Execute the implementation path for a feature after design approval, keeping delivery evidence, quality discipline, and review readiness intact.

## When to use it

Use this playbook once the feature has a confirmed scope, design artifact, and acceptance criteria.

## Responsible

- FullStack: implementation
- CTO: design guardrails and escalation
- QA: validation support
- Security: risk validation in sensitive paths
- Documentation: operational and release knowledge update

## Inputs

- approved product story
- technical design or ADR
- standards and coding guardrails in scope

## Preconditions

- design is approved or materially accepted by the owner
- implementation branch is created
- quality gates and review expectations are known

## Steps

### 1. Create a clean implementation scope

- branch from the correct source of truth
- break work into reviewable units

Checklist:
- branch naming reflects intent
- task boundary is clear
- local work is isolated from unrelated changes

### 2. Implement against the contract

- follow the approved design and standards
- avoid hidden shortcuts that bypass testing or security rules

Checklist:
- implementation matches the design
- no undocumented behavior is introduced
- contract and data model remain coherent

### 3. Build proof of correctness

- add or update unit and integration coverage
- confirm the feature is testable and edge-case aware

Checklist:
- the most relevant behaviors are covered
- regression risk is addressed with evidence
- quality proof is captured in the PR or ticket

### 4. Review readiness

- ensure the code is readable, isolated, and understandable by a second engineer
- prepare for formal review with evidence

Checklist:
- PR contains meaningful summary
- behavioral link to requirements exists
- implementation no longer relies on implicit assumptions

### 5. Deliver for the next stage

- hand the coded artifact to QA and Security with context
- preserve architecture and release traceability

Checklist:
- change summary is understandable
- rollback and risk notes are available
- environment assumptions are explicit

## Common errors

- shortcutting validation for speed
- mixing implementation with unrelated cleanup
- letting the PR become the only place where reasoning lives
- ignoring edge cases because the happy path is implemented

## Risks

- incomplete validation evidence
- review friction from inconsistent structure
- stable state loss due to feature drift
- release readiness not obvious to operators

## Best practices

- keep implementation increments small and reviewable
- implement directly from approved interface and domain design
- prefer evidence before claiming completion
- document risky assumptions before they become regressions

## Deliverables

- implementation artifact
- PR evidence
- tests or validation coverage
- review summary
- release readiness note

## Definition of Done

The feature is implemented when the change is aligned to the approved design, reviewable by team standards, and backed by enough evidence to transition responsibly into QA and release validation.

## KPIs

- implementation cycle time
- review rejection rate
- test evidence completeness
- rework after review

## Recommended tools

- IDE and source control
- CI pipeline
- test runner
- PR review tooling
- ticketing and documentation system

## Estimated time

- small feature: 0.5 to 2 days
- medium feature: 3 to 7 days
- larger changes: 1 to 3 weeks depending on architecture impact

## Practical example

A feature for resource sharing is implemented across a route, service, and database boundary after the design is approved. The implementation includes a regression test, a PR-ready summary, and evidence for security and QA review.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [standards/clean-code.md](../standards/clean-code.md)
- [standards/testing.md](../standards/testing.md)
- [standards/api.md](../standards/api.md)
- [agents/FullStack.md](../agents/FullStack.md)
