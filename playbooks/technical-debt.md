# Technical Debt

## Objective

Define a repeatable method for identifying, prioritizing, and recovering technical debt without allowing it to silently become a delivery tax.

## When to use it

Use this playbook when the team notices repeated maintenance pain, unstable quality, slow delivery, or architectural drift that comes from past shortcuts or missing design discipline.

## Responsible

- CTO: architectural prioritization and trade-off review
- Engineering Manager or lead: capacity and sequencing
- Product Manager: business priority awareness
- QA and Security: risk and regression visibility

## Inputs

- known system problems or repeated incidents
- delivery and maintenance pain evidence
- current roadmap and strategic priorities

## Preconditions

- the debt is visible in either the architecture, quality, delivery process, or product reliability
- the ownership of the affected area is known
- the team is willing to acknowledge the trade-off that created the debt

## Steps

### 1. Identify technical debt

- gather repeated symptoms: slow review cycles, fragile tests, difficult changes, regressions, compatibility pain, or high-risk code patterns
- classify the debt as design, process, testing, dependency, or operational debt

Checklist:
- debt is made explicit and observable
- root driver is not just a symptom
- the area of impact is named

### 2. Evaluate impact and urgency

- decide whether the debt blocks delivery, reduces reliability, degrades customer experience, or threatens maintainability

Checklist:
- impact is measured or qualitatively stated with evidence
- business or technical cost is visible
- the risk is specific enough to prioritize

### 3. Prioritize recovery action

- place debt recovery into the roadmap according to risk and value, not just inconvenience
- decide whether to pay off the debt in a sprint, in a focused refactor, or through a larger initiative

Checklist:
- recovery is tied to a concrete strategic or delivery goal
- ownership is assigned
- sequencing is realistic

### 4. Recover the debt with controlled scope

- implement recovery in a bounded, testable way
- avoid conflating debt recovery with unrelated feature work unless the relationship is explicit

Checklist:
- the recovery path is reviewable and small enough for confidence
- regressions are covered by evidence
- the debt is truly reduced, not hidden

### 5. Prevent recurrence

- add process, quality, or governance measures that reduce the likelihood of the same debt being created again

Checklist:
- authoring safeguards are explicit
- the team knows the operational and design rule that failed
- preventive action is assigned and not left as a general intention

## Common errors

- treating all debt as equal, regardless of impact on product or release risk
- only documenting debt without allocating a recovery owner
- burying recovery inside large feature work and then calling it “cleanup”
- failing to define the actual savings or benefit of the recovery

## Risks

- recovery work consumes capacity that could have gone into business value
- debt is hidden again by future pressure or poor planning
- reducing one type of debt may generate a second, unrelated form of debt

## Best practices

- balance debt recovery with current feature delivery through deliberate prioritization
- pay off debt when it is a direct cost multiplier on delivery, reliability, or supportability
- make the hard trade-off visible to Product and leadership, not implicit

## Deliverables

- technical debt register or issue list
- prioritization and action ownership
- recovery implementation evidence
- prevention plan for recurrence

## Definition of Done

The technical debt process is complete when debt has been identified, prioritized, recovered in a controlled and measurable route, and the prevention path is strengthened enough to avoid the same condition from returning silently.

## KPIs

- debt closure rate
- delivery friction from debt-related rework
- increase in defect recurrence from debt areas
- recurrence rate of avoidable debt patterns

## Recommended tools

- backlog and debt registry
- architecture review notes
- test and incident evidence
- release or support metrics

## Estimated time

- 0.5 to 2 days for small debt identification and remediation
- 1 to 3 weeks for broader debt recovery programs

## Practical example

The team consistently has to rework a module because a boundary was not properly separated. That debt is recorded, prioritized against a current reliability problem, then addressed through a targeted refactor with test evidence and a permanent rule about future boundary separation.

## Internal references

- [company/workflow.md](../company/workflow.md)
- [standards/clean-architecture.md](../standards/clean-architecture.md)
- [standards/testing.md](../standards/testing.md)
- [company/engineering-principles.md](../company/engineering-principles.md)
