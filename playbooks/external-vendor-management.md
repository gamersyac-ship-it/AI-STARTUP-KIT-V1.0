# External Vendor Management

## Objective

Define the official process for selecting, governing, onboarding, reviewing, and retiring external providers that affect engineering outcomes, customer trust, or company operating risk.

## When to use it

Use this playbook when the organization evaluates a SaaS vendor, third-party API provider, cloud dependency, support partner, or external service that interacts with product, security, or operations.

## Responsible

- CTO or technical lead: technical fit and architectural risk
- Product Manager: business need and business owner alignment
- Security: vendor security posture and compliance review
- DevOps or procurement owner: onboarding, dependencies, and operational continuity
- Documentation: knowledge and contract recordkeeping

## Inputs

- business or technical need
- vendor proposal or service contract
- risk, dependency, and integration assumptions

## Preconditions

- the vendor need is explicit and tied to a real business or engineering requirement
- the ownership of the relationship is named
- the minimum acceptable security and support posture is defined

## Steps

### 1. Define the need and selection criteria

- state the business problem, scope of use, expected value, and service expectation
- record what would make the vendor acceptable or unacceptable

Checklist:
- the need is concrete
- critical selection criteria are visible
- no vague “we may need this later” criteria are allowed

### 2. Evaluate the provider technically and operationally

- review service fit, support responsiveness, SLA, integration complexity, and uptime expectations
- confirm whether the vendor and its contract are compatible with the company’s standards and control needs

Checklist:
- technical fit is reviewed
- operational disruption risk is visible
- support plan and escalation path are understood

### 3. Review security posture and compliance

- inspect authentication, access control, data-handling, incident response, regional compliance needs, and support boundary expectations

Checklist:
- critical security questions are answered
- secrets, PII, or regulated data exposure is clearly mapped
- the vendor is not accepted without security risk visibility

### 4. Define the integration and governance model

- document where the vendor enters the system, what contracts are in place, and what notification or monitoring path will be used
- define owner responsibility for the service relationship

Checklist:
- integration boundary is explicit
- data ownership and auditability are clear
- escalation and renewal owner are named

### 5. Onboard and validate the real operational path

- confirm the integration path, environment configuration, and support rehearsal path before production use

Checklist:
- onboarding is not based solely on marketing material
- test and validation path exists
- production support and emergency contact process are ready

### 6. Review continuously and renew deliberately

- track vendor changes, incident history, support quality, and contract drift
- review whether the relationship remains aligned to the original need and safety posture

Checklist:
- renewal is not automatic without a meaningful review
- risk review remains active for the service
- service value is still clearly present

### 7. Retire or replace when the need ends

- preserve evidence of the service, the contract, the exit path, and the migration or replacement plan

Checklist:
- decommission path is known
- important data and access state are cleanly transferred or removed
- offboarding does not create hidden dependency on a provider that is no longer needed

## Common errors

- picking vendors because they are popular rather than suitable
- accepting third-party dependencies without security review
- treating vendor onboarding as a one-time procurement step instead of a continuing operational relationship
- leaving the exit path undocumented until the contract is already ending

## Risks

- dependency on a weakly supported or insecure provider
- business failure due to integration drift or vendor downtime
- hidden data exposure or insufficient incident response alignment
- support burden becoming a long-term cost center without a clear value return

## Best practices

- treat vendor governance as part of product and engineering risk management
- review the provider at two levels: technical fit and operational resilience
- require security and support evidence before onboarding production usage
- keep the relationship decision traceable and reviewable by the company

## Deliverables

- vendor selection note
- technical and security evaluation summary
- onboarding and implementation evidence
- operational ownership and contract record
- offboarding or replacement plan

## Definition of Done

The external vendor management process is complete when the provider is selected for a documented need, governed by clear ownership and security expectations, validated in practice, and maintainable through a known lifecycle from contract to exit.

## KPIs

- vendor onboarding time
- support escalation response quality
- security review closure rate
- vendor dependency concentration rate

## Recommended tools

- procurement and vendor intake workflow
- security and compliance review checklist
- contract and SLA management process
- access and dependency monitoring tools

## Estimated time

- 1 to 2 days for small commercial tool evaluation
- 1 to 3 weeks for a meaningful external service or platform dependency

## Practical example

A startup evaluates a third-party notification service, reviews the security posture, confirms contract and support escalation expectations, validates the integration with a staging environment, and records the ongoing operational owner and exit procedure before production adoption.

## Internal references

- [security-review.md](security-review.md)
- [deployment.md](deployment.md)
- [api-design.md](api-design.md)
- [company/release-policy.md](../company/release-policy.md)
- [agents/DevOps.md](../agents/DevOps.md)
