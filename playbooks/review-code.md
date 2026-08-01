# Review Code

## Objective

Define a professional, evidence-oriented code review process that improves correctness, maintainability, security, and team alignment.

## When to use it

Use this playbook every time a change is proposed for merge, release, or shared ownership by the team.

## Responsible

- reviewer(s): assess correctness and standards alignment
- author: provide context and evidence
- CTO or lead: resolve architectural disputes
- QA and Security: validate risk-related review focus when relevant

## Inputs

- pull request or merge request
- code diff and change summary
- test or validation evidence
- design or requirement reference

## Preconditions

- the change has a clear purpose
- the relevant context is available
- the review target is not hidden behind ambiguous titles or missing evidence

## Steps

### 1. Understand the intent

- read the summary, linked story, and surrounding context
- confirm what the author is trying to achieve

Checklist:
- intent is understandable
- scope is bounded
- the change is not mixing unrelated concerns

### 2. Assess design and domain fit

- confirm the implementation aligns with the approved architecture and domain boundaries
- reject if the change introduces hidden coupling, duplication, or unclear ownership

Checklist:
- the design is coherent
- responsibilities are still cleanly separated
- the code reflects the expected system model

### 3. Review for correctness

- validate logic, edge cases, and failure handling
- confirm the change satisfies the acceptance criteria

Checklist:
- the implementation does what it claims
- missing validations are surfaced
- the code does not introduce unsafe defaults

### 4. Review for standards compliance

- verify alignment with relevant standards in [standards/README.md](../standards/README.md)
- identify naming, structure, style, testing, and documentation compliance

Checklist:
- applicable standards are referenced
- style is consistent
- code readability has been preserved

### 5. Review for security and quality

- verify secrets, auth, permissions, logging, and validation paths
- confirm the code is testable and safe under failure conditions

Checklist:
- no sensitive data exposure or log leakage is present
- quality evidence is sufficient to accept the change
- important risk paths are explicitly considered

### 6. Approve, reject, or request changes

- approve when evidence is sufficient and risk is acceptable
- reject when the change is unsafe, incomplete, or conceptually misaligned
- request changes when the implementation is close but needs targeted corrections

Checklist:
- review decision is explicit
- blocking issues are named precisely
- the path to completion is described

## What to reject

- changes that bypass test or security controls
- broad refactors hidden inside feature work
- code with unclear ownership or hidden side effects
- any change whose evidence does not justify risk

## What to approve

- well-scoped, readable, and evidence-backed changes
- consistently styled implementation aligned to standards
- change that clearly maps back to intent and validation criteria

## Common errors

- reviewing only the diff visually while ignoring context
- approving on code style alone
- missing dangerous assumptions in validation or authorization
- allowing “it looks fine” to replace requested evidence

## Risks

- defects slipping through due to weak review discipline
- silent architectural drift from undocumented review decisions
- low-quality release standards if reviewers do not enforce evidence

## Best practices

- review for understanding first, then for standards
- keep comments actionable and specific
- favor concrete evidence over subjective wording
- escalate architectural concerns to the owner of the decision

## Deliverables

- review feedback
- approval or rejection decision
- list of required corrections
- final merge evidence

## Definition of Done

A code review is complete when the reviewers have evaluated the implementation against intent, standards, failure behavior, and release impact, and the decision is recorded clearly for the author and maintainers.

## KPIs

- review turnaround time
- review rejection or rework rate
- defect escape rate after merge
- standards compliance rate in PRs

## Recommended tools

- pull request review workflow
- CI evidence and test reports
- static analysis and lint tools
- security scan tools

## Estimated time

- 15 minutes for small contained changes
- 1 to 2 hours for standard feature reviews
- longer for architecture-sensitive or risk-heavy work

## Practical example

A PR is reviewed for a data fetch endpoint. Reviewers confirm the request contract is correct, the auth check is enforced at the boundary, the response error shape is stable, and regression tests close the relevant bug path. The PR is approved only after these checks are evident.

## Internal references

- [standards/code-style.md](../standards/code-style.md)
- [standards/testing.md](../standards/testing.md)
- [standards/security.md](../standards/security.md)
- [company/workflow.md](../company/workflow.md)
- [agents/CTO.md](../agents/CTO.md)
