---
title: Incident Response Plan
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
stakeholders:
  - Mark Widman (Chief Technology Officer)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Sam Jones (Chief AI Officer)
  - Georgia Donmoyer (GRC)
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2023-01-01
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC7.2, CC7.3, CC7.4, CC6.6
    - ISO/IEC 27001 Annex A: A.5.25, A.5.26, A.5.28, A.5.29
  controls:
    - Google Cloud Security Command Center, GitHub Advanced Security, Sentry
repo: https://github.com/pieces-app/soc-II-policy
---

# Incident Response Plan

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))

**Effective Date:** January 1, 2023

# Purpose 

This document establishes the plan for managing information security incidents and events and provides guidance for employees and incident responders who believe they have discovered, or are responding to, a security incident.

# Scope 

This plan covers all information security or data privacy events or incidents affecting Mesh Intelligent Technologies, Inc. systems, data, personnel, and facilities.

# Incident and Event Definitions

- A security event is an observable occurrence relevant to the confidentiality, availability, integrity, or privacy of company-controlled data, systems, or networks.
- A security incident is a security event that results in loss or damage to the confidentiality, availability, integrity, or privacy of company-controlled data, systems, or networks.

# Incident Reporting & Documentation

## Reporting 

If a Mesh Intelligent Technologies, Inc. employee, contractor, user, or customer becomes aware of an information security event or incident, possible incident, imminent incident, unauthorized access, policy violation, security weakness, or suspicious activity, then they shall immediately report the information using one of the following communication channels:

- Email support@pieces.app with information or reports about the event or incident

Reporters should act as a good witness. Reports should include specific details about what has been observed or discovered.

## Severity 

Mesh Intelligent Technologies, Inc. IT Team shall monitor incident and event tickets and shall assign a ticket severity based on the following categories.

### S3/S4 - Low and Medium Severity

Issues meeting this severity are simply suspicions or odd behaviors. They are not verified and require further investigation. There is no clear indicator that systems have tangible risk and do not require emergency response. This includes lost/stolen laptop with disk encryption, suspicious emails, outages, strange activity on a laptop, etc.

### S2 - High Severity

High severity issues relate to problems where an adversary or active exploitation hasn't been proven yet, and may not have happened, but is likely to happen. This may include lost/stolen laptop without encryption, vulnerabilities with direct risk of exploitation, threats with risk or adversarial persistence on our systems (e.g.: backdoors, malware), malicious access of business data (e.g.: passwords, vulnerability data, payments information).

### S1 - Critical Severity

Critical issues relate to actively exploited risks and involve a malicious actor or threats that put any individual at risk of physical harm. Identification of active exploitation is required to meet this severity category.

## Escalation and Internal Reporting

The incident escalation contacts can be found below in Appendix A.

- S1 - Critical Severity: S1 issues require immediate notification to Engineering management.
- S2 - High Severity: A support ticket must be completed and the appropriate manager (see S1 above) must also be notified via Google Chat with a reference to the ticket number.
- S3/S4 - Medium and Low Severity: A support ticket must be created and assigned to the appropriate department for response.

## Documentation

All reported security events, incidents, and response activities shall be documented and adequately protected in GitHub Issues.

A root cause analysis may be performed on all verified S1 security incidents. A root cause analysis report shall be documented and referenced in the incident ticket. The root cause analysis shall be reviewed by the Director of Engineering who shall determine if a post-mortem meeting will be called.

# Incident Response Process

For critical issues, the IRT follows an iterative process to investigate, contain, eradicate, recover, and learn.

### Summary

- Event reported
- Triage and analysis
- Investigation
- Containment and neutralization (short-term)
- Recovery and vulnerability remediation
- Hardening and detection improvements (lessons learned)

### Detailed

- IT Manager or VP of Support will manage the incident response effort
- If necessary, a central “War Room” will be designated, which may be a physical or virtual location (e.g., Google Chat Space)
- A recurring Incident Response Meeting will occur at regular intervals until the incident is resolved
- Legal and executive staff will be informed as required

