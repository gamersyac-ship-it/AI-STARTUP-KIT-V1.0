# Templates

## Objective

This folder provides reusable, implementation-agnostic templates for the principal artifacts created during the software lifecycle.

These templates are meant to support planning, execution, architecture, quality, release, and documentation work without tying the content to a specific product or project.

## Operating model

Templates must remain aligned to the company governance, standards, and playbook system:

- [company/engineering-principles.md](../company/engineering-principles.md)
- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [standards/README.md](../standards/README.md)
- [playbooks/README.md](../playbooks/README.md)

## Template index

- [epic.md](epic.md): portfolio or program level initiative description.
- [feature.md](feature.md): feature-level outcome and implementation frame.
- [user-story.md](user-story.md): user-centered requirement statement.
- [task.md](task.md): unit of execution for implementation or process work.
- [bug.md](bug.md): defect report and remediation path.
- [api.md](api.md): API contract and endpoint definition.
- [component.md](component.md): UI or shared component specification.
- [database-model.md](database-model.md): data contract and schema planning artifact.
- [architecture-decision-record.md](architecture-decision-record.md): structured decision and rationale record.
- [pull-request.md](pull-request.md): review-ready change summary and evidence artifact.
- [meeting-notes.md](meeting-notes.md): structured team meeting record.
- [sprint-planning.md](sprint-planning.md): sprint or delivery cycle commitment brief.
- [retrospective.md](retrospective.md): improvement and learning record for a delivery cycle.
- [deployment-plan.md](deployment-plan.md): release operation and rollback readiness plan.
- [test-case.md](test-case.md): execution-ready validation artifact.
- [risk.md](risk.md): risk tracking and mitigation statement.
- [change-request.md](change-request.md): controlled change authorization record.
- [research.md](research.md): exploration note for technical or product investigation.
- [proposal.md](proposal.md): decision and trade-off proposal for future action.

### Current repository status

The repository already contained a practical baseline set for the most common Lifecycle artifacts. The newly completed set above preserves that existing baseline and adds the remaining operationally useful templates needed for a complete reusable workbook.

## Template principles

- Templates must stay reusable, not product-specific.
- Each template should remain easy to fill by a human or an agent.
- Examples must use neutral language and avoid project-specific assumptions.
- Alignment with playbooks is mandatory where the artifact enters a review, release, or incident workflow.

## Definition of Done for the template set

The template set is complete when:

- all major lifecycle artifacts are represented,
- the required sections remain consistent across templates,
- and every template links to the right operating playbook and standards context.
