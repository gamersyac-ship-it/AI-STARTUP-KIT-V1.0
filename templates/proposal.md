# Proposal

## Objective

Present a structured recommendation for a future product, technical, or delivery decision, including the trade-offs, expected outcome, and the context that justifies action.

## When to use it

Use this template when the team needs a concrete recommendation for a future step, investment, change, or strategic direction that requires review before execution.

## Responsible

- Product Manager: problem framing, customer or business impact
- CTO or technical lead: technical feasibility and architectural fit
- Engineering Manager: sequencing and implementation realism
- QA and Security: validation and operational risk implications

## Required fields

- Proposal title
- Problem statement
- Context or constraints
- Options considered
- Recommended path
- Benefits
- Risks and mitigations
- Decision owner
- Next-step timing

## Optional fields

- Cost range or effort estimate
- Dependencies
- Exit criteria
- Review checkpoints

## Complete example

```md
# Proposal: Standardize Access Policy Review Gate

## Objective

Recommend a standard access policy review gate that reduces late-stage security friction and supports safer release workflows.

## When to use it

Use whenever the organization needs a repeatable governance decision for a cross-cutting delivery concern.

## Responsible

- Product Manager: aligns the business need and delivery expectation.
- CTO: owns technical architecture and governance fit.
- Engineering Manager: determines practical adoption timing.

## Required fields

- Proposal title: Standardize Access Policy Review Gate
- Problem statement: the team currently discovers authorization risks late in the cycle.
- Context or constraints: multiple features require permission changes, and release confidence is sensitive to late-stage review.
- Options considered: ad hoc review path, mandatory design-phase gate, release-only review
- Recommended path: mandatory design-phase gate with explicit approval evidence
- Benefits: fewer release surprises, faster remediation, better traceability
- Risks and mitigations: may slow initial implementation without a clear owner; mitigate by making the gate lightweight and time-boxed
- Decision owner: CTO
- Next-step timing: next sprint planning
```

## Checklist

- [ ] the proposal is action-oriented and decision-ready
- [ ] trade-offs are visible and compare real alternatives
- [ ] decision ownership is explicit
- [ ] expected next steps and timing are documented

## Common errors

- writing a proposal as a narrative without a recommendation
- omitting the trade-offs that justify choosing one path
- leaving timing or decision ownership ambiguous

## Best practices

- keep proposals short, evidence-based, and easy to review
- express benefits and risk in business and technical terms
- keep the recommendation tied to a concrete operational path

## Related playbooks

- [playbooks/design-feature.md](../playbooks/design-feature.md)
- [playbooks/security-review.md](../playbooks/security-review.md)
- [playbooks/sprint-planning.md](../playbooks/sprint-planning.md)