### Incident Response Meeting Agenda

- Update incident ticket and timelines
- Document new Indicators of Compromise (IOCs)
- Perform investigative Q&A
- Apply emergency mitigations
- External reporting / breach reporting assessment
- Plan long-term mitigations
- Document RCA
 - Additional items as needed

### Internal Communications

- IT Manager or VP of Support will report the incident to legal and executive staff as required
- The Incident Response Team will deliver appropriate notifications to personnel and affected departments
- The VP of Support or CEO will notify users, customers, law enforcement, and other third-parties as necessary and in line with the requirements listed in External Communications and Breach Reporting

## Special Considerations

### Internal Issues

If the malicious actor is an internal employee, contractor, vendor, or partner, escalation must be handled sensitively. The IM contacts HR and the CEO directly and limits disclosure to a strict need-to-know.

### Compromised Communications

Incident responders must have Google Chat arranged before listing themselves as incident members. If there are IT communication risks, an out of band solution will be chosen and communicated to incident responders via cell phone.

### Root Account Compromise

If a Google Cloud root account compromise is known or expected, refer to the playbook in Appendix D.

## Additional Requirements

- All events and incidents are documented
- Suspected incidents are assessed and classified as event or incident
- Response is performed according to this plan and any associated procedures
- All incidents are formally documented, with RCA when applicable
- Evidence is collected, preserved, and protected in line with industry guidance (e.g., NIST SP 800-86)
- Breach determinations are made by the CEO and Legal Counsel with Executive Management
- Mesh Intelligent Technologies, Inc. will notify customers, partners, affected parties, and regulators in accordance with policies, contracts, and law
- This plan is reviewed and formally tested at least annually; testing results, findings, and lessons learned are documented

# External Communications and Breach Reporting

Legal and executive staff shall confer with technical teams in the event of unauthorized access to company or customer systems, networks, and/or data. Legal staff along with the CEO shall determine if breach reporting or external communications are required. If external communications are required, breaches shall be reported to customers, consumers, data subjects and regulators without undue delay and in accordance with all contractual commitments and applicable legislation. The following notification table identifies entities and timelines for notifications.

| Who | Contact | Method | When |
| :---- | :---- | :---- | :---- |
| ICO (GDPR) | https://ico.org.uk/for-organisations/report-a-breach | Web | Within 72 hours |
| Users |  | E-mail | Once data at risk and impacted users have been identified |
| Customers |  | E-mail | Once data at risk and impacted customers have been identified |
| Press |  | According to legal and executive staff decision | According to legal and executive staff decision |
| Law Enforcement |  | Telephone | As soon as possible once criminal activity is suspected |

No personnel may disclose information regarding incident or potential breaches to any third party or unauthorized person, including the media, without the approval of legal and/or executive management.

# Mitigation and Remediation

Legal and executive staff determine immediate and long-term mitigations or remedial actions. Executive staff direct planning, communication, and execution of those activities.

# Cooperation with Customers, Data Controller and Authorities

As needed, the company cooperates with customers, Data Controllers, and regulators to fulfill obligations in the event of an incident or breach.

# Roles & Responsibilities

Every employee and user of Mesh Intelligent Technologies, Inc. information resources has responsibilities toward protecting information assets.

## Response Team Members

