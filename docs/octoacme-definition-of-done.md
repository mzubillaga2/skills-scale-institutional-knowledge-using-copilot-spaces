# OctoAcme — Definition of Done

## Purpose
Establish clear, consistent quality gates that apply across all project phases to ensure work meets OctoAcme standards before moving to the next phase.

## Sprint / Iteration Definition of Done

Work items (user stories, tasks, bugs) are considered "Done" when ALL of the following criteria are met:

### Code Quality
- [ ] Code follows team style guide and conventions
- [ ] Code is peer-reviewed and approved by at least one other developer
- [ ] No critical or high-severity linting/static analysis warnings
- [ ] Code duplication is minimized
- [ ] Comments and docstrings are clear and accurate

### Testing
- [ ] Unit tests written and passing (target: ≥80% code coverage for new code)
- [ ] Integration tests passing (if applicable)
- [ ] Manual testing completed and documented
- [ ] No critical or high-severity bugs identified

### Acceptance Criteria
- [ ] All acceptance criteria from the user story are met
- [ ] QA/Testing Specialist has validated completion
- [ ] Product Manager has approved feature meets requirements

### Documentation & Communication
- [ ] Code changes documented (README, inline comments, design doc)
- [ ] PR description clearly explains the change and includes issue link
- [ ] Release notes drafted (if customer-facing change)
- [ ] Stakeholders informed of relevant changes

### Security & Compliance
- [ ] Security scanning (SAST/DAST) passing with no critical issues
- [ ] Sensitive data is not exposed in code, logs, or error messages
- [ ] Security/Compliance Lead has reviewed if applicable
- [ ] Compliance requirements have been met

### Performance & Observability
- [ ] Performance tests passing (if applicable)
- [ ] Monitoring and alerting configured for new functionality
- [ ] Logging is sufficient for debugging and auditing
- [ ] Metrics for success criteria are being tracked

---

## Release Definition of Done

A release is considered ready to deploy to production when ALL of the following criteria are met:

### Code & Build
- [ ] All PRs merged to release branch
- [ ] Continuous Integration (CI) pipeline passing
- [ ] Build artifacts generated and stored securely
- [ ] No critical or high-severity security scan findings

### Testing & QA
- [ ] All acceptance criteria validated by QA
- [ ] Regression test suite passing
- [ ] End-to-end smoke tests passing on staging environment
- [ ] Performance baselines met or documented
- [ ] No open critical or high-severity bugs

### Security & Compliance
- [ ] Security review completed and sign-off obtained
- [ ] Compliance checklist completed (privacy, accessibility, etc.)
- [ ] Rollback plan documented and tested
- [ ] Incident response runbook updated (if applicable)

### Documentation & Communication
- [ ] Release notes finalized with all changes documented
- [ ] Deployment runbook reviewed and ready
- [ ] Customer-facing documentation updated (if applicable)
- [ ] Support team briefed on changes
- [ ] Stakeholders notified of deployment plan and timeline

### Monitoring & Rollback
- [ ] Dashboards and alerts configured
- [ ] Logging and error tracking operational
- [ ] Rollback procedure tested and documented
- [ ] On-call engineer assigned and briefed
- [ ] Post-deployment verification checklist prepared

---

## Project / Milestone Definition of Done

A project milestone or phase is considered "Done" when:

### Delivery
- [ ] All committed work items are completed to Sprint DoD
- [ ] All acceptance criteria met
- [ ] No open critical or high-severity issues

### Quality & Testing
- [ ] Quality metrics meet targets (test coverage, defect rates, etc.)
- [ ] Performance and security baselines met

### Documentation & Knowledge Transfer
- [ ] Project documentation complete and reviewed
- [ ] Team runbooks and operational procedures documented
- [ ] Knowledge transfer completed (no single-person dependencies)
- [ ] Design decisions documented (ADLs, decision logs)

### Stakeholder Sign-off
- [ ] Sponsor approval on deliverables and success metrics
- [ ] Customer UAT completed (if applicable)
- [ ] Go/no-go decision made for release

### Retrospective & Improvement
- [ ] Retrospective held with action items captured
- [ ] Lessons learned documented
- [ ] Process improvements scheduled for next iteration

---

## How to Use This Document

1. **During Sprint Planning:** Review the Sprint DoD checklist and ensure team understands each item
2. **During Execution:** Use the checklist as a quality gate before marking work complete
3. **Before Release:** Verify all Release DoD items are met before deploying
4. **Post-Release:** Update DoD based on lessons learned in retrospectives

---

## Continuous Improvement

- Review this DoD quarterly and update based on team feedback
- Add project-specific DoD items as needed (stored in project repo)
- Track DoD compliance metrics and share in retrospectives
