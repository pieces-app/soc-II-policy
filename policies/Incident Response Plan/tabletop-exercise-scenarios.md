# Incident Response Tabletop Exercise Scenarios

## Overview

These scenarios are designed for quarterly tabletop exercises with the Incident Response Team. Each scenario includes objectives, inject timeline, and success criteria.

---

## Scenario 1: Compromised API Keys (Q1)

### Background
It's Monday morning. A security researcher contacts support@pieces.app claiming they found Pieces API keys exposed on a public GitHub repository.

### Initial Inject
- **Time:** 09:00 AM
- **Discovery:** Email from researcher with link to GitHub repo
- **Content:** Repository contains what appears to be valid API keys, customer emails, and usage statistics

### Injects Timeline

**09:15 AM:** Sentry shows unusual API traffic spike from multiple geographic locations

**09:30 AM:** Customer complaints about unauthorized API usage start arriving

**09:45 AM:** Google Cloud Console shows quota exceeded alerts for several projects

**10:00 AM:** Researcher posts about the finding on Twitter

**10:30 AM:** TechCrunch reporter emails asking for comment

### Discussion Points
1. How do we validate if the keys are legitimate?
2. What is our key rotation process?
3. How do we identify affected customers?
4. When do we notify customers?
5. How do we handle the media inquiry?

### Success Criteria
- [ ] Incident severity correctly classified (S2)
- [ ] API keys rotated within 2 hours
- [ ] Affected customers identified via BigQuery
- [ ] Customer notification sent within 24 hours
- [ ] Public response coordinated with legal

---

## Scenario 2: Insider Threat - Departing Employee (Q2)

### Background
Friday afternoon. HR notifies IT that a senior engineer gave two weeks notice. The employee has extensive access to production systems.

### Initial Inject
- **Time:** 14:00 PM
- **Discovery:** HR notification of resignation
- **Context:** Employee seems disgruntled about compensation

### Injects Timeline

**Day 3:** Google Cloud Audit logs show the employee exported large amounts of data from BigQuery

**Day 5:** GitHub audit logs show cloning of all private repositories

**Day 7:** Employee's personal GitHub suddenly has a new "pieces-clone" repository (private)

**Day 9:** Employee announces joining a competitor

**Day 10:** Unusual after-hours access patterns detected

### Discussion Points
1. When do we revoke access - immediately or at departure?
2. How do we monitor for data exfiltration?
3. Legal implications of accessing personal GitHub?
4. How do we preserve evidence?
5. When do we involve law enforcement?

### Success Criteria
- [ ] Access monitoring increased without alerting employee
- [ ] Legal counsel engaged for guidance
- [ ] Evidence properly preserved
- [ ] Access revoked at appropriate time
- [ ] Exit interview includes security debriefing

---

## Scenario 3: Ransomware Attack on Development Environment (Q3)

### Background
Tuesday 03:00 AM. On-call engineer receives multiple Sentry alerts about services failing.

### Initial Inject
- **Time:** 03:00 AM
- **Discovery:** Sentry alerts for service failures
- **Initial Finding:** GitHub Actions runners are failing with "files encrypted" errors

### Injects Timeline

**03:15 AM:** GitHub repositories show README files replaced with ransom notes

**03:30 AM:** Google Cloud Build pipelines failing

**03:45 AM:** Ransom note demands 50 Bitcoin, threatens to leak customer data

**04:00 AM:** Some customer-facing services start degrading

**04:30 AM:** Attacker emails proof of stolen data

**05:00 AM:** News of the attack appears on dark web forums

### Discussion Points
1. How do we determine the scope of encryption?
2. What is our backup restoration process?
3. Do we engage law enforcement immediately?
4. How do we communicate with customers about potential degradation?
5. What if backups are also encrypted?

### Success Criteria
- [ ] Incident correctly escalated to S1
- [ ] CEO and legal notified within 1 hour
- [ ] Systems isolated to prevent spread
- [ ] Backup viability verified
- [ ] Customer communication sent about degradation
- [ ] Law enforcement notified
- [ ] Cyber insurance carrier notified

---

## Scenario 4: Supply Chain Compromise - Malicious NPM Package (Q4)

### Background
Wednesday afternoon. GitHub Dependabot creates multiple critical security alerts across repositories.

### Initial Inject
- **Time:** 14:30 PM
- **Discovery:** Dependabot alerts for critical vulnerability
- **Details:** Popular NPM package was compromised with credential stealer

### Injects Timeline

**14:45 PM:** Security advisory published - package was compromised for 4 hours yesterday

**15:00 PM:** We had automated builds running during the compromise window

**15:30 PM:** Customer reports their Pieces extension is triggering antivirus alerts

