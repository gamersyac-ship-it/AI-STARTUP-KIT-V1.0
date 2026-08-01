# Security Review

## Objective

Establish the official security review process for engineering changes that could affect access, secrets, data handling, output, or externally exposed behavior.

## When to use it

Use this playbook for new features, API changes, authentication changes, authorization changes, data-handling changes, incident response support, and any release that touches security-sensitive boundaries.

## Responsible

- Security: lead the formal review
- CTO: architecture risk and exception handling
- FullStack: implementation evidence and fix closures
- QA: validation of risk-driven regression paths
- Product Manager: business risk awareness and release prioritization

## Inputs

- design/artifact under review
- auth and authorization scope
- API contract or feature description
- exposure environment and production assumptions

## Preconditions

- the system or feature scope is understood
- the trust boundaries are clear
- review evidence can be tied to a concrete deliverable

## Steps

### 1. Scope exposure and trust boundaries

- identify where data enters and leaves the system
- list the assets, permissions, and risks associated with the change

Checklist:
- boundary of exposure is clear
- data sensitivity is identified
- system owner is clear

### 2. Review authorization and identity

- validate JWT, session, token, or equivalent security model
- verify least privilege and permission boundaries

Checklist:
- role or permission checks are enforced in the right layer
- anonymous or overly broad access is not accepted
- security assumptions are validated with evidence

### 3. Review secrets handling

- confirm secrets are stored and rotated correctly
- confirm no secret or token is present in source, logs, or diagnostics

Checklist:
- secret management is externalized appropriately
- default behavior is safe
- rotation or exposure controls are clearly documented

### 4. Review input and output protections

- inspect user input, file upload, query and body handling, response shaping, and logging
- cover OWASP-relevant classes of flaw

Checklist:
- escaping and validation are appropriate to the technology
- the response does not leak internal state or stack details
- dangerous serialization, injection, or query patterns are ruled out

### 5. Review headers, rate limiting, and transport protection

- verify that required headers and security policies are applied
- confirm exposure controls such as rate limiting are active where necessary

Checklist:
- CORS and other relevant policy decisions are explicit
- rate limit strategy is present where appropriate
- system does not rely on implicit transport safety

### 6. Review logging and auditability

- confirm security-relevant actions are logged consistently and safely
- ensure auditability exists for sensitive operations

Checklist:
- logging does not expose sensitive values
- auth or permission critical actions are traceable
- logs are structured and usable by support and incident teams

### 7. Release decision

- approve, reject, or request mitigations
- keep unresolved risk explicit and business-aware

Checklist:
- all critical concerns are resolved or documented as accepted risk
- evidence is preserved in the review artifact
- owner and follow-up are named

## Common errors

- validating only the happy path
- checking permissions only in the UI layer
- exposing secrets in logs or configuration
- assuming transport protection alone is sufficient

## Risks

- auth bypass or privilege escalation
- secret exposure
- broken security boundaries after refactor
- hidden rate-limit or header configuration gap

## Best practices

- use a consistent review checklist with explicit pass/fail criteria
- include a security owner in every high-risk change
- keep security decisions linked to the release or design artifact
- treat security failures as engineering design issues, not just patch work

## Deliverables

- security review report
- findings list with risk rating
- required remediation evidence
- final approval or blocker note

## Definition of Done

The security review is complete when the authentication and authorization path, secret handling, transport and output protections, and logging needs have been assessed against the current risk and the approval evidence is explicit.

## KPIs

- critical finding closure time
- number of blocker releases prevented
- percentage of changes with documented security evidence
- security review turnaround time

## Recommended tools

- OWASP ZAP or equivalent scanning tool
- static analysis and dependency scanning
- secret scanning in CI
- token and auth test harness
- audit and logging observability

## Estimated time

- 30 minutes to 2 hours for small changes
- 1 to 3 days for sensitive or architecture-level review

## Practical example

A new role-based API feature is reviewed for JWT policy, permission checks in server-side boundaries, secrets handling in environment variables, CORS policy, and rate limiting. The review records a blocker until a server-side role check is enforced and test evidence proves unauthorized access is rejected.

## Internal references

- [standards/security.md](../standards/security.md)
- [standards/api.md](../standards/api.md)
- [standards/testing.md](../standards/testing.md)
- [company/workflow.md](../company/workflow.md)
- [agents/QASecurity.md](../agents/QASecurity.md)
