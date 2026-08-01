# Deployment Automation

## Objective

Define the automation concept for `/deploy`, which should standardize deployment readiness, rollout strategy, release evidence, and rollback planning without executing a live deployment.

## Inputs

- target environment
- release artifact or version reference
- deployment strategy preference
- rollback criteria
- observability and support context
- review and quality gate evidence

## Outputs

- deployment plan artifact
- rollout rationale and sequence
- rollback and contingency guidance
- release-evidence checklist for execution and post-deploy validation

## Flow

1. Capture the target environment and release version.
2. Confirm that required review and quality evidence is attached.
3. Generate a deployment strategy and observable validation plan.
4. Record rollback conditions and responsible owners.
5. Produce a deployment-ready command package for review and execution.

## Possible automations

- generate a deployment plan from release and environment context;
- check that security, QA, and release expectations are satisfied;
- prepare rollback and post-deploy verification instructions.

## Integration with Claude Code/OpenCode

- produce a deployment design package that can be reviewed and approved before execution;
- maintain traceability to the release and quality gate artifacts;
- support safe deployment sequencing in a human-reviewable way.

## Integration with VS Code

- create or update the deployment plan inside the workspace;
- keep rollback and validation evidence visible to the team;
- assist with environment-specific notes and change record maintenance.

## Integration with GitHub

- attach deployment evidence to the release PR or issue chain;
- preserve change and verification traceability outside the local editor.

## Integration with CI/CD

- require deployment gate readiness before a pipeline stage is allowed to proceed;
- align deployment status with release and rollback evidence through the pipeline.

## Risks

- deployment planning without operational rollback details;
- environment drift between staging and production assumptions;
- release evidence collected only after the deployment event.

## Checklist

- [ ] release candidate and environment are explicit
- [ ] rollback path is identified
- [ ] observability and post-deploy validation are defined
- [ ] required review evidence is attached
- [ ] owner and communication plan are defined

## Roadmap of implementation

### Phase 1

- define deployment plan and evidence output structure.

### Phase 2

- add environment-aware rollout and rollback decision rules.

### Phase 3

- integrate the deployment package with CI/CD and release governance.

## Definition of Done

The `/deploy` automation is complete when it produces an operationally reviewable deployment plan with evidence, rollback criteria, and release gate alignment.
