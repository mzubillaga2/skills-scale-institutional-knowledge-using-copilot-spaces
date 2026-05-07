# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

### Key Interactions
- **With QA/Testing Specialist:** Collaborate on test coverage requirements, testability improvements, and acceptance criteria validation
- **With Technical Lead:** Receive design guidance and architectural decisions; participate in code reviews
- **With Project Manager:** Provide effort estimates and status updates; flag blockers early

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

### Key Interactions
- **With Project Manager:** Weekly sync on timeline, risks, and dependencies
- **With Developers:** Refine requirements, validate acceptance criteria, answer clarifying questions
- **With Stakeholders:** Provide roadmap alignment, business context, and decision rationale

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

### Key Interactions
- **With Product Manager:** Weekly alignment on roadmap changes, priorities, and scope
- **With Technical Lead:** Understand technical risks, feasibility, and effort estimates
- **With QA/Testing Specialist:** Track quality metrics and release readiness
- **With Stakeholders:** Provide status updates and escalation handling

---

## QA / Testing Specialist

### Role Summary
QA/Testing Specialists validate that software meets acceptance criteria, quality standards, and user expectations. They own the testing strategy, automation, and acceptance verification for delivered work.

### Responsibilities
- Create and maintain test plans and test cases
- Automate regression and integration tests
- Conduct manual testing, exploratory testing, and user acceptance testing (UAT)
- Validate acceptance criteria before marking work as done
- Identify and report defects with clear reproduction steps
- Collaborate with developers on test coverage and testability
- Ensure security and compliance testing is included in release validation

### Goals
- Ensure zero critical defects reach production
- Maintain high test coverage and fast test execution
- Reduce production incidents through thorough validation
- Enable fast, confident deployments

### Typical Communication
- Sprint planning and backlog refinement (estimating test effort)
- Daily standups (test status and blockers)
- PR reviews and code quality checks
- Release readiness reviews
- Quality metrics dashboards and status reports

### Key Interactions
- **With Developers:** Partner on test automation, review PRs for testability, define test coverage standards
- **With Product Manager:** Validate user stories for clear acceptance criteria, participate in planning to estimate testing effort
- **With Project Manager:** Report on test status, flag quality risks, provide input on release readiness
- **With Security/Compliance Lead:** Coordinate on security testing and compliance validation

---

## Technical Lead / Architect

### Role Summary
Technical Leads own system design decisions, provide technical mentorship, and ensure projects maintain architectural integrity and scalability. They balance innovation with maintainability.

### Responsibilities
- Define technical architecture and design standards
- Review technical designs and provide guidance on feasibility
- Mentor developers and support technical growth
- Identify and mitigate technical risks and debt
- Ensure code quality, performance, and security standards are met
- Make trade-off decisions on technology choices and design patterns
- Participate in post-mortems and drive technical improvements

### Goals
- Maintain technical excellence and code quality
- Reduce technical debt and system complexity
- Enable team to scale and ship faster
- Prevent architectural missteps and rework

### Typical Communication
- Design reviews and RFC (Request for Comments) discussions
- Code reviews and PR feedback
- Technical spike sessions
- Architecture decision logs (ADLs)
- Retrospectives and post-mortems

### Key Interactions
- **With Developers:** Mentor, code review, pair programming, technical decision-making
- **With Project Managers:** Advise on technical risks, effort estimation, and feasibility
- **With Product Managers:** Consult on technical feasibility of features and trade-offs
- **With Security/Compliance Lead:** Ensure architectural decisions meet security requirements

---

## Scrum Master / Agile Coach

### Role Summary
Scrum Masters facilitate agile ceremonies, remove impediments, and coach teams on agile practices. They enable the team to execute efficiently and continuously improve.

### Responsibilities
- Plan and facilitate daily standups, sprint planning, reviews, and retrospectives
- Remove impediments and blockers identified by the team
- Coach team on agile principles and healthy team dynamics
- Maintain sprint board and tracking metrics (velocity, burndown, cycle time)
- Identify process improvements and run experiments
- Protect team from external interruptions during sprints
- Ensure retrospective action items are tracked and completed

