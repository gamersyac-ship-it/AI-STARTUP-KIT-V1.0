# New Database Model Command Specification

## Objective

Specify the framework-level automation concept for `/new-database-model`, focused on producing a persistent model design package that can be reviewed safely and deployed through a governed release process.

## Inputs

- entity or data domain name
- relation and ownership assumptions
- expected queries or retrieval patterns
- migration or schema strategy
- data sensitivity and retention constraints
- release environment or deployment timing

## Outputs

- database model artifact
- migration and integrity considerations
- performance and access constraints summary
- review and release gates for schema safety

## Flow

1. Capture the data-domain problem and the expected persistence requirements.
2. Generate the model artifact with entities, relationships, constraints, and ownership.
3. Assess migration and rollback implications.
4. Add review and release checkpoints for integrity, security, and performance.
5. Deliver the artifact as a reviewable design package.

## Possible automations

- generate schema and migration brief from a neutral template;
- produce relationship and query planning notes;
- identify required integrity, performance, and rollback checks.

## Integration with Claude Code/OpenCode

- create a model specification that is reviewable and versionable;
- link the artifact to the database design, release, and security playbooks;
- establish a path to migration implementation and QA validation.

## Integration with VS Code

- scaffold the database design document and migration notes in the workspace;
- allow cross-linking with schema and deployment artifacts;
- keep review and remediation work in one repository-readable pathway.

## Integration with GitHub

- trace the data model change via issue, PR, or migration work record;
- store migration evidence and approvals with the release artifact.

## Integration with CI/CD

- gate migration rollout on schema verification, rollback readiness, and quality evidence;
- block release if data integrity or rollback planning is incomplete.

## Risks

- schema changes that break consumer compatibility;
- migrations without explicit rollback or ownership;
- performance and data-integrity issues discovered only after production rollout.

## Checklist

- [ ] data domain and purpose are explicit
- [ ] relationships and constraints are mapped
- [ ] migration sequence is described
- [ ] rollback or rescue path is present
- [ ] review and release path is attached

## Roadmap of implementation

### Phase 1

- create the database model artifact template.

### Phase 2

- add migration, integrity, and rollback metadata generation.

### Phase 3

- connect schema review evidence into GitHub and CI/CD release workflows.

## Definition of Done

The `/new-database-model` automation is complete when it creates a reviewable data design package that can be implemented, tested, deployed, and governed without relying on undocumented persistence assumptions.
