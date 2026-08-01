# Project Bootstrap Automation

## Objective

Define the automation specification for creating a new project foundation that mirrors the AI-STARTUP-KIT operating model, governance model, and repository structure.

## Inputs

- project name
- domain or business problem statement
- target delivery model
- ownership roster
- preferred stack or architecture profile
- repository target location
- initial release and quality expectations

## Outputs

- project skeleton aligned to the repository structure
- governance and operating docs baseline
- initial templates inventory
- starter review and release expectations
- a defined command entry path for all future automation commands

## Flow

1. Collect project naming, domain scope, and ownership context.
2. Create the initial repository topology and document set.
3. Copy or reference the framework’s governance and standards baseline.
4. Add project-specific placeholders and tracking artifacts.
5. Produce a bootstrap summary for human review and approval.

## Possible automations

- generate repository structure from a standard template set;
- create a project README and initial operating docs;
- initialize the working folder for company, standards, playbooks, templates, reviews, and agents;
- add a first-pass backlog or roadmap skeleton.

## Integration with Claude Code/OpenCode

- use the command to generate and organize repository artifacts in a reviewable way;
- ask the assistant to emit the project baseline as a set of structured markdown artifacts;
- preserve governance and standards references rather than creating a ad hoc structure.

## Integration with VS Code

- create the file tree and workspace scaffolding in the editor;
- open the new project’s primary docs in an ordered sequence for review;
- offer a structured checklist for human sign-off.

## Integration with GitHub

- open the new repository in GitHub-ready form;
- create a starter issue or milestone for governance setup;
- attach the generated bootstrap plan to the initial PR or branch model.

## Integration with CI/CD

- define the first quality gate expectations for repository health;
- mark the bootstrap as ready only once the directory structure, docs, and quality rules are present.

## Risks

- bootstrap drift from the intended operating model;
- project-specific slippage into undocumented decisions;
- missing review and release gates at project start.

## Checklist

- [ ] project name and boundaries are explicit
- [ ] ownership model is documented
- [ ] baseline folder structure is present
- [ ] governance references are linked
- [ ] initial review path is documented
- [ ] release and quality gates are included in the baseline

## Roadmap of implementation

### Phase 1

- define bootstrap templates and repository structure.

### Phase 2

- add project metadata and ownership defaults.

### Phase 3

- enable GitHub and CI integration for initial quality and release gates.

## Definition of Done

The project bootstrap automation is complete when the generated project can be understood as a valid operating instance of the framework and the initial quality, governance, and release expectations are present in the repository.
