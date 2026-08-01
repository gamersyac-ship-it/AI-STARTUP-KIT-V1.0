# Refactoring

## Objective

Provide a low-risk, evidence-based path for improving code structure without changing the intended behavior in unbounded ways.

## When to use it

Use this playbook when code no longer matches the desired architecture, becomes difficult to maintain, or shows repeated modification patterns that can be safely cleaned up.

## Responsible

- CTO or technical lead: architectural guardrails
- FullStack: implementation
- QA: regression validation
- Documentation: knowledge update where behavior remains stable

## Inputs

- existing code or service with known maintenance or readability issues
- change or defect history, where relevant
- desired target state or structural improvement goal

## Preconditions

- the refactor goal is known and bounded
- behavior must remain stable or the intended behavior change is clearly documented
- test or validation paths exist for the relevant behavior

## Steps

### 1. Identify the refactor target

- locate the code path with duplicated logic, unclear ownership, or repeated maintenance risk
- decide whether the change is purely structural or also touches behavior

Checklist:
- target is specific and reviewable
- non-goal cleanup is not mixed into the change
- the risk level is understood

### 2. Plan the change

- define small transformation steps and the evidence path
- specify what will remain unchanged and what will be improved

Checklist:
- plan is concrete and sequenced
- regression surfaces are identified
- the PR remains manageable and reviewable

### 3. Implement incrementally

- preserve behavior while changing structure
- avoid combining structural and feature changes in the same step unless the risk is controlled

Checklist:
- behavior is intentional and preserved
- changes stay isolated and understandable
- no hidden logic changes are introduced

### 4. Test the refactor

- validate with unit, integration, or E2E evidence relevant to the modified behavior
- confirm expected stability before broadening scope

Checklist:
- the same release confidence exists as before the refactor
- tests prove the preserved behavior
- the refactor does not become an unverified redesign

### 5. Document the result

- record what changed, why the change was needed, and what risk boundaries remained

Checklist:
- future maintainers have a clear explanation
- the new structure is easier to understand than the previous one
- docs remain aligned with actual code boundaries

## Common errors

- refactoring and feature changes at the same time without a safe separation
- rewriting too much without evidence of a bounded benefit
- changing names or structure without a reason grounded in maintainability
- removing tests or weakening regression coverage during the refactor

## Risks

- hidden behavior change behind façade-only structural changes
- extended review time and merge churn from large restructuring
- increased regressions if the refactor is not measured by real evidence

## Best practices

- keep the refactor small enough to reason about clearly
- refactor to improve domain boundaries or readability, not merely aesthetics
- freeze the behavior before changing structure whenever practical
- preserve test coverage through the change

## Deliverables

- refactor plan
- implementation and test evidence
- documentation or note of the targeted structural improvement
- review summary and final traceability

## Definition of Done

The refactor is complete when the structural improvement is explicit, the system behavior remains validated, and the code becomes easier to maintain without introducing hidden production risk.

## KPIs

- refactor regression rate
- code readability improvement measured via review signals
- time to complete a refactor safely
- percentage of refactors with preserved test evidence

## Recommended tools

- code review and pull request workflow
- automated tests and coverage reports
- linter or static analyzer
- architecture tracking or diagram artifact

## Estimated time

- 0.5 to 2 days for small refactors
- 1 to 2 weeks for larger domain cleanup

## Practical example

A service layer is extracted from a controller to remove duplication and reduce business-state coupling. In the process, behavior is preserved, tests are rerun, and the new boundary is documented for future maintainers.

## Internal references

- [standards/clean-architecture.md](../standards/clean-architecture.md)
- [standards/clean-code.md](../standards/clean-code.md)
- [standards/testing.md](../standards/testing.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
