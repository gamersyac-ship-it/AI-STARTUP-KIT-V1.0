# Deployment

## Objective

Define the operational deployment path for moving accepted changes into the target environment safely and with rollback awareness.

## When to use it

Use this playbook for any deployment of code, config, schema, or release artifacts that must move through a managed environment path.

## Responsible

- DevOps: deployment orchestration and control
- CTO: technical readiness risk and escalation
- QA: release confidence evidence
- Security: exposure and policy validation
- Documentation: operational knowledge and release note alignment

## Inputs

- tested release candidate
- release summary and rollback plan
- environment and change scope

## Preconditions

- the release candidate has passed relevant QA and security review
- rollout owner is named
- rollback path is defined before starting

## Steps

### 1. Pre-deploy validation

- confirm target environment, permissions, and version
- verify configuration, secrets, dependency state, and migration dependencies

Checklist:
- exact release artifact is clear
- target environment is authoritative and ready
- rollback or mitigation path exists

### 2. Deployment execution

- run the deployment in the approved sequence
- confirm logs, health, and critical service status

Checklist:
- deployment is traceable by release ID or version tag
- no unexpected drift or partial failure has occurred
- operators have the correct signal path for success or failure

### 3. Post-deploy validation

- confirm that the expected system behavior is present
- verify monitoring, logs, and customer or service impact

Checklist:
- smoke test passes
- error rate or service health remains within acceptable thresholds
- any failed verification step is labeled and escalated

### 4. Rollback decision and execution

- trigger rollback if the deployment creates unacceptable impact or quality failure
- revert using the approved, known-safe path

Checklist:
- rollback owner is identified
- rollback command or procedure is available
- communication paths are prepared

## Common errors

- deploying without a rollback plan
- mixing configuration and code changes without clear sequencing
- unclear ownership of health signal interpretation
- skipping post-deploy validation because the deploy command appeared successful

## Risks

- partial release failure
- migration drift or data inconsistency
- production outage due to state mismatch
- undetected regression after final traffic exposure

## Best practices

- treat deployment as a controlled operational process, not a quick command
- keep rollback and release truth separated but linked
- document performance and service health expectations before deployment
- use canary or staged rollout when risk is material

## Deliverables

- deployment artifact or version target
- deployment log or evidence
- post-deploy verification result
- rollback route and owner note

## Definition of Done

The deployment is complete when the change has been executed in the approved environment path, the system is confirmed healthy enough to continue, and rollback or mitigation evidence is available if quality or service thresholds are exceeded.

## KPIs

- successful deploy rate
- rollback frequency
- mean time to recover from failed deployment
- release health adherence after rollout

## Recommended tools

- CI/CD pipeline
- environment management and secrets policy
- health checks, metrics, and alerting
- release logging and deployment evidence system

## Estimated time

- 30 minutes to 2 hours for small pre-approved releases
- several hours for more complex or staged releases

## Practical example

A new API release is deployed to a staging environment with smoke validation, then to production using a staged rollout that can be paused or rolled back immediately if health checks or error rates exceed the approved threshold.

## Internal references

- [company/release-policy.md](../company/release-policy.md)
- [company/workflow.md](../company/workflow.md)
- [standards/security.md](../standards/security.md)
- [standards/testing.md](../standards/testing.md)
- [agents/DevOps.md](../agents/DevOps.md)
