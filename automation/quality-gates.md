# Quality Gates Automation

## Objective

Define the concept for `/quality-gates`, a command family that establishes delivery checkpoints across implementation, test, review, release, and documentation readiness.

## Inputs

- change type or lifecycle stage
- applicable governance references
- repository and environment state
- quality and release expectations
- owner or approval requirements

## Outputs

- checklist-driven gate summary
- required evidence list
- pass or fail recommendation for merge or release
- next action or blocker record

## Flow

1. Determine the stage and mandatory gate set for the change.
2. Map the relevant review, test, security, and deployment requirements.
3. Evaluate whether the evidence package is complete and reviewable.
4. Return a decision record with blockers or approval evidence.

## Possible automations

- produce gate-specific checklists from repository policies;
- map mandatory review sets by change type;
- infer required release readiness evidence before a deployment command is allowed.

## Integration with Claude Code/OpenCode

- use repository policy and review standards as the source of truth;
- transform the gate state into a reviewable command output;
- preserve evidence and follow-up actions in a standardized artifact.

## Integration with VS Code

- create or update a gate summary in the workspace;
- highlight missing or incomplete evidence items clearly;
- keep the gate context available to the development and release owners.

## Integration with GitHub

- attach gate status to the PR or release record;
- support required-review enforcement and mandatory evidence preservation.

## Integration with CI/CD

- connect gate readiness evaluation to repository pipelines;
- block deployment or merge when required evidence is incomplete.

## Risks

- gate definitions that are too generic and too weak to prevent low-quality releases;
- inconsistent enforcement between local workflows and CI/CD;
- evidence collected after the fact rather than before the gate.

## Checklist

- [ ] gate type is known
- [ ] mandatory review or evidence set is clear
- [ ] blockers are explicit and owner-named
- [ ] approval or rejection path is visible
- [ ] gate evidence is reusable in release records

## Roadmap of implementation

### Phase 1

- define gate models and policy mapping.

### Phase 2

- add repository-specific enforcement methods for mandatory review and release evidence.

### Phase 3

- connect gate summaries to GitHub and CI system outputs.

## Definition of Done

The `/quality-gates` automation is complete when its output can be used as a formal evidence-backed gate decision that aligns with the repository’s review, release, and governance expectations.
