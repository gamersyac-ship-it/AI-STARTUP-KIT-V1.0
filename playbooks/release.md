# Release

## Objective

Define the official path for publishing and communicating a release with evidence, version discipline, and business clarity.

## When to use it

Use this playbook when moving a validated change into a production, customer-facing, or shared release train context.

## Responsible

- Product Manager: business impact and release message alignment
- CTO: release readiness and design validation
- DevOps: deployment and environment sequence
- QA: evidence for quality readiness
- Security: release risk and blocker review
- Documentation: release note and knowledge update

## Inputs

- approved version candidate
- deployment evidence
- release notes and support ownership

## Preconditions

- the change has passed QA and security checks
- the deployment path and rollback path are known
- the release owner is identified

## Steps

### 1. Define the release type

- determine whether the release is a patch, minor, or major release based on the scope and backward compatibility

Checklist:
- version classification is justified
- release type is consistent with the approved policy
- compatibility risks are named

### 2. Set the version and changelog

- apply semver rules and update release metadata
- document key changes, known limitations, and risk notes

Checklist:
- versioning is explicit and traceable
- release notes are concrete and readable
- breaking change warning is present where needed

### 3. Validate the release candidate

- confirm release evidence, health checks, and rollback path
- re-check support ownership and communication needs

Checklist:
- quality evidence supports the release
- rollback is still validated
- incident escalation path is known

### 4. Communicate the release

- inform all relevant stakeholders of scope, user impact, and expected support expectations

Checklist:
- messages are concise and concrete
- timing and owner are named
- known risks are visible

### 5. Close the release loop

- attach the release record to the delivery and support artifact
- document any post-release follow-up or monitoring needs

Checklist:
- release artifact is stored as traceable knowledge
- support team has the release summary
- any issue discovered after rollout is linked to the release artifact

## Common errors

- releasing without a clear version classification
- failing to communicate breaking changes or compatibility risk
- missing rollback awareness during final release approval
- leaving release notes too vague to guide support

## Risks

- customer confusion about important changes
- hidden compatibility impact
- failure due to weak deployment confidence or missing sandbox validation
- support burden from poor release communication

## Best practices

- hold release discipline through semver and evidence-based signoff
- release notes should be written for support and customer understanding
- keep the communication path brief, clear, and tied to ownership

## Deliverables

- source of truth release tag or version reference
- changelog and notes
- communication artifact
- release evidence summary

## Definition of Done

The release is complete when the version is tracked, evidence is attached, communication is sent to the correct owners, and release supportability remains explicit.

## KPIs

- release success rate
- rollback rate
- post-release incident frequency
- communication completeness rate

## Recommended tools

- semver-aware release management
- changelog generation or documentation update path
- communication toolchain and incident channel
- deployment evidence telemetry

## Estimated time

- 30 minutes to 2 hours for a standard release
- longer for major releases or cross-team communication

## Practical example

A minor release is tagged `1.4.0`, the changelog records the new endpoint and its user impact, and release owners send a concise note to support and stakeholders that includes limits, rollback awareness, and the expected monitoring path.

## Internal references

- [company/release-policy.md](../company/release-policy.md)
- [company/workflow.md](../company/workflow.md)
- [standards/api.md](../standards/api.md)
- [standards/documentation.md](../standards/documentation.md)
