# Branching Strategy

## Goal

The branch strategy must support disciplined delivery, clean integration, safe release practices, and maintainable history.

## Branch Model

### `main`

Use `main` for production-ready, stable, fully validated code.

Rules:

- only merge after review and release approval,
- should represent the latest accepted production baseline,
- release tags should be associated with this branch.

### `develop`

Use `develop` as the integration branch for current delivery work.

Rules:

- receives merged feature work after validation,
- is the branch where the next release is assembled,
- should remain in a releasable state.

### `feature/*`

Use `feature/*` for new business or product capability work.

Naming example:

- `feature/user-session-improvements`
- `feature/api-rate-limits`

### `hotfix/*`

Use `hotfix/*` for urgent production corrections that require immediate action.

Naming example:

- `hotfix/security-token-validation`

### `release/*`

Use `release/*` when preparing a version for candidate validation and final release stabilization.

Naming example:

- `release/1.4.0`

## Naming Convention

Branch names should be:

- descriptive,
- lowercase,
- hyphen-separated,
- tied to the business or technical intent.

Avoid vague names such as `fix-1` or `update-work`.

## Merge Strategy

- Prefer pull requests or merge requests with review.
- Require at least one qualified reviewer.
- Do not merge to `main` without passing release gates.
- Keep individual branches short-lived and focused.
- Merge only after validation against the relevant quality and security checks.

## Versioning and Release Alignment

The repository should align branch use with semantic versioning:

- `major` for breaking changes,
- `minor` for backward-compatible new features,
- `patch` for backwards-compatible fixes.

This branch model must remain compatible with the release policy documented in [release-policy.md](release-policy.md).

## Relationship to Other Documents

This strategy supports the execution rules established in [workflow.md](workflow.md) and the delivery confidence required in [release-policy.md](release-policy.md).
