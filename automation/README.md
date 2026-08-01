# Automation

## Objective

Define the official architecture for future AI-assisted automation inside AI-STARTUP-KIT. This module is intentionally specification-first: it describes the command model, orchestration boundaries, repository integrations, and implementation roadmap for future automation workflows without executing any script or modifying runtime behavior.

## Operating principles

- automation should remove repetitive toil while preserving human accountability;
- every automation must be traceable to a review, release, or delivery gate;
- the command layer must remain compatible with Claude Code/OpenCode, VS Code, GitHub, and CI/CD;
- automation must never bypass governance, quality, security, or documentation expectations.

## Command model

Conceptual commands to be supported:

- `/new-project`
- `/new-feature`
- `/new-api`
- `/generate-tests`
- `/review-code`
- `/security-review`
- `/update-docs`
- `/deploy`
- `/sync-memory`
- `/build-roadmap`

## Automation architecture

The automation layer is organized into four layers:

1. Command interface layer
   - AI assistant command entry points in Claude Code/OpenCode or VS Code.
   - Human or agent invocation models.

2. Workflow orchestration layer
   - stateful flow definitions for bootstrap, feature delivery, testing, review, release, and memory synchronization.
   - deterministic prompts, selected templates, and structured outputs.

3. Integration layer
   - GitHub PR creation, issue awareness, workflow triggers, release notes, and repository evidence.
   - VS Code workspace actions and file generation patterns.
   - CI/CD acceptance gates and observability handoff.

4. Evidence and governance layer
   - artifacts, markdown reviews, checklists, test evidence, and release traceability.
   - all automations must result in reviewable artifacts rather than hidden side effects.

## Automation index

- [project-bootstrap.md](project-bootstrap.md): create a consistent project baseline.
- [new-project.md](new-project.md): initialize a new product or engineering workspace from the framework.
- [new-feature.md](new-feature.md): scaffold feature definition and delivery evidence.
- [new-api.md](new-api.md): design and document a contract-first API workstream.
- [new-component.md](new-component.md): generate reusable UI or shared component design artifacts.
- [new-database-model.md](new-database-model.md): define persistent model and migration planning inputs.
- [new-user-story.md](new-user-story.md): produce a user-story artifact aligned to delivery expectations.
- [generate-tests.md](generate-tests.md): produce test strategy and validation evidence streams.
- [generate-docs.md](generate-docs.md): produce or update project documentation from approved inputs.
- [review-code.md](review-code.md): drive a structured code review and evidence collection process.
- [security-scan.md](security-scan.md): orchestrate threat and exposure review preparation.
- [quality-gates.md](quality-gates.md): enforce release, test, security, and documentation readiness.
- [deployment.md](deployment.md): standardize deployment orchestration planning and execution readiness.
- [release.md](release.md): formalize go/no-go evidence for release decisions.
- [sync-memory.md](sync-memory.md): import or refresh project knowledge into memory structure.
- [health-check.md](health-check.md): validate process cadence, repository health, and automation readiness.

## Integration architecture

### Claude Code / OpenCode

- interpret command intent and map it to a governed workflow;
- use repository templates and playbooks as evidence-backed inputs;
- produce reviewable markdown or structured artifacts instead of opaque transformations.

### VS Code

- open the relevant workspace and file set;
- create or update the expected documents in the repository;
- provide inline summaries, checklist status, and task handoff context.

### GitHub

- create branches, PRs, Reviews, and issue-linked change records;
- attach evidence artifacts to the release pathway;
- support approval and merge gates via repository rules.

### CI/CD

- run validation processes on code, docs, security, test coverage, and release readiness;
- block merge or release when evidence or required reviews are incomplete;
- preserve a durable trace of the change through build, test, review, and deployment.

## Risks

- over-automation that weakens accountability;
- hidden command behavior without explicit evidence artifacts;
- command drift between human workflows and AI execution;
- repository state changes without review or release guards.

## Checklist

- [ ] each automation is traceable to a policy or playbook;
- [ ] each automation declares input and output evidence;
- [ ] each automation has explicit integration targets;
- [ ] each automation remains reviewable and reversible;
- [ ] each automation is safe to run in a collaborative repository context.

## Roadmap of implementation

### Phase 1

- document command semantics and workflow boundaries;
- enable repository-scoped file generation through templates;
- standardize quality gate handoff artifacts.

### Phase 2

- connect GitHub issue and PR workflows;
- add structured review and release evidence collection;
- implement CI/CD gate handoff to enforcement.

### Phase 3

- add memory synchronization and project health intelligence;
- enable standardized operational dashboards and release evidence summaries;
- formalize command packages as reusable automation protocols.

## Definition of Done for the automation module

The automation module is complete when all major command families are specified, each command includes the required workflow contract, and the system architecture clearly shows how these commands integrate with the repository, its review layer, and its delivery lifecycle.
