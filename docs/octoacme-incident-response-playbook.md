# OctoAcme — Incident Response Playbook

## Purpose
Establish a structured, blameless incident response process to minimize impact and enable rapid recovery.

## Severity Levels

| Level | Definition | Examples | Response Time | Scope |
|-------|-----------|----------|---|---|
| **SEV-1 (Critical)** | Complete outage or severe degradation affecting all users | All services down, data loss, security breach | Immediate (0-5 min) | All hands; exec escalation |
| **SEV-2 (High)** | Major feature unavailable or significant degradation | Feature unavailable to subset of users, 10-50% latency increase | Within 5-15 min | Core team + SMEs |
| **SEV-3 (Medium)** | Minor feature unavailable or noticeable degradation | Non-critical feature broken, <10% latency increase | Within 15-60 min | On-call engineer + relevant SME |
| **SEV-4 (Low)** | Cosmetic or isolated issue | UI bug, documentation typo | Next business day | Reporter + owner |

---

## SEV-1 & SEV-2 Incident Response

### Phase 1: Detect & Alert (0-5 min)

**Who:** Monitoring system, support team, or customer

**Actions:**
- [ ] Alert triggers (automated) or report received (manual)
- [ ] On-call engineer notified via Slack + SMS
- [ ] Severity assessed: SEV-1 vs. SEV-2
- [ ] Slack incident channel created (e.g., #incident-2026-05-07-001)

**Communication:**
- Slack: Post incident summary with severity, brief description, and incident commander name

---

### Phase 2: Triage & Response (5-15 min)

**Who:** On-call engineer + Incident Commander (IC)

**Actions:**
- [ ] Incident Commander assigned (usually most senior on-call)
- [ ] Engineering team notified to join incident channel
- [ ] Customer impact assessed (which users/features affected?)
- [ ] Severity confirmed or escalated
- [ ] Initial hypothesis: is this a deployment issue, infrastructure issue, or external dependency?
- [ ] Rollback vs. forward fix decision made

**Decision Tree:**
Is this caused by recent deployment? ├─ YES → Prepare rollback │ ├─ If <15 min → Rollback immediately │ └─ If >15 min → Assess forward fix vs. rollback trade-off └─ NO → Investigate infrastructure/dependency ├─ Check monitoring dashboards ├─ Review error logs └─ Contact dependent teams if external issue

**Communication:**
- Slack incident channel: Post initial assessment, hypothesis, and action plan
- Status page (if applicable): Update customer-facing status page to "Investigating"

---

### Phase 3: Mitigation (Ongoing)

**Who:** Incident Commander + Engineering team

**Actions (in parallel):**
- [ ] **Mitigation track:** Execute rollback or forward fix
- [ ] **Investigation track:** Root cause analysis begins (separate team if possible)
- [ ] **Communication track:** Status updates every 15 min (to leadership, customers, internal)

**Rollback Checklist:**
- [ ] Identify last known-good commit/tag
- [ ] Verify rollback has been tested (gate check)
- [ ] Coordinate with Database team if schema changes needed
- [ ] Execute rollback to production
- [ ] Verify metrics normalize and alerts clear
- [ ] Post-incident analysis scheduled (within 24 hours)

**Forward Fix Approach:**
- [ ] If rollback risks greater than moving forward → Apply targeted fix
- [ ] Pair of engineers: one reviewing, one implementing
- [ ] Expedited code review (IC approves)
- [ ] Deploy fix; monitor metrics

---

### Phase 4: Stabilization & Recovery (30 min - 2 hours)

**Who:** Incident Commander + Engineering team

**Actions:**
- [ ] Confirm incident is resolved (metrics normal, alerts cleared)
- [ ] Post-incident communication sent
- [ ] Customer-facing status page updated to "Resolved"
- [ ] Internal incident channel summarized
- [ ] Incident timeline documented

**Communication:**
- All stakeholders: "Incident resolved at [time]. Root cause: [summary]. Investigating further."

---

### Phase 5: Post-Incident Review (Within 24 hours)

**Attendees:** IC, engineering team, product lead, project manager

**Duration:** 30-45 minutes

**Agenda:**
1. **Timeline:** What happened step-by-step?
2. **Root cause:** Why did it happen?
3. **Detection:** How was it detected? Could we detect faster?
4. **Response:** What went well? What could improve?
5. **Action items:** Prevent recurrence

**Post-Incident Report Template:**

```markdown
# Incident Report: [Incident ID]

## Summary
- **Severity:** SEV-1/2/3
- **Duration:** [Start] - [End] ([X min/hours])
- **Impact:** [Affected users/features/revenue]

## Timeline
- [HH:MM] Alert triggered
- [HH:MM] On-call engineer notified
- [HH:MM] Root cause identified
- [HH:MM] Mitigation applied
- [HH:MM] Incident resolved

## Root Cause
- Primary cause: [What went wrong?]
- Contributing factors: [What made it worse?]

## Resolution
- Action taken: [Rollback | Fix deployed]
- Verification: [How did we confirm resolution?]

## What Went Well
- [Recognition of fast response, good communication, etc.]

## What Could Improve
- [Process, tooling, monitoring gaps]

## Action Items (Owner → Due Date)
- [ ] Implement monitoring for [metric] to detect faster (Engineer → Due date)
- [ ] Add test case for [scenario] to prevent recurrence (Engineer → Due date)
- [ ] Update runbook for [process] (PM → Due date)
- [ ] Customer communication follow-up (Support → Due date)

## Lessons Learned
- [What did we learn?]
- [How do we prevent this?]
Blameless Culture:

Focus on systems and processes, not individuals
Avoid language like "human error" or "careless mistake"
Ask "Why?" 5 times to understand root cause
Celebrate fast response and learning; don't punish
SEV-3 & SEV-4 Incident Response
SEV-3 (Medium)
On-call engineer investigates; no escalation needed unless severity increases
Update status within 15 min to customers/stakeholders
Fix or add to next sprint backlog
Post in #operations for team awareness
SEV-4 (Low)
Logged in issue tracker
Assigned to owner for next available sprint
No immediate communication required (bundle in status update if needed)
Incident Commander Responsibilities
The Incident Commander (IC) is the single point of coordination and has final authority during the incident.

Responsibilities:

 Establish severity and escalation level
 Coordinate teams (don't let everyone talk at once; use IC as hub)
 Make trade-off decisions (rollback vs. forward fix, notify customers, etc.)
 Ensure timely communication to stakeholders
 Document timeline and decisions
 Schedule and facilitate post-incident review
 Prevent scope creep (keep focus on stabilization, not optimization)
IC Escalation:

For SEV-1, notify VP Engineering immediately after detection
For SEV-2, notify Director/Manager after mitigation starts
For cross-team incidents, notify other team leads in incident channel
Tools & Access
Ensure incident response team has access to:

 Monitoring dashboard (Datadog, New Relic, CloudWatch, etc.)
 Logging system (ELK, Splunk, CloudWatch Logs)
 Deployment/rollback tools (CI/CD pipeline, kubectl, etc.)
 Database admin tools (if applicable)
 Customer notification system (status page, email, SMS)
 Incident tracking system (Jira, GitHub Issues, PagerDuty)
Weekly Incident Review
During weekly team meetings:

 Review open incidents (status, ETA for action items)
 Share post-incident reports and lessons learned
 Update runbooks based on new incidents
 Assess monitoring gaps and tool improvements
Continuous Improvement
Update this playbook based on real incident learnings
Run incident simulations quarterly to test response
Track incident metrics (MTTR, MTTD, recurrence rate) and share trends
