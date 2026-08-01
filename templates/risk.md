# Risk

## Objective

Capture a meaningful delivery, product, or operational risk with its likely impact and the mitigation or decision that should be taken.

## When to use it

Use this template whenever a risk may delay or damage a delivery objective, a security posture, a business outcome, or an operating capability.

## Responsible

- Product Manager or project owner: business and value exposure
- CTO or technical lead: architecture or engineering likelihood assessment
- Security or QA: risk and validation exposure assessment

## Required fields

- Risk title
- Description
- Likelihood
- Impact
- Owner
- Mitigation action
- Trigger or early-warning signal
- Status

## Optional fields

- Contingency plan
- Dependency or external factor
- Review date
- Residual risk note

## Complete example

```md
# Risk: Late Security Review on Access Boundary

## Objective

Document the delivery risk introduced by a security review dependency on a critical permission flow.

## When to use it

Use when a risk threatens release confidence, timing, or security assurance.

## Responsible

- Product Manager: owns business impact communication.
- CTO: validates architecture implications.
- Security: validates required mitigation or approval conditions.

## Required fields

- Risk title: Late Security Review on Access Boundary
- Description: access changes may require security review after implementation starts
- Likelihood: Medium
- Impact: High
- Owner: CTO
- Mitigation action: complete design review earlier and add explicit test evidence before final deploy
- Trigger or early-warning signal: design not approved before implementation milestone
- Status: Open
```

## Checklist

- [ ] the risk is tied to a real consequence and not just a concern
- [ ] owner and mitigation are explicit
- [ ] triggers or indicators are visible
- [ ] status is maintained during the delivery cycle

## Common errors

- storing risk in a vague note without actionable recovery
- leaving ownership or trigger conditions undefined
- letting risk remain open without any visible next step

## Best practices

- keep risks aligned to business and delivery impact
- store an action, not just a concern
- review risk state as part of the operational cadence

## Related playbooks

- [playbooks/security-review.md](../playbooks/security-review.md)
- [playbooks/sprint-planning.md](../playbooks/sprint-planning.md)
- [playbooks/incident-response.md](../playbooks/incident-response.md)
