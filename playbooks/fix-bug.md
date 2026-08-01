# Fix Bug

## Objective

Provide a disciplined workflow for bug discovery, classification, root cause identification, remediation, validation, and prevention.

## When to use it

Use this playbook for any defect that affects correctness, customer value, security, availability, or quality expectations.

## Responsible

- QA or Product Manager: initial triage and reproduction evidence.
- CTO: architectural and severity review.
- FullStack: fix implementation.
- Security: risk assessment when security is implicated.
- DevOps: production mitigation and rollback support.
- Documentation: knowledge capture and prevention note.

## Inputs

- defect report
- reproduction steps
- logs, traces, user impact, and affected environment

## Preconditions

- the bug is reproducible or has credible evidence
- the impact is known
- the owner of the failing area is identified

## Steps

### 1. Classify severity

Classify the bug as Critical, High, Medium, or Low.

- Critical: data loss, privilege bypass, outage, major customer-impacting failure.
- High: material product failure or elevated reliability risk.
- Medium: degraded but recoverable experience.
- Low: cosmetic or low-impact issue.

Checklist:
- severity is explicit
- customer impact is documented
- escalation path is clear

### 2. Triage and reproduction

- confirm reproduction path
- isolate the failing environment and scope
- record measurable evidence

Checklist:
- steps to reproduce are clear
- logs or screenshots exist
- affected release or environment is known

### 3. Root Cause Analysis

- trace data flow and execution path
- identify the nearest breaking assumption or missing validation
- capture why it happened, not just what happened

Checklist:
- the causal path is described
- missing guard or bad contract is identified
- the issue is not merely symptom-handled

### 4. Fix design

- define the minimal safe correction
- decide whether a hotfix, patch, or standard fix path is appropriate
- document rollback implications

Checklist:
- fix scope is narrow and controlled
- risk of regression is understood
- the mitigation path is safe

### 5. Implementation

- change only the affected behavior or contract boundary
- add or update tests for the failing case
- keep the fix readable and reviewable

Checklist:
- regression test exists
- no unrelated code is mixed into the patch
- implementation follows the applicable [standards](../standards/README.md)

### 6. Validation

- validate the fix against the failing scenario
- run regression checks and release-level validations relevant to the impacted area

Checklist:
- the original issue no longer reproduces
- affected paths continue to pass
- evidence is stored with the work item

### 7. Prevention

- identify a preventive control
- add test coverage, guardrails, monitoring, or process improvements

Checklist:
- prevention action is concrete
- ownership is assigned
- the action links to the root cause

## Common errors

- fixing the symptom without understanding the root cause
- deploying without regression evidence
- classifying severity too late
- leaving a production issue without preventive closure

## Risks

- hidden regression from a narrow fix
- poor escalation for user-impacting bugs
- insufficient production visibility
- incomplete post-fix documentation

## Best practices

- prioritize traceability from issue to fix to validation
- classify early and escalate to the right decision-maker
- avoid “quick patches” that hide design issues
- make the prevention action part of the fix commitment

## Deliverables

- triage note
- severity classification
- RCA artifact
- code change and tests
- validation evidence
- prevention action record

## Definition of Done

The bug is done when the defect is corrected, evidence confirms the behavioral change, prevention is captured, and the production risk is materially reduced.

## KPIs

- mean time to triage
- mean time to resolve
- bug recurrence rate
- defect escape rate

## Recommended tools

- issue tracker
- log and tracing platform
- CI test execution
- observability dashboards
- release change records

## Estimated time

- 30 minutes to 2 hours for low-impact local bugs
- 1 to 3 days for production or cross-team incidents

## Practical example

A broken pagination endpoint is reported by QA with reproduction steps. Severity is set to High because it affects user navigation. The investigation reveals a missing guard in the database query path, the fix is applied with regression tests, validation confirms the issue is resolved, and a contract test is added to prevent future mismatches.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [company/incident-management.md](../company/incident-management.md)
- [standards/testing.md](../standards/testing.md)
- [standards/error-handling.md](../standards/error-handling.md)
- [standards/security.md](../standards/security.md)