**16:00 PM:** We discover the malicious package in our production build

**16:30 PM:** Multiple customers report suspicious activity

### Discussion Points
1. How do we determine which builds are affected?
2. Can we identify all customers who downloaded affected versions?
3. How do we coordinate with the package maintainer?
4. What is our customer notification strategy?
5. How do we prevent this in the future?

### Success Criteria
- [ ] Affected versions identified via build logs
- [ ] Customer impact assessed via telemetry
- [ ] Patched version released within 4 hours
- [ ] Customer notification with specific version information
- [ ] Post-incident supply chain security improvements identified

---

## Scenario 5: Data Leak via Misconfigured Google Cloud Storage (Q1 - Year 2)

### Background
Thursday morning. A security researcher emails that they found an open Google Cloud Storage bucket containing customer data.

### Initial Inject
- **Time:** 10:00 AM
- **Discovery:** Email to security@pieces.app
- **Content:** Researcher provides URL to publicly accessible bucket

### Injects Timeline

**10:15 AM:** Verification confirms bucket contains customer usage logs and email addresses

**10:30 AM:** Google Cloud logs show bucket was public for 3 months

**10:45 AM:** Access logs show 1,000+ downloads from various IPs

**11:00 AM:** Researcher says they'll publish a blog post in 48 hours

**11:30 AM:** We discover similar misconfiguration in 2 other buckets

### Discussion Points
1. How do we determine what data was exposed?
2. Can we identify who accessed the data?
3. GDPR requires 72-hour notification - when does the clock start?
4. How do we work with the researcher on responsible disclosure?
5. How did this misconfiguration happen?

### Success Criteria
- [ ] Buckets secured within 30 minutes
- [ ] Data exposure scope determined via BigQuery
- [ ] GDPR notification timeline understood
- [ ] Researcher coordination established
- [ ] Root cause identified (IaC drift, manual change, etc.)

---

## Scenario 6: Cryptojacking in GitHub Actions (Q2 - Year 2)

### Background
Monday morning. Finance notices unusual Google Cloud charges over the weekend.

### Initial Inject
- **Time:** 09:00 AM
- **Discovery:** Finance flags $50,000 in unexpected compute charges
- **Initial Finding:** GitHub Actions ran for 200+ hours over weekend

### Injects Timeline

**09:30 AM:** Investigation shows PRs from new contributors triggered the builds

**10:00 AM:** PRs contained hidden cryptocurrency mining code

**10:30 AM:** We discover our GitHub Actions can be triggered by any PR

**11:00 AM:** Google Cloud threatens to suspend account for Terms violation

**11:30 AM:** Similar PRs found in other public repositories

### Discussion Points
1. How do we stop the bleeding immediately?
2. Can we identify all malicious PRs?
3. How do we work with Google Cloud on the charges?
4. What GitHub settings need to change?
5. How do we detect this faster in the future?

### Success Criteria
- [ ] Malicious workflows terminated immediately
- [ ] GitHub Actions permissions corrected
- [ ] Cost impact documented
- [ ] Google Cloud engaged about charges
- [ ] Monitoring implemented for unusual compute usage

---

## Exercise Execution Guide

### Pre-Exercise (1 week before)
1. Schedule 2-hour block with IRT members
2. Assign roles (some may play multiple roles)
3. Share only the background, not the injects
4. Remind participants about IR plan location

### During Exercise
1. **Introduction (10 min)**
   - Review scenario background
   - Assign roles
   - Set ground rules

2. **Scenario Execution (60 min)**
   - Present initial inject
   - Allow team discussion and decisions
   - Introduce timeline injects at specified times
   - Document all decisions and actions

3. **Resolution (20 min)**
   - Team presents their response plan
   - Walk through what would happen next
   - Identify any gaps or issues

4. **Debrief (30 min)**
   - What went well?
   - What was challenging?
   - What was missing from our plan?
   - What tools/access did we need?

### Post-Exercise
1. Document lessons learned
2. Create action items for plan improvements
3. Update IR plan based on findings
4. Schedule follow-up for action items

### Success Metrics
- Time to correct severity classification
- Time to key decisions
- Completeness of response
- Team coordination effectiveness
- Documentation quality

---

## Annual Exercise Schedule

| Quarter | Primary Scenario | Backup Scenario |
| :------ | :-------------- | :-------------- |
| Q1 | Compromised API Keys | Data Leak via Misconfiguration |
| Q2 | Insider Threat | Cryptojacking |
| Q3 | Ransomware Attack | DDoS Attack (bonus) |
| Q4 | Supply Chain Compromise | Zero-Day Vulnerability (bonus) |

Rotate scenarios yearly and update based on current threat landscape.
