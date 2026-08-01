# Review Code Automation

## Objective

Define the automation concept for `/review-code`, which should structure a code review workflow around evidence, traceability, standards alignment, and clear approval or rejection decisions.

## Inputs

- code diff or review target
- commit or PR metadata
- acceptance criteria or implementation intent
- standards or architecture references
- quality, security, or release risk markers

## Outputs

- review summary with explicit findings
- approval, rejection, or requested-change outcome
- action items and remediation evidence
- traceability to the related PR or merge path

## Flow

1. Capture the review target and its intent.
2. Compare the implementation against standards, acceptance criteria, and risk constraints.
3. Generate a review evidence artifact with findings and decisions.
4. Attach required remediation or follow-up actions.
5. Close the loop as a review record that can move into merge or release.

## Possible automations

- produce a structured PR review checklist summary;
- identify missing tests, security concerns, or standards gaps;
- generate review comments or safe next-step prompts for the author.

## Integration with Claude Code/OpenCode

- enable review assistance through command-driven repository analysis;
- keep the review output evidence-based and traceable;
- preserve the review record as a markdown artifact or repository-linked note.

## Integration with VS Code

- surface findings in the editor context for code review workflow;
- keep a human-readable evidence trail and next-step checklist;
- propose remediation and re-review checkpoints.

## Integration with GitHub

- attach review findings to a PR or review discussion;
- maintain a path linking approvals to branch status and merge readiness;
- keep merge-blocking conditions visible and traceable.

## Integration with CI/CD

- gate merge or release on the presence of review evidence and remediation closure;
- enforce repository-specific quality barriers when review comments remain unresolved.

## Risks

- shallow review output that misses architecture or security concerns;
- reviewer automation that substitutes for evidence and ownership;
- weak handling of trade-offs where implementation is close but still not acceptable.

## Checklist

- [ ] review target and business intent are explicit
- [ ] applicable standards are referenced
- [ ] security and quality risks are assessed
- [ ] review outcome is explicit and owner-assigned
- [ ] remediation path is visible if approval is conditional

## Roadmap of implementation

### Phase 1

- define the review summary and evidence format.

### Phase 2

- add branch or PR-linked finding generation rules.

### Phase 3

- integrate review evidence with merge policy and CI gate enforcement.

## Definition of Done

The `/review-code` automation is complete when it produces a review record that is actionable, evidence-backed, and suitable for merge-readiness or release-readiness decision making.
