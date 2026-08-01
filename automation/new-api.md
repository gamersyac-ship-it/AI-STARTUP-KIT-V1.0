# New API Command Specification

## Objective

Specify the automation concept for `/new-api`, which should create a contract-first API design workflow aligned to the framework’s API standards, security, QA, and release expectations.

## Inputs

- API purpose or business capability
- public or internal exposure model
- expected endpoints and resources
- authentication and authorization assumptions
- versioning or deprecation constraints
- error handling and compatibility expectations

## Outputs

- API design artifact
- endpoint contract summary
- security and compatibility notes
- validation and review path for QA and release

## Flow

1. Capture the API intent, compatibility constraints, and consumer context.
2. Generate the API contract template with endpoint, request, and response expectations.
3. Add security and governance requirements relevant to access, exposure, and rate control.
4. Attach the review and validation path required by the API type.
5. Publish the contract as a reviewable artifact before implementation.

## Possible automations

- generate endpoint and DTO skeleton documentation;
- create versioning, deprecation, and compatibility notes;
- identify required security gates such as review, rate limiting, auth, and auditability.

## Integration with Claude Code/OpenCode

- scaffold the API design package as a reviewable source artifact;
- keep the design aligned to the API and security standards;
- enable the next command path into implementation, testing, or review.

## Integration with VS Code

- create the API artifact in the workspace for human review;
- keep the file linked to implementation and release artifacts;
- support local editing of the contract prior to commit.

## Integration with GitHub

- raise the API design as a reviewable PR or design record;
- align endpoint changes with issue or milestone traceability;
- attach the API review evidence to the pull request.

## Integration with CI/CD

- verify that contract changes have a documented review path;
- block release if the API contract lacks safe versioning, security, or compatibility evidence.

## Risks

- contract drift between design and implementation;
- security or authorization assumptions being implicit;
- hidden breaking changes for client consumers.

## Checklist

- [ ] endpoint objective and exposure are explicit
- [ ] authentication and authorization path are named
- [ ] request and response contract are documented
- [ ] compatibility and versioning decisions are visible
- [ ] security and release review path is attached

## Roadmap of implementation

### Phase 1

- document contract-first workflow and artifact outputs.

### Phase 2

- add endpoint description and compatibility metadata generation.

### Phase 3

- add GitHub and CI evidence gating for API contract review.

## Definition of Done

The `/new-api` automation is complete when it produces a reviewable API contract package that is sufficiently explicit for safe design, implementation, testing, and release decision making.
