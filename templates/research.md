# Research

## Objective

Document an exploratory investigation into a problem, technology, integration pattern, or product hypothesis before a formal decision is made.

## When to use it

Use this template when a team needs to understand a technical or product option, compare approaches, or confirm whether a proposed direction is viable.

## Responsible

- Product Manager or analyst: business and user problem framing
- CTO or technical lead: technical investigation ownership
- Engineering Manager: sequencing and effort trade-offs

## Required fields

- Research topic
- Question or hypothesis
- Context
- Sources or inputs reviewed
- Findings
- Recommendation
- Decision status
- Owner

## Optional fields

- Risks or unknowns
- Alternatives considered
- Cost or effort estimate
- Next steps

## Complete example

```md
# Research: Access Policy Model for Multi-Workspace Collaboration

## Objective

Evaluate whether a role-based access model can satisfy the collaboration requirement without unnecessary complexity.

## When to use it

Use when a team needs to choose between multiple implementation paths before formal design acceptance.

## Responsible

- Product Manager: defines user need and business constraint.
- CTO: owns the comparative technical assessment.
- Engineering Manager: evaluates implementation realism.

## Required fields

- Research topic: Access Policy Model for Multi-Workspace Collaboration
- Question or hypothesis: a policy-based role assignment can preserve security and reduce custom logic.
- Context: the upcoming workspace collaboration feature requires role flexibility and auditability.
- Sources or inputs reviewed: current role registry, domain rules, security posture, and implementation constraints.
- Findings: a policy-based model reduces duplication but introduces stronger dependency management.
- Recommendation: proceed with a policy-aware role model with a constrained number of explicit role definitions.
- Decision status: proposed
- Owner: CTO
```

## Checklist

- [ ] the question or hypothesis is explicit
- [ ] findings reflect evidence and not assumptions
- [ ] recommendation can be used for a design or decision step
- [ ] ownership is named

## Common errors

- making research look like a solution proposal without evidence
- skipping known alternatives or constraints
- leaving the recommendation without a clear next action

## Best practices

- keep research grounded in actual data, implementation constraints, and observed dependency risk
- separate findings from recommendations
- link the research to the eventual design or ADR if the decision is accepted

## Related playbooks

- [playbooks/design-feature.md](../playbooks/design-feature.md)
- [playbooks/architecture-review.md](../playbooks/architecture-review.md)
- [playbooks/project-kickoff.md](../playbooks/project-kickoff.md)