| Role | Responsibility |
| :---- | :---- |
| Incident Manager | The Incident Manager is the primary and ultimate decision maker during the response period. The Incident Manager is ultimately responsible for resolving the incident and formally closing incident response actions. See Appendix A for Incident Manager contact information. These responsibilities include: Ensuring the right people from all functions are actively involved as appropriate; communicating status updates to the appropriate person or teams at regular intervals; resolving incidents in the immediate term; determining necessary follow-up actions; assigning follow-up activities to the appropriate people; promptly reporting incident details which may trigger breach reporting, in writing to the Director of Engineering. |
| Incident Response Team (IRT) | The individuals who have been engaged and are actively working on the incident. All members of the IRT will remain engaged in incident response until the incident is formally resolved, or they are formally dismissed by the Incident Manager. |
| Engineers (Support and Development) | Qualified engineers will be placed into the on-call rotation and may act as the Incident Manager (if primary resources are not available) or a member of the IRT when engaged to respond to an incident. Engineers are responsible for understanding the technologies and components of the information systems, the security controls in place including logging, monitoring, and alerting tools, appropriate communications channels, incident response protocols, escalation procedures, and documentation requirements. When Engineers are engaged in incident response, they become members of the IRT. |
| Users | Employees and contractors of Mesh Intelligent Technologies, Inc.. Users are responsible for following policies, reporting problems, suspected problems, weaknesses, suspicious activity, and security incidents and events. |
| Customers | Customers are responsible for reporting problems with their use of Mesh Intelligent Technologies, Inc. services. Customers are responsible for verifying that reported problems are resolved. |
| Legal Counsel | Responsible, in conjunction with the CEO and executive management, for determining if an incident presents legal or regulatory exposure as well as whether an incident shall be considered a reportable breach. Counsel shall review and approve in writing all external breach notices before they are sent to any external party. |
| Executive Management | Responsible, in conjunction with the CEO and Legal Counsel, for determining if an incident shall be considered a reportable breach. An appropriate company officer shall review and approve in writing all external breach notices before they are sent to any external party. Mesh Intelligent Technologies, Inc. shall seek stakeholder consensus when determining whether a breach has occurred. The Mesh Intelligent Technologies, Inc. CEO shall make a final breach determination in the event that consensus cannot be reached. |

## Management Commitment

Management has approved this plan and commits to providing resources, tools, and training needed to respond to events and incidents that may adversely affect the company or its customers.

# Exceptions

Requests for an exception to this Policy must be submitted to and authorized by the IT Manager for approval. Exceptions shall be documented.

# Violations & Enforcement

Any known violations of this policy should be reported to the CEO. Violations of this policy may result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0 | 8-Mar-2023 | First Version | Mack Myers | Tsavo Knott |
| 1.1 | 15-Aug-2023 | Updated Communication Procedures based on lessons learned | Georgia Donmoyer | Mack Myers |

# Appendix A – Contact Information

Contacts for IT and Engineering Management as well as executive staff and can be found in the Team Roster.

# Appendix B – Incident Collection Form

| General Information |  |  |  |  |
| ----- | :---- | :---- | :---- | :---- |
| Incident Detector’s Information |  |  |  |  |
| Name: |  |  | Date and Time Detected:  |  |
| Title: |  |  |  |  |
| Phone: |  |  | Location Incident Detected From:  |  |
| E-mail: |  |  |  |  |
|  |  |  | Additional Information: |  |
|  |  |  |  |  |

| Incident Summary |  |  |  |  |
| ----- | :---- | :---- | :---- | :---- |
| Type of Incident Detected: |  |  |  |  |
| Denial of Service  | Unauthorized Use | Espionage | Probe | Hoax |
| Malicious Code | Unauthorized Access | Other: |  |  |
|  |  |  |  |  |
| Incident Location: |  |  |  |  |
| Site: |  |  |  |  |
| Site Point of Contact: |  |  |  |  |
| Phone: |  |  |  |  |
| Email: |  |  |  |  |
|  |  |  |  |  |
| How was the Incident Detected: |  |  |  |  |
|  |  |  |  |  |
| Additional Information: |  |  |  |  |
|  |  |  |  |  |

