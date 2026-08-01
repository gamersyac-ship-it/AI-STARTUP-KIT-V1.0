# Performance Optimization

## Objective

Define the operational process for improving performance across frontend, backend, database, and delivery boundaries without degrading maintainability or correctness.

## When to use it

Use this playbook when the product, API, service, or user flow shows latency, load, or bundle-related issues that materially affect experience or reliability.

## Responsible

- CTO or technical lead: architectural prioritization
- FullStack: implementation and measurement
- QA: evidence for functional stability under performance changes
- DevOps: environment and telemetry ownership
- Product Manager: business expectation and trade-off visibility

## Inputs

- observed performance issue
- metrics or evidence of impact
- relevant user, service, or endpoint context

## Preconditions

- the bottleneck is observed or measured
- the target user or system impact is known
- the performance threshold or expected behavior is explicit

## Steps

### 1. Measure and localize

- identify the actual layer where the issue arises: frontend, backend, database, network, or bundle delivery
- collect measurable evidence before optimizing

Checklist:
- bottleneck is identified rather than guessed
- evidence is tied to the impacted workflow
- performance threshold or target is named

### 2. Prioritize by business impact

- determine which bottlenecks most affect user experience, availability, or operational cost
- choose the smallest high-value optimization path first

Checklist:
- priority fits business urgency
- low-value optimization is not preferred over high-value user impact
- dependencies are visible

### 3. Change the right layer

- address frontend rendering, backend logic, database query patterns, caching, or bundle delivery based on the actual root cause

Checklist:
- optimization targets the observed hotspot
- architectural impact is understood
- trade-offs are explicit

### 4. Validate behavior and performance together

- ensure the performance change does not break functionality or contracts
- verify load, throughput, and responsiveness under realistic conditions

Checklist:
- the workflow remains correct after the optimization
- evidence for improved metrics exists
- no hidden quality drop occurred

### 5. Document and monitor

- capture improved baseline and any remaining cost or risk
- keep the performance profile visible to the recovery owner

Checklist:
- metrics are documented in the release or operational note
- the team knows how to validate the improvement again
- alerting or monitoring is not removed

## Common errors

- optimizing without measurement
- micro-optimizing a path that is not the true bottleneck
- moving performance work into the release without test evidence
- ignoring cache and query design until after production impact exists

## Risks

- performance improvement that reduces readability or maintainability too far
- infrastructure or cache change that creates consistency errors
- optimization path targeted at the wrong layer and not the true cause

## Best practices

- optimize from measured evidence, not guesswork
- prefer the architectural fix over cosmetic tuning when the bottleneck is structural
- keep performance budgets and thresholds explicit
- align optimization work with release and support expectations

## Deliverables

- measured bottleneck report
- optimization scope and target metric
- implementation evidence
- post-change performance validation note

## Definition of Done

The optimization is complete when the bottleneck is confirmed, an evidence-based fix is implemented, and the resulting system behavior is measured and documented for future support and release confidence.

## KPIs

- p95 latency
- page or endpoint load time
- query latency for critical paths
- regression rate after optimization change

## Recommended tools

- performance profile and tracing tools
- browser profiling or bundle analysis tools
- metrics dashboards
- database explain and inspection tools

## Estimated time

- 0.5 to 2 days for a small targeted optimization
- several days or weeks for architecture and scaling-focused work

## Practical example

A frontend screen is slow due to a large bundle and duplicated fetch chain. The team measures the actual rendering and request path, then applies lazy loading and request deduplication, validates that usability and content correctness remain intact, and documents the quantified improvement.

## Internal references

- [standards/performance.md](../standards/performance.md)
- [standards/api.md](../standards/api.md)
- [standards/database.md](../standards/database.md)
- [standards/react.md](../standards/react.md)
