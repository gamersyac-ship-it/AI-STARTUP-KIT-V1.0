# Change Request

## Objective

Formalize a request to alter scope, behavior, architecture, or operational expectations after work has already begun or after a decision has been made.

## When to use it

Use this template when a change of scope, requirements, contract, environment, or release path needs approval and traceability.

## Responsible

- Product Manager: business or customer impact owner
- CTO: architectural or technical approval owner
- Engineering Manager: delivery sequencing and capacity impact
- QA and Security: impact validation and approval support

## Required fields

- Change request title
- Description of the requested change
- Reason for the change
- Impacted area
- Requested by
- Approval owner
- Business or technical impact
- Release or timeline impact
- Status

## Optional fields

- Rollback implications
- Dependencies triggered by the request
- Cost or complexity note
- Communication needs

## Complete example

```md
# Change Request: Expand Role Validation Scope

## Objective

Request a change in validation scope to cover a broader access rule for shared workspace invites.

## When to use it

Use when an approved feature requires a contract-level change that affects implementation or test scope.

## Responsible

- Product Manager: behalf of the business owner.
- CTO: approves the technical impact and design path.
- Engineering Manager: determines sprint or sequencing impact.

## Required fields

- Change request title: Expand Role Validation Scope
- Description of the requested change: include support for additional role types in the validation path.
- Reason for the change: new access policy requires a wider role range for a supported deployment path.
- Impacted area: workspace invite API and permission registry
- Requested by: Product Manager
- Approval owner: CTO
- Business or technical impact: moderate implementation and QA change
- Release or timeline impact: shift by one sprint day
- Status: Pending review
```

## Checklist

- [ ] the requested change is traceable and not an informal preference
- [ ] affected area and owner are explicit
- [ ] the impact on schedule or release is visible
- [ ] approval path is known

## Common errors

- allowing informal scope changes without a traceable record
- bypassing approval path because the change appears small
- leaving release impact or dependency visibility implicit

## Best practices

- require explicit owner approval for material scope changes
- document the reason, not just the desired outcome
- preserve the change request with the delivery or release artifact

## Related playbooks

- [playbooks/create-feature.md](../playbooks/create-feature.md)
- [playbooks/design-feature.md](../playbooks/design-feature.md)
- [playbooks/release.md](../playbooks/release.md)