| Location(s) of affected systems: |  |  |  |  |
| :---- | :---- | ----- | ----- | :---- |
|  |  |  |  |  |
| Date and time incident handlers arrived at site: |  |  |  |  |
|  |  |  |  |  |
| Describe affected information system(s) (one form per system is recommended): |  |  |  |  |
| Hardware Manufacturer: |  |  |  |  |
| Serial Number:  |  |  |  |  |
| Corporate Property Number (if applicable): |  |  |  |  |
|  |  |  |  |  |
| Is the affected system connected to a network? |  | Yes | No |  |
|  |  |  |  |  |
| Describe the physical security of the location of affected information systems (locks, security alarms, building access, etc.): |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
| Isolate affected systems:  |  |  |  |  |
| Approval to removal from network?  |  | Yes | No |  |
| If YES, Name of Approver: |  |  |  |  |
| Date and Time Removed: |  |  |  |  |
| If NO, state the reason:  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
| Backup of Affected System(s): |  |  |  |  |
| Last System backup successful?  |  | Yes | No |  |
| Name of persons who did backup: |  |  |  |  |
|  |  |  |  |  |
| Date and time last backups started: |  |  |  |  |
| Date and time last backups completed: |  |  |  |  |
| Backup Storage Location:  |  |  |  |  |
|  |  |  |  |  |
| Incident Eradication: |  |  |  |  |
| Name of persons performing forensics: |  |  |  |  |
| Was the vulnerability (root cause) identified:  |  | Yes | No |  |
| Describe: |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
| How was eradication validated: |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

# Appendix C – HIPAA Breach Procedures for Protected Health Information (PHI)

If Mesh Intelligent Technologies, Inc. is acting as a Business Associate for a HIPAA-covered customer and identifies a potential breach of PHI, the following procedures apply.

## Procedures

### Step 1: Identification (Discovery)

A breach of PHI is deemed discovered on the first day Mesh knows of the breach or, by exercising reasonable diligence, would or should have known about it. Potential breaches must be reported immediately to the designated Security and/or Privacy Officer.

Provide all information available at the time of initial report, including names, dates, nature of PHI, manner of disclosure, employees involved, recipients, other persons with knowledge, and any associated documentation.

### Step 2: Investigation and Step 3: Risk Assessment

The designated Security and/or Privacy Officer promptly investigates and performs a risk assessment to determine whether the use or disclosure of PHI constitutes a breach and requires notification.

### Step 4: Final Determination and Step 5: Notification

Executive Management with Legal Counsel has final authority to determine whether a breach of PHI occurred and whether notification is warranted. Notices are sent to Covered Entities without unreasonable delay and no later than 60 days after discovery, subject to law enforcement delay exceptions.

All phases are documented and retained according to record retention requirements (≥ six years where applicable).

# Appendix D – Google Cloud Root Account Compromise Playbook

## Objective

Provide specific guidance to manage suspected compromise of a Google Cloud root or organization-level administrator account.

## Assumptions

- gcloud CLI installed and configured for break-glass admin
- Reporting and on-call process in place
- Security Command Center and Audit Logs enabled

## Indicators of Compromise (examples)

- Unexpected IAM role grants or policy changes (e.g., Owner on critical projects)
- Admin Activity or Data Access logs disabled or tampered
- Sudden creation of service accounts or keys; unusual key usage
- Org Policies modified to weaken controls

## Steps to Remediate – Establish Control

1. Initiate incident bridge; assign Incident Manager
2. Suspend or revoke suspected user sessions via Google Workspace Admin; force password reset and require MFA re-enrollment
3. Remove anomalous IAM bindings (prefer group-based bindings); reapply baseline policies and Org Policies (Deny/Constraints)
4. Disable or rotate compromised service account keys; prefer Workload Identity Federation
5. Verify Cloud Audit Logs are enabled and immutable retention is in place; export logs if needed for preservation
6. Review recent Admin Activity; enumerate privilege grants, project/org changes, and network/security config changes
7. Rotate credentials for affected resources (secrets, API keys); invalidate tokens
8. Engage Google Cloud Support if platform assistance is required
9. Close incident when containment and remediation complete; perform RCA and hardening actions


