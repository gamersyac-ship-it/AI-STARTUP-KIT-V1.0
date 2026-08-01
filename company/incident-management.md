# Incident Management

## Objective

The incident management process ensures the company can detect, contain, resolve, and learn from operational failures without losing accountability or traceability.

## Severity Classification

### Severity 1: Critical

- production outage,
- major data risk,
- major security exposure,
- or widespread user-impacting failure.

Required response:

- immediate incident escalation,
- team mobilization,
- executive or leadership visibility when needed,
- and a rapid stabilization objective.

### Severity 2: High

- significant but contained product degradation,
- partial outage,
- elevated security risk,
- or material user experience break.

### Severity 3: Medium

- limited impact,
- controlled operational issue,
- or product defect requiring focused follow-up.

### Severity 4: Low

- non-critical issue,
- low-risk defect,
- or internal process inconsistency without immediate production impact.

## Process

### 1. Detect and classify

Identify the issue and assign an initial severity level using the impact, exposure, and urgency of the problem.

### 2. Assign ownership

A single incident owner must be named. That owner keeps the investigation coordinated and accountable.

### 3. Contain and stabilize

Reduce user impact and stop the bleeding. Use rollback, failover, or temporary mitigation if required.

### 4. Communicate

The incident owner should communicate:

- what is happening,
- impact observed,
- mitigation steps,
- expected next update time,
- and the current owner.

### 5. Investigate root cause

Once stability has been restored, examine the precise failure mode and underlying condition.

### 6. Correct and prevent recurrence

Implement the permanent fix, update the relevant documentation, and record actions that reduce repeat risk.

## Required Records

Every incident should produce:

- incident summary,
- severity classification,
- timeline,
- affected systems or users,
- owner and responders,
- mitigation steps,
- root cause analysis,
- corrective action,
- post-incident follow-up.

## Post-Incident Review

A post-incident review must answer:

- what failed,
- why it failed,
- what was observed,
- what was done to contain it,
- what could have prevented it,
- and what follow-up action is now required.

## Example Incident

Example: a public API starts returning unauthorized errors for authenticated users after a deployment.

Response:

1. Severity is classified as High.
2. DevOps and Security are engaged immediately.
3. The release is rolled back or traffic is redirected if the mitigations are effective.
4. The incident owner logs the timeline and the impacted dependency.
5. The engineering team identifies a missing authorization condition in the release.
6. A corrective change is made, validated, and documented as a preventive action.

## Relationship to Other Documents

This document should be used with:

- [workflow.md](workflow.md)
- [release-policy.md](release-policy.md)
- [communication.md](communication.md)
- [branching-strategy.md](branching-strategy.md)
