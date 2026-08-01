# Hotfix

## Objective

Provide a rapid and controlled emergency path for urgent production corrections when customer impact, service failure, or data risk requires immediate action.

## When to use it

Use this playbook when a severe production issue requires fast mitigation, minimal release-risk, and explicit operational ownership.

## Responsible

- DevOps or incident owner: execution of the hotfix path
- CTO: design and architectural approval for the emergency fix
- Security: risk review if the issue affects access, secrets, or data exposure
- QA: targeted validation after the mitigation
- Product Manager: business impact awareness and release signoff

## Inputs

- production incident or bug evidence
- version and environment affected
- operational mitigation prior information

## Preconditions

- the impact is known and urgent
- a clear rollback path exists or is known
- the emergency owner is named

## Steps

### 1. Confirm severity and urgency

- classify the issue as critical or other high-impact event
- determine whether a full release process is blocked by time or customer risk

Checklist:
- urgency is real and documented
- service or customer impact has been measured
- emergency ownership is assigned

### 2. Contain and stabilize

- isolate impact, disable the failing path if necessary, or reduce user exposure
- preserve evidence while mitigating immediate damage

Checklist:
- the service is stabilized or degraded safely
- production risk is reduced quickly
- noisy or unsafe manual changes are avoided

### 3. Prepare the minimal corrective change

- define the narrowest safe patch to resolve the direct failure mode
- avoid unrelated work in the same release

Checklist:
- scope is truly emergency-bound
- the fix is matched to the root cause
- the change can be understood by a second reviewer quickly

### 4. Validate the hotfix path

- run focused validation against the failure condition
- verify that the mitigation is not creating a second defect

Checklist:
- the failing flow is now stable under a real test scenario
- regression risk is assessed and documented
- QA or operational verification evidence is attached

### 5. Push the hotfix under control

- deploy with explicit communication, owner, and rollback note
- align the emergency release with the normal release principles as far as the timeline allows

Checklist:
- version or deployment traceability is present
- the release communication is short and operationally clear
- rollback path is still known

### 6. Close the hotfix responsibly

- create or link to the follow-up backlog for the permanent solution
- document what happened, why it happened, and how it was prevented going forward

Checklist:
- permanent fix ownership is assigned
- RCA or incident follow-up is captured
- the hotfix is not treated as final system recovery alone

## Common errors

- treating a hotfix as a normal feature release without evidence
- bundling multiple unrelated changes into the emergency change
- skipping a focused validation path because the issue is urgent
- failing to capture the RCA and permanent mitigation

## Risks

- emergency change causing secondary regressions
- missing production telemetry for validation
- support confusion due to informal patch ownership

## Best practices

- make the emergency path as small and reviewable as possible
- document the fix as an exception to the usual process, not as an abandonment of process
- make the follow-up permanent remediation explicit and non-optional

## Deliverables

- incident or production evidence
- emergency mitigation statement
- hotfix changelog and deployment evidence
- RCA and permanent corrective action item

## Definition of Done

The hotfix is complete when the service or product behavior is stabilized, the emergency change is validated with evidence, supporting communication is recorded, and a permanent remedy path is captured.

## KPIs

- time to stabilize production
- rollback or re-open frequency
- time to full permanent remediation
- customer or business impact volume

## Recommended tools

- incident response channel
- deployment and rollback process
- monitoring and health signal tools
- release note or incident tracking artifact

## Estimated time

- 30 minutes to several hours for focused hotfix containment
- 1 to 2 days for post-fix closure and investigation follow-up

## Practical example

A payment flow outage is stabilized by disabling the problematic fallback path, applying a narrow patch to the failing branch, validating with a live regression path, and recording the incident for later root cause remediation.

## Internal references

- [incident-response.md](incident-response.md)
- [deployment.md](deployment.md)
- [fix-bug.md](fix-bug.md)
- [company/incident-management.md](../company/incident-management.md)
