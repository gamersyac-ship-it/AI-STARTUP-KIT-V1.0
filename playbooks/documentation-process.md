# Documentation Process

## Objective

Create and maintain the documentation that supports execution, quality, support, and future maintenance without relying on tribal knowledge.

## When to use it

Use this playbook whenever a feature, bug fix, architecture decision, API shape, deployment, or release needs to remain understandable and supportable over time.

## Responsible

- Documentation owner or designated maintainer: documentation upkeep and quality
- Product Manager: user or product-facing narrative alignment
- CTO: architecture and design record consistency
- DevOps: operational runbooks and deployment knowledge
- QA and Security: evidence and risk summary update

## Inputs

- implementation or release artifact
- supporting design or operational decision
- user-facing or support-facing change notes

## Preconditions

- the change has a clear owner
- the final state is known with enough certainty to document
- the expected consumer of the documentation is known

## Steps

### 1. Decide whether the change requires documentation

- determine whether the work affects architecture, API behavior, release communication, support paths, or user operation

Checklist:
- the documentation need is linked to a real delivery or support need
- the owner is clear
- the consumer of the artifact is named if possible

### 2. Update the right document

- write to the correct reference location rather than duplicating the same knowledge across unrelated files
- connect new decisions to the existing system documentation

Checklist:
- the doc location is the right place for the information
- references are maintained instead of becoming stale copies
- the artifact is connected to the release or technical decision context

### 3. Keep the content evidence-based

- base the documentation on final behavior, not just the intent of the last planning conversation

Checklist:
- examples are representative of actual behavior
- known limitations and risks are not hidden
- support and operations can follow the workflow without guesswork

### 4. Review the documentation

- verify that the content remains consistent with the code, API, environment assumptions, and release state

Checklist:
- documentation can be read by a new contributor without missing context
- changes in contracts or behavior are reflected in the associated docs
- owners are not overreliant on personal memory

### 5. Maintain the lifecycle

- ensure that documentation is updated whenever the system meaningfully changes

Checklist:
- update timing is explicit
- release or sprint closure does not bypass documentation maintenance
- outdated docs are corrected rather than preserved as a false source of truth

## Common errors

- documenting only when a release is already done
- duplicating content across multiple places without a primary source of truth
- writing transitory notes that never become evergreen knowledge
- leaving architectural decisions undocumented and only visible through implementation artifacts

## Risks

- team-level knowledge loss
- support and operational confusion after release
- future engineering effort wasted because prior decisions were not traceable
- customer or internal misunderstanding due to conflicting docs

## Best practices

- keep documentation connected to live delivery artifacts
- link decisions to their source context and teams
- prioritize durable, maintainable knowledge over decorative descriptions
- assign actual ownership to the update and maintenance path

## Deliverables

- updated technical or product documentation
- release or support note
- linked decision or architecture result
- clear ownership record for future maintenance

## Definition of Done

The documentation process is complete when the knowledge required to maintain, support, and understand the system is current, connected, and usable without relying on hidden memory.

## KPIs

- documentation update rate on change
- percentage of critical docs linked to release or implementation artifacts
- time to onboard a new engineer using the documentation set
- rate of documentation drift or conflict

## Recommended tools

- markdown documentation repository
- reference linking and navigation
- release note or ADR template
- support and operations knowledge path

## Estimated time

- 15 minutes to 1 hour for small updates
- 0.5 to 2 days for broader documentation refreshes linked to a release or architecture change

## Practical example

A feature changes API semantics and release behavior. The implementation team updates the API contract, release note, and support reference so the operational team can understand the change without unpicking the code or chasing a previous conversation.

## Internal references

- [standards/documentation.md](../standards/documentation.md)
- [company/workflow.md](../company/workflow.md)
- [company/release-policy.md](../company/release-policy.md)
- [agents/ProductManager.md](../agents/ProductManager.md)
