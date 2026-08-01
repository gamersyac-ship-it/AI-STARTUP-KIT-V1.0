# Generate Docs Automation

## Objective

Define the automation concept for `/update-docs`, which should maintain or generate documentation that stays aligned with the framework’s governance, playbook, template, and release expectations.

## Inputs

- target document or section set
- repository state and current documentation context
- required governance or standards references
- release, feature, or architecture status to reflect
- audience such as engineering, operations, or support

## Outputs

- updated or generated documentation artifact
- linked references to standards, playbooks, company rules, and review evidence
- a traceable documentation update summary for the associated change

## Flow

1. Determine the document or artifact that requires update.
2. Gather the current repository state and relevant references.
3. Generate or revise the documentation in a standards-aligned structure.
4. Link the documentation to required reviews, release notes, or playbooks.
5. Return the documentation for approval and release readiness review.

## Possible automations

- update README files and repository index content;
- generate or refresh feature, API, deployment, or architecture documentation;
- keep documentation aligned with current code, release gates, and review artifacts.

## Integration with Claude Code/OpenCode

- produce structured documentation artifacts that remain human-reviewable;
- preserve the framework’s governance and cross-linking patterns;
- support both project-level and repository-level documentation updates.

## Integration with VS Code

- create or edit docs directly in the workspace;
- use repository templates for consistent formatting and structure;
- provide a readable summary when documentation changes are completed.

## Integration with GitHub

- attach documentation updates to PR or issue evidence;
- preserve release note or change-note traceability;
- link docs changes to related commits or artifacts.

## Integration with CI/CD

- treat documentation completeness as a release gate where relevant;
- block release when essential docs are outdated or missing.

## Risks

- documenting the wrong state of the repository;
- stale docs that drift from implementation or operational reality;
- documentation changes without applicable review or owner recognition.

## Checklist

- [ ] the document target is explicit
- [ ] repository state and current references are identified
- [ ] the generated content matches the current operating model
- [ ] links to standards, playbooks, or reviews are valid
- [ ] release impact of the documentation update is known

## Roadmap of implementation

### Phase 1

- define standard documentation generation and update flows.

### Phase 2

- connect document updates to review and release evidence.

### Phase 3

- support large-scale repository documentation health checks and summaries.

## Definition of Done

The `/update-docs` automation is complete when the documentation artifact is current, aligned with the repository state, and reviewable as part of the same delivery evidence path as the associated change.
