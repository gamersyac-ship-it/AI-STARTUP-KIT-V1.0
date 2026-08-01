# Security Scan Automation

## Objective

Define the automation concept for `/security-review`, whose purpose is to assess change exposure, trust boundaries, permissions, secrets handling, and release risk before a change moves toward merge or deployment.

## Inputs

- repository or diff scope
- authentication and authorization model
- data sensitivity assumptions
- exposure and dependency context
- release environment and access boundaries

## Outputs

- security review summary
- exposure and trust boundary findings
- blocker or remediation list
- release-risk visibility and evidence package

## Flow

1. Identify the feature or change surface and its trust boundaries.
2. Evaluate security-critical paths such as auth, secrets, logging, input handling, output exposure, and dependencies.
3. Produce a formal risk review narrative with findings and severity.
4. Return the security evidence and go/no-go recommendation for release or merge.

## Possible automations

- produce a security checklist summary tied to the review artifacts;
- identify likely secrets, permissions, transport, and output exposure flags;
- prepare a security evidence package for release approval.

## Integration with Claude Code/OpenCode

- create a review-ready security evidence artifact;
- connect the output to the repository’s security and release governance;
- keep the argument anchored in observable evidence instead of broad assumptions.

## Integration with VS Code

- surface the findings and checklist in the workspace prior to release;
- maintain a visible review note for the security owner and engineering team;
- help the author resolve blockers quickly with a structured remediation path.

## Integration with GitHub

- map security review evidence to PR, issue, and release context;
- attach required blockers or remediation notes into the repository record.

## Integration with CI/CD

- require threat or exposure evidence for sensitive changes;
- block release or merge when the security review is incomplete or unresolved.

## Risks

- incomplete trust-boundary review;
- hidden exposure caused by low-visibility configuration or logging;
- policy or security findings discovered only after release.

## Checklist

- [ ] trust boundaries are identified
- [ ] authorization and secrecy controls are explicit
- [ ] exposure, logging, and output safety are evaluated
- [ ] release or merge blockers are named
- [ ] evidence is preserved for follow-up and approval

## Roadmap of implementation

### Phase 1

- define security review evidence and severity output format.

### Phase 2

- link the command to repository exposure review and checklist context.

### Phase 3

- integrate with the repository’s release gate and GitHub security workflow.

## Definition of Done

The `/security-review` automation is complete when it produces a clear, owner-identified security evidence record that can support go/no-go decision making with concrete blockers or remediation needs.
