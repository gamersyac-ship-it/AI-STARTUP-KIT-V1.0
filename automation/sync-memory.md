# Sync Memory Automation

## Objective

Define the conceptual automation for `/sync-memory`, which should synchronize the project or repository context into the shared memory layer so that future AI-assisted work remains context-aware and consistent.

## Inputs

- repository state or updated documentation set
- change summaries or release notes
- memory boundaries or target memory scope
- operational constraints and current project assumptions

## Outputs

- memory update package
- relevant knowledge summary for future work
- repository-level context refresh or consistency record

## Flow

1. Gather the current repository state and any recent change or delivery events.
2. Identify the memory scope to be refreshed.
3. Convert the current state into a reviewable, structured memory update.
4. Attach the memory update to the relevant project context and release or delivery state.
5. Return the memory sync summary for validation and follow-up.

## Possible automations

- refresh memory from project docs, reviews, and release notes;
- update project context, standards awareness, and operational constraints;
- capture cross-repo or cross-project learnings in a structured memory record.

## Integration with Claude Code/OpenCode

- bring the current repository truth into the memory layer for future commands;
- preserve a consistent record of important decisions, constraints, and lessons learned;
- keep operational memory connected to user intent rather than reliant on local-only context.

## Integration with VS Code

- update memory-related notes or project knowledge artifacts in the workspace;
- show the memory synchronization state in a readable summary;
- guide future commands with a versioned knowledge context.

## Integration with GitHub

- preserve memory refresh evidence in repository-linked notes or artifacts;
- support release or change traceability across sessions and contributors.

## Integration with CI/CD

- treat memory synchronization as an evidence-supporting layer rather than a deployment command;
- keep memory updates consistent with the repository’s documented operating state.

## Risks

- stale or inaccurate memory state that misguides future work;
- memory updates that are too broad and lose local project context;
- overtrust in memory without a corresponding review of the current repo state.

## Checklist

- [ ] current repository state is known
- [ ] memory scope is explicitly bounded
- [ ] notes and evidence are updateable and reviewable
- [ ] refresh output can be linked to the project or release state
- [ ] stale context is flagged or avoided

## Roadmap of implementation

### Phase 1

- define memory synchronization scope and artifact format.

### Phase 2

- connect repository knowledge and change history into the memory update workflow.

### Phase 3

- formalize memory refresh signals with GitHub and release state awareness.

## Definition of Done

The `/sync-memory` automation is complete when the memory layer can be refreshed from the repository’s current and reviewable state without introducing ambiguity or stale context into future automation workflows.
