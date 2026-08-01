# Health Check Automation

## Objective

Define the automation concept for a repository or delivery health check intended to provide a concise view of governance, quality, delivery, and operational readiness.

## Inputs

- repository or project scope
- target environment or delivery stage
- current branches, release status, and evidence records
- health indicators such as docs, tests, reviews, and release readiness

## Outputs

- health summary by area
- blockers or drift findings
- recommended next actions
- readiness report for engineering decision making

## Flow

1. Inspect repository state, evidence, and working context.
2. Evaluate quality, review, security, deployment, and documentation completeness.
3. Produce an operational readiness summary.
4. Surface blockers or governance drift that should be corrected before further work.

## Possible automations

- summarize repository health by documentation, reviews, tests, and release state;
- detect missing release evidence or quality gate coverage;
- surface project drift or automation readiness gaps for the next command.

## Integration with Claude Code/OpenCode

- generate an evidence-based system health summary for the repo;
- help the next command sequence focus on the most relevant operational gaps;
- keep the health report suitable for human review and escalation.

## Integration with VS Code

- show a health update in the workspace context;
- guide the user to the most important files or workflows requiring action;
- present the summary in a repository-consistent operation format.

## Integration with GitHub

- link the health summary to issue status, PR readiness, or release planning artifacts;
- support a continuous health view across branches and releases.

## Integration with CI/CD

- feed health information into a repository or release pipeline state;
- use health results to gate or qualify a deployment or release path.

## Risks

- health checks that are too shallow and miss actual delivery risk;
- hidden repository drift that the command cannot infer without full evidence context;
- over-reliance on metrics that do not reflect human review or governance reality.

## Checklist

- [ ] repository state is explicit
- [ ] critical quality, review, and release evidence are evaluated
- [ ] drift or blocker findings are visible
- [ ] next action is named and reviewable
- [ ] health summary can be reused by GitHub or CI context

## Roadmap of implementation

### Phase 1

- define the health signal model and output format.

### Phase 2

- add linkages to reviews, release evidence, branch state, and repository readiness.

### Phase 3

- connect health check output to GitHub and CI operational dashboards.

## Definition of Done

The `/health-check` automation is complete when it can deliver a concise, evidence-backed view of repository or delivery readiness that supports the next engineering or release decision with clarity.
