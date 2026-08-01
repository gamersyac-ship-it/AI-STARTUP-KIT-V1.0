# New Project Command Specification

## Objective

Specify the conceptual automation behind `/new-project`, whose purpose is to initialize an enterprise-style software project using the AI-STARTUP-KIT repository model.

## Inputs

- project name
- short business description
- delivery domain or customer segment
- ownership roles
- preferred architecture type
- repository destination
- release strategy expectations

## Outputs

- new project baseline
- startup governance and delivery documents
- initial repository structure and naming plan
- initial roadmap and review expectations

## Flow

1. Capture business context and constraints.
2. Generate the standard repository structure.
3. Insert the baseline operating docs referencing governance, standards, playbooks, templates, and reviews.
4. Mark the project as ready for a feature backlog or product roadmap.
5. Return a human-review summary with approval gates.

## Possible automations

- template-based skeleton generation;
- role assignment from the standard agent roster;
- initial architecture and delivery profile definition;
- policy document linking and cross-reference creation.

## Integration with Claude Code/OpenCode

- interpret the command as a repository creation workflow;
- produce structured markdown artifacts and decision logs;
- preserve the operating manual chain as the source of truth.

## Integration with VS Code

- scaffold the repository file set in the workspace;
- create relevant metadata and initial docs for review;
- suggest next commands such as `/new-feature` or `/build-roadmap`.

## Integration with GitHub

- create a baseline issue or milestone for repository setup;
- align with branch strategy and protected default branches;
- attach the project bootstrap plan to the first PR or repository setup record.

## Integration with CI/CD

- set default quality gate expectations for the new repository;
- define repository health and documentation completeness as the first pass of pipeline validation.

## Risks

- project defaults becoming too rigid for the actual product domain;
- missing early ownership and branch discipline;
- over-automation that skips real design review.

## Checklist

- [ ] name and mission are explicit
- [ ] target operating model is chosen
- [ ] governance, playbooks, and reviews are referenced
- [ ] repository structure is generated consistently
- [ ] approval or review owner is assigned

## Roadmap of implementation

### Phase 1

- implement repository skeleton generation.

### Phase 2

- add default team, workflow, and review onboarding guidelines.

### Phase 3

- connect GitHub and CI for startup readiness traceability.

## Definition of Done

The `/new-project` automation is complete when the created repository can be used as a legitimate, reviewable starting point for delivery within the AI-STARTUP-KIT operating model.
