# Tech Stack

## Default Technology Philosophy

The framework is intentionally technology-agnostic at the repo level. It must remain reusable across different product and startup contexts.

## Recommended Baseline

### Frontend

- React or equivalent modern framework
- TypeScript by default
- Component-driven architecture
- Accessibility-first UI design

### Backend

- Node.js or equivalent service runtime
- TypeScript for API and service consistency
- Domain-oriented API structure
- Structured logging and request tracing

### Data

- Relational database for transactional systems by default
- Schema migration management
- Explicit data ownership and indexing strategy

### DevOps

- CI/CD pipelines
- Environment separation
- Observability and release gates
- Infrastructure as code when appropriate

## Decision Rule

Choose the simplest stack that satisfies the required product, security, operability, and maintainability goals.