### Goals
- Enable high team velocity and throughput
- Create a self-organizing, empowered team
- Reduce process friction and cycle time
- Foster continuous learning and improvement

### Typical Communication
- Daily standups (15 min)
- Sprint planning and estimation sessions
- Retrospectives and improvement discussions
- Velocity and metric tracking
- Weekly leadership syncs on team health

### Key Interactions
- **With Project Manager:** Coordinate planning and release readiness, escalate blockers
- **With Developers:** Facilitate ceremonies, support impediment removal, coach on agile practices
- **With Product Manager:** Ensure backlog is ready and prioritized for planning

---

## Stakeholder / Sponsor

### Role Summary
Stakeholders and Sponsors provide business context, secure resources, and ensure projects deliver value aligned with organizational strategy. They own executive oversight and approval authority.

### Responsibilities
- Approve project charter and scope
- Secure budget and resource allocations
- Provide business context and success metrics
- Remove organizational blockers and escalations
- Review milestone progress and release decisions
- Communicate project status to leadership and other stakeholders
- Make trade-off decisions on scope, timeline, and quality

### Goals
- Ensure projects deliver business value on time
- Maximize ROI and alignment with organizational strategy
- Remove barriers to project success
- Maintain transparency with leadership

### Typical Communication
- Monthly stakeholder status briefings
- Approval gates for initiation, planning, and release
- Escalation handling and decision-making
- Executive steering committee meetings (if applicable)
- Incident notifications and post-mortem reviews

### Key Interactions
- **With Project Manager:** Receive regular status updates, provide guidance on escalations
- **With Product Manager:** Align on roadmap and business priorities, approve scope changes

---

## Security / Compliance Lead

### Role Summary
Security and Compliance Leads ensure projects meet regulatory and security requirements throughout the development lifecycle. They reduce risk and protect customer data and organizational assets.

### Responsibilities
- Define security and compliance requirements for projects
- Review designs and code for security vulnerabilities
- Conduct security testing and threat modeling
- Manage security incident response and escalation
- Ensure audit trails and compliance documentation
- Advise on encryption, authentication, and data handling
- Participate in post-mortems on security incidents

### Goals
- Prevent security breaches and data loss
- Maintain compliance with regulations and standards
- Reduce risk through proactive security practices
- Enable team to ship securely and confidently

### Typical Communication
- Security design reviews and threat modeling sessions
- Code review participation (security focus)
- Incident response and post-mortems
- Compliance audits and reporting
- Security training and awareness sessions

### Key Interactions
- **With Technical Lead:** Collaborate on secure design and architecture decisions
- **With Developers:** Provide security guidance and code review feedback
- **With QA Specialists:** Coordinate on security and penetration testing
- **With Project Manager:** Advise on security risks and escalation procedures

---

## Customer / User Representative

### Role Summary
Customer/User Representatives advocate for end-user needs, validate usability, and ensure products solve real customer problems. They provide the voice of the customer in project decisions.

### Responsibilities
- Represent end-user needs and perspective in project discussions
- Participate in user research and usability testing
- Validate product features for user value and usability
- Provide feedback on prototypes and designs
- Identify gaps between product vision and user needs
- Participate in beta testing and UAT
- Share customer feedback with Product and Project teams

### Goals
- Ensure products meet real user needs and deliver value
- Maximize user satisfaction and adoption
- Reduce rework by catching usability issues early
- Build empathy for users across the team

### Typical Communication
- Design review sessions and usability testing
- Backlog refinement (user story validation)
- Sprint demos and feedback sessions
- Customer advisory board meetings (if applicable)
- Post-release feedback and metrics review

### Key Interactions
- **With Product Manager:** Provide user research insights and validate prioritization
- **With Developers:** Participate in design reviews and usability testing
- **With QA Specialists:** Participate in UAT and acceptance criteria validation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Reference the Key Interactions section to understand cross-functional collaboration patterns and communication needs.

