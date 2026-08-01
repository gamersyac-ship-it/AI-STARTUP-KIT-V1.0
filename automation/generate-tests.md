# Generate Tests Automation

## Objective

Define the automation concept for `/generate-tests`, whose purpose is to prepare test strategy, validation evidence, and regression coverage for a proposed change.

## Inputs

- feature, bug, API, or architecture context
- acceptance criteria or review criteria
- environment assumptions
- known risk areas
- existing test infrastructure or repository conventions

## Outputs

- test plan or strategy artifact
- suggested test cases and traceability notes
- QA evidence requirements
- regression-risk checklist for the change scope

## Flow

1. Read the intent and define the validation domain.
2. Produce a structured test plan based on the change type.
3. Identify happy-path, error-path, and edge conditions.
4. Mark the evidence and review requirements needed for approval.
5. Return the test package as a reviewable artifact.

## Possible automations

- generate unit, integration, API, UI, or regression test outline;
- propose expected evidence, test naming, and coverage anchors;
- create links to review and release gates for the change.

## Integration with Claude Code/OpenCode

- create a reviewable test specification without writing production code;
- connect the test plan to the feature, API, QA, and release workflows;
- keep the test strategy aligned to repository standards and quality policy.

## Integration with VS Code

- create or update the test plan file in the workspace;
- surface the required evidence markers in the editor for human review;
- guide the next implementation and execution steps.

## Integration with GitHub

- place the test strategy in the PR or issue evidence chain;
- connect test evidence to merge readiness and release gating.

## Integration with CI/CD

- suggest which test suites are mandatory for merge or deployment;
- block release when essential validation evidence is absent.

## Risks

- test strategy that looks complete but lacks real evidence or coverage;
- absent negative tests for important edge conditions;
- weak alignment between acceptance criteria and final verification evidence.

## Checklist

- [ ] change type and confidence area are identified
- [ ] happy-path, negative-path, and regression scenarios are listed
- [ ] environment, data, and ownership assumptions are documented
- [ ] review and release gates are linked
- [ ] evidence expected from execution is visible

## Roadmap of implementation

### Phase 1

- define the test design and evidence format.

### Phase 2

- support command-driven generation for specific change types.

### Phase 3

- integrate with GitHub and CI verification evidence pipelines.

## Definition of Done

The `/generate-tests` automation is complete when the generated test strategy can be used as a formal validation package for the associated change, including evidence, scope, and release readiness expectations.
