# Release Policy

## Objective

The release policy defines how the organization ships changes safely, measurably, and transparently.

## Semantic Versioning

The framework uses Semantic Versioning (SemVer):

- `MAJOR`: breaking or incompatible changes
- `MINOR`: backwards-compatible new features
- `PATCH`: backwards-compatible fixes

Examples:

- `1.0.0` initial stable release
- `1.1.0` new feature or capability addition
- `1.1.1` defect fix or operational correction

## Release Types

### Patch Release

Use for critical bug fixes or low-risk corrective updates.

### Minor Release

Use for added functionality or product improvements that do not break current users.

### Major Release

Use when the change introduces breaking behavior, schema changes, or a materially different contract.

## Pre-Deployment Checklist

A release should only proceed when all of the following are true:

- QA confirms the behavior against acceptance criteria.
- Security confirms the release does not introduce unacceptable risk.
- DevOps confirms the deployment path and rollback plan.
- Documentation is updated and aligned with the release state.
- The release is traceable to a requirement, ADR, or approved change.
- Observability and rollback paths are understood by the owners of the release.

## Approval Criteria

The release must have:

- clear business or technical rationale,
- validated evidence of quality,
- secure defaults and no unresolved critical findings,
- environment readiness and release ownership,
- and communication of expected impact.

## Rollback Policy

Rollback must be planned before the release begins.

If a release fails or creates an unacceptable production impact, the team must:

1. determine the severity,
2. isolate the failed change,
3. revert or roll back using the approved path,
4. communicate the incident quickly,
5. and document the cause and corrective action.

## Communication of Changes

Every release should include:

- release summary,
- affected user or system area,
- known risks or limitations,
- rollback note,
- and the owner of operational support.

## Relationship to Other Documents

This policy is connected to:

- [workflow.md](workflow.md)
- [branching-strategy.md](branching-strategy.md)
- [incident-management.md](incident-management.md)
- [communication.md](communication.md)
