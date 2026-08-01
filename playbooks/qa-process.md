# QA Process

## Objective

Define the official quality validation path for functionality, integration, user experience, and release confidence.

## When to use it

Use this playbook after implementation and before release, and whenever a regression, workflow change, or customer-impacting behavior must be validated with evidence.

## Responsible

- QA: execution and evidence capture
- FullStack: implementation support and defect clarification
- Product Manager: acceptance alignment
- Security: risk-driven review support
- DevOps: environment readiness for test execution

## Inputs

- user story or acceptance criteria
- implementation artifact
- environment and release candidate information

## Preconditions

- the feature or fix has a defined scope
- validation target and environment are clear
- relevant acceptance criteria are available for assertion

## Steps

### 1. Define the test scope

- identify unit, integration, E2E, performance, accessibility, and responsive coverage needed
- define what will be validated and what will not

Checklist:
- scope is explicit
- regression surface is known
- edge cases are listed

### 2. Unit tests

- validate isolated logic paths, domain rules, and transformation behavior

Checklist:
- business rules are protected by tests
- error paths are covered where relevant
- unit tests are stable and meaningful

### 3. Integration tests

- validate contract behavior between components, services, and persistence assumptions

Checklist:
- API or service boundary contract is verified
- state transitions are tested with realistic dependencies
- test evidence is reproducible

### 4. E2E tests

- validate full workflows from the user or external-system perspective

Checklist:
- user workflow is represented accurately
- login, navigation, submission, and failure flows are validated
- no critical flow is skipped

### 5. Performance and load validation

- confirm the behavior remains acceptable under realistic usage assumptions

Checklist:
- latency or throughput thresholds are defined
- performance regressions are observed with evidence
- no critical path ignores user impact thresholds

### 6. Accessibility and responsive checks

- check keyboard navigation, contrast, semantics, and viewport behavior

Checklist:
- accessibility issues are identified and documented
- mobile or other key viewport layouts are validated
- user-facing barriers are not accepted quietly

### 7. Release confidence statement

- record the final evidence against acceptance criteria
- confirm whether the release is ready, blocked, or needs mitigation

Checklist:
- evidence is attached to the release item
- incident risk is named if present
- release owner accepts the conditions of readiness

## Common errors

- testing only the happy path
- skipping integration or E2E for “small” changes
- treating accessibility as optional
- using manual QA without a clear evidence record

## Risks

- customer-facing regression escaping production
- poor confidence in release quality
- accessibility or responsive friction after deploy
- performance degradation that only appears at scale

## Best practices

- decide the test strategy before the implementation is considered complete
- test the behavior, not just a mocked representation of it
- preserve evidence tied to the release record
- require coverage of both success and failure paths where risk is material

## Deliverables

- QA test plan
- test evidence and report
- release readiness summary
- remediation or blocker list if needed

## Definition of Done

The QA process is complete when the requested behavior has been validated with appropriate evidence across the necessary levels of testing and the release confidence is explicit enough for the next stage to proceed.

## KPIs

- release defect escape rate
- regression detection rate
- test execution success rate
- mean time to validation

## Recommended tools

- unit and integration test runner
- E2E framework
- browser accessibility tooling
- performance testing toolchain
- issue tracking and evidence attachment flow

## Estimated time

- 0.5 to 2 days for small feature validation
- 2 to 7 days for cross-surface or high-risk releases

## Practical example

A feature that adds a new project creation flow is validated with unit tests around form rules, integration coverage on the API boundary, E2E verification of the user journey, responsive checks on mobile layouts, and performance observation for the initial load and save path.

## Internal references

- [standards/testing.md](../standards/testing.md)
- [standards/performance.md](../standards/performance.md)
- [standards/security.md](../standards/security.md)
- [company/workflow.md](../company/workflow.md)
- [agents/QASecurity.md](../agents/QASecurity.md)
