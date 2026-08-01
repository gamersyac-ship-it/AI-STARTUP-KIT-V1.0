# New Component Command Specification

## Objective

Specify the automation concept for `/new-component`, which should generate a reusable component specification aligned to UX, implementation, and review expectations.

## Inputs

- component name
- component purpose
- input and output contract
- target framework or platform assumptions
- design or UX constraints
- integration context with existing UI or shared design system

## Outputs

- component brief or specification
- input and output contract summary
- UX and implementation considerations
- review and quality entry points for implementation and acceptance

## Flow

1. Capture the component purpose, interface, and target usage context.
2. Generate the component artifact in a reusable and neutral format.
3. Add behavior, validation, and notes on interactions or dependencies.
4. Mark the review checkpoints for design, QA, and code quality.
5. Return the component package for review or implementation handoff.

## Possible automations

- create a component specification from a neutral template;
- infer required props, validation, and accessibility expectations;
- attach UX and testability requirements before implementation.

## Integration with Claude Code/OpenCode

- create a structured component artifact using repo templates and standards;
- prepare a reviewable component plan and next-step implementation prompts;
- preserve maintainability and shared design expectations.

## Integration with VS Code

- create the component-related document in the workspace;
- open the appropriate source and test directory locations;
- maintain a structured view of design and review notes.

## Integration with GitHub

- map the component work into reviewable issues or PRs;
- create a change record tying the component to scope, review, and release evidence.

## Integration with CI/CD

- enforce build and test readiness for the affected component;
- attach quality gate evidence prior to merge or deployment.

## Risks

- poor component contract clarity;
- inconsistent design reuse between teams;
- hidden accessibility or test gaps in the shared artifact.

## Checklist

- [ ] component purpose is clear
- [ ] inputs and outputs are explicit
- [ ] UX and accessibility considerations are listed
- [ ] implementation ownership is known
- [ ] test or review evidence path is defined

## Roadmap of implementation

### Phase 1

- create the component template and metadata model.

### Phase 2

- add validation and UX considerations by design context.

### Phase 3

- connect component review evidence to CI and GitHub release gates.

## Definition of Done

The `/new-component` automation is complete when it yields a reusable, reviewable component artifact that is well-scoped, testable, and aligned with the framework’s design and delivery expectations.
