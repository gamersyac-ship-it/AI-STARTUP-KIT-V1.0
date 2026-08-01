# New Feature Command Specification

## Objective

Specify the automation concept for `/new-feature`, which should generate a feature delivery package aligned to the framework’s quality, review, and release expectations.

## Inputs

- product or business objective
- target user or business benefit
- expected acceptance criteria
- dependencies and impacted modules
- risk or quality constraints
- related architecture or API context

## Outputs

- feature brief or implementation artifact
- linked acceptance criteria and risk notes
- review entry points for product, QA, security, architecture, and release
- traceable handoff to implementation, test, and governance workflows

## Flow

1. Accept a feature intent and write it into a neutral feature document.
2. Attach relevant business, UX, architecture, and compliance constraints.
3. Create or reference the review checkpoints required for this feature type.
4. Prepare implementation and QA evidence starting points.
5. Produce a feature package ready for human review and engineering execution.

## Possible automations

- generate a feature artifact from the feature template;
- attach required review checklists and release gates;
- enqueue the right review sequence based on the feature scope.

## Integration with Claude Code/OpenCode

- create a feature-ready artifact and keep it aligned to the playbook and template system;
- propose next-step prompts such as design, implementation, or code review;
- preserve acceptance criteria and evidence requirements across the lifecycle.

## Integration with VS Code

- create or update the feature document in the repo;
- open the linked implementation area and current review artifacts;
- show the automation plan inside the editor as a structured checklist.

## Integration with GitHub

- map the feature to an issue, milestone, or PR workflow;
- place the acceptance criteria in a traceable repository artifact;
- attach review and quality gate evidence to the change record.

## Integration with CI/CD

- require test and code review evidence before merge-ready status;
- block release when the feature lacks the mandatory review set.

## Risks

- generating a feature artifact that is not tied to real release and quality rules;
- missing cross-team ownership for review and release sign-off;
- allowing a feature to move without explicit acceptance criteria.

## Checklist

- [ ] business and user problem are explicit
- [ ] acceptance criteria are measurable
- [ ] review gate requirements are attached
- [ ] implementation dependencies are visible
- [ ] QA and release evidence path is documented

## Roadmap of implementation

### Phase 1

- create the feature package template and command output structure.

### Phase 2

- enforce review checklist linking and acceptance traceability.

### Phase 3

- integrate GitHub issue and CI evidence handoff.

## Definition of Done

The `/new-feature` automation is complete when its output produces a reviewable feature package with explicit acceptance criteria, required review gates, and enough delivery traceability to move into implementation safely.
