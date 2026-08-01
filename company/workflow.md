# Workflow

## Purpose

This workflow defines the mandatory operating path for any initiative governed by AI-STARTUP-KIT. Its purpose is to preserve business clarity, engineering quality, delivery discipline, and release accountability.

## Operating Principle

No code is built on a vague idea. Every request, improvement, or defect must pass through an explicit chain of definition, technical review, implementation, verification, and delivery approval.

## Official Flow

CEO

↓

Product Manager

↓

CTO

↓

FullStack

↓

QA

↓

Security

↓

DevOps

↓

Documentation

↓

Deploy

## Stage Inputs and Outputs

### CEO

Input:

- strategic business direction,
- commercial or product goal,
- sponsor alignment.

Output:

- initial direction and approval to proceed.

### Product Manager

Input:

- business objective,
- customer or market problem,
- strategic priority.

Output:

- epic,
- user story,
- acceptance criteria,
- priority and risk statement.

### CTO

Input:

- approved story or epic,
- technical constraints and business context.

Output:

- architectural review,
- constraints,
- technical approval or rejection,
- ADR or architecture decision note when required.

### FullStack

Input:

- approved technical direction and acceptance criteria.

Output:

- implementation,
- testable code,
- unit or integration evidence,
- minimal delivery documentation.

### QA

Input:

- implementation evidence and functional scope.

Output:

- QA report,
- regressions identified,
- release confidence statement.

### Security

Input:

- implementation artifact and security-sensitive scope.

Output:

- security review,
- blocker or approval evidence,
- risk register update if needed.

### DevOps

Input:

- approved and tested release candidate,
- environment readiness information.

Output:

- deployment plan,
- environment readiness,
- rollback path confirmation.

### Documentation

Input:

- final change evidence and release artifact.

Output:

- updated documentation,
- cross-linked release knowledge,
- maintainability evidence.

### Deploy

Input:

- validated release evidence and approval chain.

Output:

- deployed release,
- traceable production outcome.

## What Must Be True to Advance

A stage may pass work forward only when:

- the prior output is complete,
- evidence is attached,
- the next receiver can understand the scope,
- and current quality gates are satisfied.

## Definition of Ready

A task is ready to execute when:

- the business problem is understood,
- success criteria are explicit,
- dependencies are known,
- a priority is assigned,
- the expected value is defined,
- and the entry point is approved by the responsible owner.

## Definition of Done

A task is done when:

- all acceptance criteria are satisfied,
- QA evidence is recorded,
- Security review is recorded,
- Documentation is updated,
- DevOps confirms deployment readiness,
- and the release is traceable to the original requirement.

## Rules of Execution

- No stage may be skipped.
- No code may be written from an unapproved business request.
- No release may proceed without QA and Security evidence.
- No architecture change may happen without CTO review and clear documentation.
- Any scope change must return to the Product Manager before continuing.

## Bug Handling Flow

Bug

↓

QA

↓

Product Manager

↓

CTO

↓

FullStack

↓

QA

↓

Security

↓

DevOps

↓

Documentation

↓

Deploy

## Improvement Handling Flow

Idea

↓

Product Manager

↓

CTO

↓

FullStack

↓

QA

↓

Security

↓

DevOps

↓

Documentation

↓

Deploy

## Quality Expectations

All work should be:

- scalable,
- secure,
- modular,
- reusable,
- documented,
- testable,
- and operationally understandable.

## Relationship to Other Documents

This document is the execution backbone of the company model. It must be read with:

- [communication.md](communication.md)
- [release-policy.md](release-policy.md)
- [branching-strategy.md](branching-strategy.md)
- [incident-management.md](incident-management.md)
