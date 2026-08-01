# Release Automation

## Objective

Define the automation concept for `/release`, which should support the formal readiness decision for shipping a version, artifact, or product increment with evidence and operational accountability.

## Inputs

- release candidate identifier
- scope and summary of changes
- review evidence package
- deployment and rollback evidence
- release owner and communication path
- environment and production constraints

## Outputs

- release brief or readiness package
- go/no-go recommendation with evidence
- outstanding blockers or required remediation list
- release summary for support and communication

## Flow

1. Collect release artifact, change summary, and gate evidence.
2. Check for mandatory review and deployment readiness conditions.
3. Build the release approval package with blockers or approval evidence.
4. Generate a final release decision path for human approval.

## Possible automations

- compile review-ready release evidence from repo artifacts;
- map release blockers to specific missing reviews, test evidence, or operations inputs;
- produce notifications or release briefings for the responsible owners.

## Integration with Claude Code/OpenCode

- construct a release evidence package that is human-reviewable and traceable;
- preserve governance alignment across security, QA, deployment, and documentation.

## Integration with VS Code

- prepare the release summary from current workspace evidence;
- surface any missing review gate or deployment condition clearly;
- support final release sign-off in the editor workflow.

## Integration with GitHub

- attach the release package to a repository release, PR, or milestone;
- keep approval evidence and blockers visible to the responsible engineering and product owners.

## Integration with CI/CD

- require completion of mandatory review evidence before a release stage is approved;
- keep pipeline status consistent with the release decision record.

## Risks

- release decision based on incomplete evidence;
- missing escalation or communication path for production support;
- hidden release blockers discovered only after the artifact is already promoted.

## Checklist

- [ ] scope and candidate version are explicit
- [ ] required review evidence is present
- [ ] deployment and rollback evidence are present
- [ ] release owner and support path are named
- [ ] go/no-go decision is explicit and documented

## Roadmap of implementation

### Phase 1

- define release readiness package and evidence bundling.

### Phase 2

- add GitHub and CI release gate linking.

### Phase 3

- formalize release evidence dashboards and branch-to-release traceability.

## Definition of Done

The `/release` automation is complete when the repository can generate a clear, reviewable, evidence-driven release decision package that is usable by engineering, product, and operations owners.
