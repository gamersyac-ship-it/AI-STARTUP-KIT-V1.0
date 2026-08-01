# Playbooks

## Objective

This folder defines the official operating procedures for execution, review, release, and incident handling inside AI-STARTUP-KIT.

These playbooks are intended to be reusable, practical, and executable by engineering, product, QA, security, and operations roles.

## When to use this folder

Use this set whenever a team needs a repeatable sequence of decisions and actions for delivery, quality, release, or resilience.

## Operating model

The playbooks must be read alongside:

- [company/engineering-principles.md](../company/engineering-principles.md)
- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [standards/README.md](../standards/README.md)
- [agents/CTO.md](../agents/CTO.md)
- [agents/ProductManager.md](../agents/ProductManager.md)
- [agents/FullStack.md](../agents/FullStack.md)
- [agents/QASecurity.md](../agents/QASecurity.md)
- [agents/DevOps.md](../agents/DevOps.md)

## Playbook map

- [create-feature.md](create-feature.md): end-to-end creation of a new feature.
- [design-feature.md](design-feature.md): technical design and decision capture before implementation.
- [develop-feature.md](develop-feature.md): implementation workflow and delivery readiness.
- [review-code.md](review-code.md): code review process and approval criteria.
- [fix-bug.md](fix-bug.md): triage, diagnosis, remediation, validation, and prevention.
- [security-review.md](security-review.md): security review for new or changed systems.
- [qa-process.md](qa-process.md): test strategy across unit, integration, E2E, and quality gates.
- [api-design.md](api-design.md): contract-first API design and validation workflow.
- [database-design.md](database-design.md): schema design, migration, optimization, and integrity.
- [deployment.md](deployment.md): release deployment sequence and rollback safety.
- [release.md](release.md): semver and release communications.
- [hotfix.md](hotfix.md): emergency delivery workflow for urgent production changes.
- [incident-response.md](incident-response.md): detection, isolation, communication, mitigation, and postmortem.
- [infrastructure-migration.md](infrastructure-migration.md): controlled infrastructure migration and rollback path.
- [external-vendor-management.md](external-vendor-management.md): external provider selection, governance, and lifecycle control.
- [refactoring.md](refactoring.md): structured refactoring to reduce risk.
- [performance-optimization.md](performance-optimization.md): performance improvement workflow across the stack.
- [architecture-review.md](architecture-review.md): architecture evaluation and approval path.
- [project-kickoff.md](project-kickoff.md): startup sequence for new delivery initiatives.
- [sprint-planning.md](sprint-planning.md): agile planning and capacity discipline.
- [technical-debt.md](technical-debt.md): debt identification, prioritization, and recovery.
- [documentation-process.md](documentation-process.md): documentation lifecycle and maintenance discipline.

## Operating principles

- No work starts from vague intent.
- Every feature, bug, and deployment must have explicit evidence.
- No release enters production without QA, security, documentation, and owner validation.
- Every playbook must be traceable to a business need, technical decision, or operational risk.

## Definition of Done for the playbook set

The playbook set is complete when:

- the lifecycle from idea to release is documented,
- all major execution, review, and incident pathways are covered,
- and every document links back to the applicable governance and standards assets.
