# Incident Response

## Objective

Provide the official operating procedure for detecting, classifying, communicating, mitigating, and learning from incidents that threaten product, reliability, privacy, or service continuity.

## When to use it

Use this playbook for production or environment incidents that require coordination across engineering, support, and leadership.

## Responsible

- Incident commander: manage response flow
- DevOps: stabilization and environment action
- Security: security-impact assessment and control validation
- QA or support: customer impact and reproduction evidence
- CTO: escalation and technical coordination
- Product Manager: user and business impact communication

## Inputs

- alert, user report, or monitoring signal
- environment and affected service evidence
- ownership data and current release state

## Preconditions

- the incident is observed or reported
- severity is not yet fully established but the issue is active or urgent
- the responsible owner is identified enough to begin coordination

## Steps

### 1. Detect and classify severity

- confirm the incident signal and whether it is customer-visible, internal, or high risk
- classify severity using the incident management model and business impact

Checklist:
- severity is assigned quickly
- customer or service impact is estimated
- incident commander is named

### 2. Declare incident and assemble response

- open a communication channel or incident record
- assign direct owners for mitigation, communications, and evidence gathering

Checklist:
- ownership is explicit
- response scope is bounded
- decision-maker is clear

### 3. Stabilize the service or product

- isolate the fault, divert traffic, disable the harmful path, or revert the problematic change
- preserve evidence before any destructive remediation action

Checklist:
- mitigation aims to reduce impact immediately
- the service is moved to a known safe state where possible
- rollback or containment path is available and tracked

### 4. Communicate the incident

- provide a brief statement of what is known, impact, status, and recovery owner
- keep communications brief but share the business and technical risk level

Checklist:
- stakeholders are informed quickly
- status updates are periodic and transparent
- dependencies or blockers are visible

### 5. Contain and recover

- implement the approved mitigation or hotfix flow
- validate that the system or service has recovered as expected

Checklist:
- service health is measured after mitigation
- rollback or failover path is still available
- release or configuration drift is bounded

### 6. Postmortem and learning closure

- document the timeline, cause, impact, communication path, and corrective actions
- assign the permanent fix owning actions

Checklist:
- the postmortem is honest and evidence-driven
- action owners and dates are explicit
- preventive actions are identified, not just described

## Common errors

- waiting too long to classify severity
- allowing multiple parallel response streams without clear ownership
- escalating after the service is already failing without traceable actions
- treating this as a “just fix it” event without postmortem closure

## Risks

- slow decision-making in a high-pressure event
- incomplete communication to stakeholders and support owners
- second-order impact if the initial mitigation is too narrow
- permanent recurrence due to absent preventive action

## Best practices

- one owner for the incident flow
- one channel for communications and evidence
- keep mitigation decisions minimal and reversible where possible
- write the postmortem for the next team, not just for the current event

## Deliverables

- severity and incident ticket
- communication artifact
- mitigation evidence
- recovery proof
- postmortem and preventive action record

## Definition of Done

The incident response is done when service or product stability is restored, communication is explicit, evidence is preserved, and the preventive closure is captured for future resilience.

## KPIs

- mean time to detect
- mean time to recover
- number of high-severity incident escalations
- percent of incidents with postmortem and action closure

## Recommended tools

- alerting platform
- incident communication channel
- monitoring and tracing tools
- release evidence and rollback record

## Estimated time

- 30 minutes to 2 hours for contained incidents
- multiple hours or days for cross-team or severe customer business impact

## Practical example

A payment API raises latency failures and an alert is generated. The incident commander classifies the event as High severity, communicates the status to stakeholders, applies a rollback or mitigation route, validates health after the action, and closes the incident with a postmortem that documents the root cause and prevention action.

## Internal references

- [company/incident-management.md](../company/incident-management.md)
- [company/release-policy.md](../company/release-policy.md)
- [deployment.md](deployment.md)
- [hotfix.md](hotfix.md)
