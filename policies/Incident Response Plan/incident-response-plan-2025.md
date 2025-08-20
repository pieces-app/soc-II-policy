---
title: Incident Response Plan
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
stakeholders:
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Mark Widman (Chief Technology Officer)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Sam Jones (Chief AI Officer)
  - Georgia Donmoyer (GRC)
  - Tsavo Knott (CEO)
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC7.2, CC7.3, CC7.4, CC7.5, CC6.6, CC6.8
    - ISO/IEC 27001 Annex A: A.5.24-A.5.30 (Information security incident management)
  procedures:
    - Incident Response Runbooks (Appendix D-F)
    - Evidence Collection & Preservation Procedure
    - Breach Notification Procedure
  controls:
    - Google Cloud Security Command Center, GitHub Advanced Security, Sentry, Vanta
repo: https://github.com/pieces-app/soc-II-policy
---

# **Incident Response Plan**

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))

**Effective Date:** August 19, 2025

# **Purpose** 

This document establishes the plan for managing information security incidents and events, and offers guidance for employees or incident responders who believe they have discovered, or are responding to, a security incident.

# **Scope** 

This plan covers all information security or data privacy events or incidents affecting Mesh Intelligent Technologies, Inc. systems, data, personnel, customers, and facilities, including:
- Cloud infrastructure (Google Cloud Platform)
- Development and repository systems (GitHub)
- SaaS applications and integrations
- Customer data and services
- Employee devices and access

# **Incident and Event Definitions**

- **Security Event**: An observable occurrence relevant to the confidentiality, availability, integrity, or privacy of company-controlled data, systems, or networks.
- **Security Incident**: A security event that results in actual or potential loss or damage to the confidentiality, availability, integrity, or privacy of company-controlled data, systems, or networks.
- **Data Breach**: A security incident that results in unauthorized access to or disclosure of personal data or confidential information.

# **Incident Reporting & Documentation**

## **Reporting** 

If a Mesh Intelligent Technologies, Inc. employee, contractor, user, or customer becomes aware of an information security event or incident, possible incident, imminent incident, unauthorized access, policy violation, security weakness, or suspicious activity, they shall immediately report the information using one of the following communication channels:

**Primary Channels:**
- Email security@pieces.app for security-specific incidents
- Email support@pieces.app for general incidents or issues
- Emergency Security Hotline (24/7 for critical incidents): (513) 572-3339
- Internal Slack channel: #security-incidents (for employees)

Reporters should act as a good witness and behave as if they are reporting a crime. Reports should include specific details about what has been observed or discovered, including:
- Date and time of observation
- Systems or data affected
- Nature of the activity
- Any error messages or unusual behavior
- Screenshots or other evidence if available

## **Severity Classification**

The Incident Response Team (IRT) shall monitor incident and event reports and assign severity based on the following categories:

### **S4 - Low Severity**
Minimal impact issues or potential security improvements. Examples:
- Policy violations with no data exposure
- Failed phishing attempts (reported, not clicked)
- Minor configuration issues
- Security awareness questions

**Response Time**: Within 2 business days

### **S3 - Medium Severity**
Suspicions or odd behaviors requiring investigation. No immediate risk identified. Examples:
- Lost/stolen laptop with full-disk encryption enabled
- Suspicious emails (unopened)
- Unusual but explainable system activity
- Non-critical service degradation

**Response Time**: Within 1 business day

### **S2 - High Severity**
Likely threats or elevated risk scenarios where exploitation hasn't been confirmed but is probable. Examples:
- Lost/stolen laptop without encryption
- Critical vulnerabilities with exploit code available
- Suspected malware or persistence mechanisms
- Unauthorized access attempts to sensitive systems
- Compromise of non-privileged user account
- Data exposure risk without confirmed breach

**Response Time**: Within 4 hours

### **S1 - Critical Severity**
Active exploitation, confirmed breaches, or threats to physical safety. Examples:
- Confirmed data breach or exfiltration
- Active ransomware or destructive malware
- Compromise of administrative or privileged accounts
- Customer data exposure
- Threats to personal safety
- Complete service outage affecting customers

**Response Time**: Immediate (within 1 hour)

## **Escalation and Internal Reporting**

Incident escalation follows severity-based procedures:

### **S1 - Critical Severity**
1. Immediate notification to CEO, CTO, and Head of Cloud Infrastructure via phone/SMS
2. Open incident bridge (Slack huddle or video call)
3. Create incident ticket in tracking system
4. Designate Incident Manager
5. Activate on-call rotation if outside business hours

### **S2 - High Severity**
1. Create incident ticket
2. Notify appropriate manager and on-call engineer via Slack
3. Tag @incident-response in #security-incidents channel
4. Escalate to S1 if evidence of active exploitation found

### **S3/S4 - Medium and Low Severity**
1. Create ticket in incident tracking system
2. Assign to appropriate team for investigation
3. Update ticket with findings within SLA

**Escalation Contacts**: See Appendix A for current escalation roster

## **Documentation Requirements**

All security events, incidents, and response activities shall be documented in GitHub Issues (primary tracking) and Google Docs (post-mortem documentation) with:

- Incident timeline (detection through resolution)
- Affected systems and data classification
- Impact assessment (actual and potential)
- Response actions taken
- Evidence collected and preserved
- Communication log
- Lessons learned

**Incident Tracking Process**:
- GitHub Issue created with highest priority label
- Google Chat Space created for incident coordination
- Google Calendar recurring meeting scheduled until resolution
- Post-mortem Google Doc created for analysis

**Root Cause Analysis (RCA)**:
- Required for all S1 incidents
- Recommended for S2 incidents with actual impact
- RCA documented in post-mortem Google Doc
- Post-mortem meeting scheduled with team for review
- Action items tracked in GitHub Issues

# **Incident Response Process**

## **Response Phases**

The IRT follows the NIST incident response lifecycle:

### **1. Preparation**
- Maintain incident response capabilities
- Conduct training and tabletop exercises
- Ensure tools and access are ready
- Review and update playbooks

### **2. Detection & Analysis**
- Event reported or detected via monitoring
- Triage and initial assessment
- Severity classification
- Impact analysis
- Evidence collection

### **3. Containment, Eradication & Recovery**
- Short-term containment (isolate affected systems)
- Evidence preservation
- Eradication (remove threat)
- System recovery and validation
- Long-term containment (temporary controls)

### **4. Post-Incident Activity**
- Root cause analysis
- Lessons learned documentation
- Process improvements
- Control enhancements
- Stakeholder reporting

## **Incident Response Team Structure**

### **Core IRT Roles**
- **Incident Manager (IM)**: Overall incident coordination and decision-making
- **Technical Lead**: Technical response and investigation
- **Communications Lead**: Internal and external communications
- **Legal/Compliance Lead**: Regulatory and legal requirements

### **Extended Team** (activated as needed)
- Engineering teams (by affected system)
- Customer Success (for customer impact)
- HR (for insider threats)
- External forensics or consultants

## **War Room Operations**

For S1 and complex S2 incidents:

1. **Virtual War Room**: 
   - Google Chat Space for incident coordination
   - Google Meet bridge for real-time discussion
   - Slack channel (#incident-YYYY-MM-DD-XXX) for async updates
2. **Documentation**: Post-mortem Google Doc shared with team
3. **Status Updates**: Every 2 hours or at significant milestones
4. **Shift Handoffs**: For incidents exceeding 8 hours
5. **Recurring Meetings**: Google Calendar events until incident resolved

## **Incident Response Meeting Cadence**

- **S1 Incidents**: Continuous bridge with hourly status updates
- **S2 Incidents**: Every 4 hours until contained
- **S3/S4 Incidents**: Daily check-ins until resolved

### **Standard Agenda**
1. Current status and timeline update
2. New findings and IOCs
3. Impact assessment update
4. Containment and mitigation actions
5. Recovery progress
6. External communication needs
7. Next steps and owner assignments
8. Decision points requiring approval

# **Special Incident Scenarios**

## **Insider Threats**

When the threat actor is an internal employee, contractor, or partner:

1. Restrict information to strict need-to-know basis
2. IM contacts CEO and Legal Counsel directly
3. Coordinate with HR for employment actions
4. Preserve evidence for potential legal action
5. Consider engaging external forensics
6. Review and revoke all access immediately

## **Compromised Communications**

If internal communication channels are suspected compromised:

1. Switch to predetermined out-of-band channels
2. Use phone/SMS for critical communications
3. Establish alternate collaboration platform
4. Document all communications offline
5. Consider air-gapped systems for sensitive analysis

## **Supply Chain Incidents**

For incidents involving third-party services or dependencies:

1. Assess impact on Mesh systems and data
2. Coordinate with vendor security teams
3. Review contractual obligations
4. Implement compensating controls
5. Notify affected customers if required

## **AI/LLM Provider Incidents**

For incidents involving AI providers (OpenAI, Anthropic, Google):

1. Models run on edge devices - limited cloud exposure
2. For cloud LLM issues:
   - Defer to provider's incident response
   - Assess any data sent to provider APIs
   - Review provider's incident notification
   - Communicate impact to affected users
3. Nano-models on edge have no cloud dependency
4. No model training on customer data - no poisoning risk

## **Ransomware Response**

Specific procedures for ransomware incidents:

1. Immediate isolation of affected systems
2. Determine scope and variant identification
3. Engage law enforcement (FBI IC3)
4. Assess backup viability
5. Do not pay ransom without executive and legal approval
6. Coordinate with cyber insurance carrier

# **Evidence Collection & Forensics**

## **Evidence Handling**

Follow chain of custody procedures:

1. Document all evidence collection
2. Create forensic images before analysis
3. Maintain evidence integrity (hashing)
4. Secure storage of evidence
5. Limited access with audit trail

## **Forensic Capabilities**

- **Cloud Forensics**: GCP snapshot capabilities, Cloud Logging exports
- **Endpoint Forensics**: Memory dumps, disk imaging
- **Network Forensics**: Packet captures, flow logs
- **Application Forensics**: Application logs, database audit trails

Reference NIST SP 800-86 "Guide to Integrating Forensic Techniques into Incident Response"

# **External Communications and Breach Reporting**

## **Breach Determination**

Breach determination requires consensus between:
- CEO (final authority)
- Legal Counsel
- Head of Cloud Infrastructure
- Chief Product Officer

## **Notification Requirements**

### **Customer Notification**
- **Timeline**: Within 24 hours of confirming impact to customer data
- **Method**: Email to registered contact and in-app notification
- **Content**: Nature of incident, data affected, actions taken, recommendations

### **Regulatory Notifications**

| Authority | Requirement | Timeline | Method |
| :---- | :---- | :---- | :---- |
| GDPR (EU) | Data Protection Authorities | Within 72 hours | Online form |
| CCPA (California) | Attorney General | Without unreasonable delay | Online submission |
| State Breach Laws | Various state AGs | Varies (typically 30-60 days) | Written notice |
| HIPAA (if applicable) | HHS and affected individuals | Within 60 days | OCR portal |

### **Other Stakeholders**

| Stakeholder | Trigger | Timeline | Method |
| :---- | :---- | :---- | :---- |
| Cyber Insurance | Any incident with potential claim | Within 24 hours | Phone + written (carrier on file) |
| Law Enforcement | Criminal activity suspected | Immediate | Phone (FBI IC3) |
| Media/Press | Major breach or public impact | Per Legal/CEO decision | Press release |
| Partners/Vendors | Their data affected | Within 48 hours | Direct contact |

## **Communication Restrictions**

- No personnel may communicate about incidents externally without approval from Legal and CEO
- All external communications must be reviewed by Legal Counsel
- Designated spokesperson for media inquiries (CEO or delegate)
- Internal communications follow need-to-know principle

# **Recovery and Remediation**

## **System Recovery**

1. Verify threat eradication
2. Restore from clean backups (RPO: 24 hours)
3. Apply all security patches
4. Implement additional controls
5. Enhanced monitoring period (30 days)
6. Gradual service restoration with validation

## **Remediation Actions**

Short-term (immediate):
- Patch vulnerabilities
- Reset compromised credentials
- Block malicious IPs/domains
- Isolate affected systems

Long-term (within 30 days):
- Architecture improvements
- Policy updates
- Process enhancements
- Training and awareness
- Tool deployment

# **Testing and Improvement**

## **Testing Requirements**

- **Tabletop Exercises**: Quarterly for IRT members
- **Technical Drills**: Semi-annually (simulated incidents)
- **Full IR Test**: Annually with external participation
- **Playbook Reviews**: After each incident and annually

## **Continuous Improvement**

- Post-incident lessons learned (within 5 business days)
- Quarterly IR metrics review
- Annual plan update
- Industry threat intelligence integration
- Regulatory requirement updates

## **Metrics and Reporting**

Track and report quarterly:
- Mean Time to Detect (MTTD)
- Mean Time to Respond (MTTR)
- Mean Time to Contain (MTTC)
- Mean Time to Recover (MTTR)
- Incidents by severity and type
- False positive rate

# **Roles & Responsibilities**

| Role | Responsibility |
| :---- | :---- |
| **Incident Manager** | Primary decision-maker during response. Coordinates team, communicates status, drives resolution, assigns follow-up, triggers breach assessment. Reports to CEO for S1 incidents. |
| **Incident Response Team (IRT)** | Technical responders actively working the incident. Remain engaged until formal resolution or dismissal by IM. |
| **Engineers (On-Call)** | Serve as first responders, may act as IM if primary unavailable. Must understand systems, monitoring tools, communication channels, and documentation requirements. |
| **Security Team** | Lead technical investigation, threat hunting, and forensics. Maintain security tools and threat intelligence. |
| **Legal Counsel** | Determine legal/regulatory requirements, approve external notices, coordinate with law enforcement, manage legal privilege. |
| **Executive Management** | Approve major decisions, external communications, and resource allocation. CEO makes final breach determination. |
| **All Employees** | Report suspicious activity, follow security policies, cooperate with investigations, maintain confidentiality. |
| **Customers** | Report security concerns, verify issue resolution, follow provided guidance during incidents. |

# **Management Commitment**

Mesh Intelligent Technologies, Inc. management has approved this plan and commits to providing the resources, tools, training, and support needed to maintain effective incident response capabilities and protect company and customer interests.

# **Exceptions**

Requests for exceptions to this plan must be submitted to the Head of Cloud Infrastructure and approved by the CEO. Exceptions must be documented, time-bound, and include compensating controls.

# **Violations & Enforcement**

Known violations should be reported to security@pieces.app or the CEO. Violations may result in immediate suspension of privileges and/or disciplinary action up to and including termination.

## **Compliance & Audit**

- Annual review by GRC function
- SOC 2 audit verification
- Regulatory compliance validation
- Customer audit support as required

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0 | 8-Mar-2023 | First Version | Mack Myers | Tsavo Knott |
| 1.1 | 15-Aug-2023 | Updated Communication Procedures based on lessons learned | Georgia Donmoyer | Mack Myers |
| 1.2 | 19-Aug-2025 | Major refresh: Enhanced severity model, 24-hour customer notification, forensics procedures, comprehensive playbooks, aligned with LEGAL_POLICY_2025 | Executive Leadership | Tsavo Knott (CEO) |

## **References**

- NIST SP 800-61r2: Computer Security Incident Handling Guide
- NIST SP 800-86: Guide to Integrating Forensic Techniques
- ISO/IEC 27035: Information Security Incident Management
- LEGAL_POLICY_2025_COUNSEL_VERIFIED: Customer notification and forensic requirements
- Business Continuity and Disaster Recovery Plan: Recovery objectives and procedures
- Access Control Policy: Emergency access procedures

# **Appendix A – Contact Information**

Emergency contacts and escalation roster maintained in:
- Google Workspace Contacts (shared group)
- GitHub Issues with @mentions for priority alerts
- Emergency Hotline: (513) 572-3339
- All employee contact info (phone, WhatsApp, Signal) in secure shared doc

Key Contacts:
- CEO: Tsavo Knott
- CTO: Mark Widman  
- Head of Cloud Infrastructure: Hiro Tamada
- CPO/Security: Mack Myers
- Legal: External Counsel (contact via CEO/CPO)
- Investors: For FBI/Secret Service connections (via CEO)

# **Appendix B – Incident Report Form**

## **Initial Report Information**

| Field | Details |
| :---- | :---- |
| Report Date/Time | |
| Reporter Name | |
| Reporter Contact | |
| Detection Method | |
| Initial Severity Assessment | |

## **Incident Details**

| Field | Details |
| :---- | :---- |
| Incident Type | ☐ Malware ☐ Unauthorized Access ☐ DoS ☐ Data Breach ☐ Insider ☐ Other |
| Systems Affected | |
| Data Classification | ☐ Public ☐ Internal ☐ Confidential ☐ Restricted |
| User Impact | |
| Business Impact | |

## **Technical Information**

| Field | Details |
| :---- | :---- |
| IP Addresses | |
| Domains/URLs | |
| File Hashes | |
| User Accounts | |
| Timeline | |
| IOCs | |

## **Response Actions**

| Field | Details |
| :---- | :---- |
| Containment Actions | |
| Evidence Collected | |
| Systems Isolated | |
| Notifications Made | |

# **Appendix C – HIPAA Breach Procedures**

*[Applicable only for Business Associate relationships]*

If Mesh Intelligent Technologies, Inc. processes Protected Health Information (PHI) as a Business Associate:

## **Discovery and Assessment**
- Breach "discovered" when known or reasonably should have known
- Immediate notification to Security Officer
- Risk assessment per HIPAA requirements

## **Notification Requirements**
- Covered Entity: Within 60 days of discovery
- Include all required HIPAA breach notification elements
- Maintain documentation for 6 years minimum

## **Risk Assessment Factors**
1. Nature and extent of PHI involved
2. Unauthorized person who accessed PHI
3. Whether PHI was acquired or viewed
4. Extent of risk mitigation

# **Appendix D – Google Cloud Incident Response Playbook**

## **Preparation**
- Enable Cloud Audit Logs (Admin, Data Access, System Events)
- Configure Security Command Center
- Set up Cloud Logging exports to secure bucket
- Maintain break-glass admin account

## **Detection Indicators**
- Unexpected IAM changes (especially Owner/Editor roles)
- Audit log tampering or disabling
- Unusual API activity or quotas
- New service accounts or keys
- Firewall or network changes
- Compute instance creation in new regions

## **Containment Actions**

### **Immediate Actions**
1. **Suspend Compromised Identities**
   ```
   gcloud auth revoke [USER_EMAIL]
   gcloud projects remove-iam-policy-binding [PROJECT_ID] \
     --member="user:[USER_EMAIL]" --role="[ROLE]"
   ```

2. **Rotate Service Account Keys**
   ```
   gcloud iam service-accounts keys list --iam-account=[SA_EMAIL]
   gcloud iam service-accounts keys delete [KEY_ID] --iam-account=[SA_EMAIL]
   ```

3. **Enable VPC Service Controls** (if not already)
   - Create security perimeter
   - Restrict data exfiltration

4. **Snapshot Critical Systems**
   ```
   gcloud compute disks snapshot [DISK_NAME] --snapshot-names=[SNAPSHOT_NAME]
   ```

### **Investigation**
- Review Cloud Audit Logs for unauthorized actions
- Check for new or modified resources
- Analyze network flow logs
- Review Cloud Storage access logs
- Check for data exfiltration indicators

### **Recovery**
1. Remove unauthorized IAM bindings
2. Delete compromised resources
3. Restore from clean backups
4. Re-enable security controls
5. Enhanced monitoring for 30 days

## **Google Cloud Support Escalation**
- Premium Support: Available 24/7
- Critical priority for security incidents
- Request GCP incident response assistance

# **Appendix E – GitHub Security Incident Playbook**

## **Preparation**
- Enable GitHub Advanced Security
- Configure audit log streaming
- Maintain admin account inventory
- Document repository sensitivity

## **Detection Indicators**
- Unauthorized repository access
- Secret scanning alerts
- Unusual commit patterns
- Branch protection bypasses
- OAuth app authorizations
- Webhook modifications

## **Response Actions**

### **Account Compromise**
1. Reset user password via GitHub Enterprise
2. Revoke all personal access tokens
3. Review and remove SSH keys
4. Audit recent commits and actions
5. Review organization and repository permissions

### **Repository Compromise**
1. Enable temporary repository freeze
2. Review commit history for malicious changes
3. Scan for exposed secrets
4. Verify branch protections
5. Audit webhook and integration configurations

### **Secret Exposure**
1. Immediately rotate exposed credentials
2. Review secret access logs
3. Determine exposure window
4. Assess potential unauthorized usage
5. Implement additional secret scanning rules

## **Recovery Steps**
1. Revert malicious commits if found
2. Re-enable branch protections
3. Require code review for sensitive repositories
4. Implement signed commits
5. Enhanced audit logging

# **Appendix F – Data Breach Response Checklist**

## **Hour 1-4: Immediate Response**
☐ Activate IRT and designate IM  
☐ Open incident bridge  
☐ Begin evidence preservation  
☐ Implement immediate containment  
☐ Start incident documentation  
☐ Notify CEO and Legal  

## **Hour 4-24: Assessment**
☐ Determine scope of breach  
☐ Identify affected data and individuals  
☐ Assess regulatory requirements  
☐ Engage external resources if needed  
☐ Prepare for customer notification  
☐ Contact cyber insurance  

## **Day 1-3: Notification**
☐ Finalize breach determination  
☐ Prepare notification content  
☐ Legal review of notifications  
☐ Send customer notifications (24hr target)  
☐ Submit regulatory notifications  
☐ Prepare FAQ and support responses  

## **Day 3-7: Remediation**
☐ Complete eradication  
☐ Implement additional controls  
☐ Begin recovery operations  
☐ Continue monitoring  
☐ Provide customer updates  

## **Day 7-30: Follow-up**
☐ Complete root cause analysis  
☐ Conduct lessons learned  
☐ Implement long-term fixes  
☐ Update security controls  
☐ Provide final report  
☐ Review and update IR plan  

# **Appendix G – Alert Investigation Procedures**

## **Sentry Alert Investigation**

### **Initial Response**
1. **Identify Source**: Determine which service/application triggered the alert
2. **Check Error Rate**: Review error frequency and affected users
3. **Review Stack Trace**: Analyze error details and patterns
4. **Check Related Services**: Verify dependent service health

### **Escalation Decision**
- **Error spike > 100/min**: Escalate to S2
- **Authentication errors**: Check for potential security issue
- **Database connection failures**: Check GCP status
- **Memory/resource exhaustion**: Review for potential DoS

### **Investigation Path**
1. Sentry → Identify service and error pattern
2. Google Cloud Logging → Check infrastructure logs
3. BigQuery → Query impact on customers
4. GitHub → Review recent deployments

## **Google Cloud Security Alert Investigation**

### **Security Command Center Alerts**
1. **Review Finding**: Assess severity and affected resources
2. **Verify Configuration**: Check if intentional change
3. **Check Audit Logs**: Review who made changes and when
4. **Assess Impact**: Determine data/service exposure

### **Common Alert Types**
- **Public Storage Buckets**: Immediate remediation required
- **Excessive Permissions**: Review IAM bindings
- **Unused Service Accounts**: Disable if confirmed unused
- **API Key Exposure**: Rotate immediately
- **Firewall Rules**: Verify business justification

### **Investigation Workflow**
1. Security Command Center → Finding details
2. Cloud Asset Inventory → Resource configuration
3. Cloud Audit Logs → Change history
4. Cloud Monitoring → Resource metrics
5. BigQuery audit logs → Detailed analysis

## **GitHub Advanced Security Alert Investigation**

### **Secret Scanning Alerts**
1. **Immediate Actions**: 
   - Assume compromised
   - Rotate secret immediately
   - Check secret usage logs
2. **Investigation**:
   - Review commit history
   - Check if pushed to public repo
   - Verify secret was active
3. **Remediation**:
   - Remove from git history if needed
   - Update secret management practices

### **Dependabot Security Alerts**
1. **Assess Severity**: Critical/High require immediate attention
2. **Check Exposure**: Is vulnerable code in production?
3. **Review Fix**: Is patch available?
4. **Test & Deploy**: Validate fix doesn't break functionality

### **Code Scanning Alerts**
1. **Triage**: Review CodeQL findings
2. **Validate**: Confirm if true positive
3. **Prioritize**: Based on exploitability
4. **Fix**: Implement secure coding fix

## **Metrics Dashboard Investigation**

### **Abuse Detection (BigQuery/Metabase)**
1. **Check Dashboards**:
   - API abuse metrics in Metabase
   - Usage anomaly detection
   - Geographic distribution
2. **Deep Dive in BigQuery**:
   ```sql
   SELECT user_id, COUNT(*) as request_count, 
          COUNT(DISTINCT ip_address) as unique_ips
   FROM api_logs
   WHERE timestamp > TIMESTAMP_SUB(CURRENT_TIMESTAMP(), INTERVAL 1 HOUR)
   GROUP BY user_id
   HAVING request_count > 10000
   ORDER BY request_count DESC
   ```
3. **Cross-Reference**:
   - Descope for authentication anomalies
   - Segment for user behavior patterns
   - Sentry for correlated errors

### **Customer Impact Analysis**
Using BigQuery data lakes:
```sql
-- Identify affected customers
SELECT DISTINCT user_id, email, last_activity
FROM user_telemetry
WHERE resource_id IN (
  SELECT resource_id 
  FROM incident_affected_resources
  WHERE incident_id = 'INC-2025-001'
)
```

## **Communication Fallback Procedures**

### **Primary Channels Down**
If Slack and email are unavailable:

1. **Immediate**: SMS/Phone calls to IRT members
2. **Group Coordination**:
   - WhatsApp group (pre-established)
   - Signal group (for sensitive discussions)
   - iMessage for Apple users
   - Google Chat Spaces via mobile
3. **Documentation**: 
   - Local notes, transfer to systems when restored
   - Screenshots and timestamps critical

### **Contact Priority**
1. CEO: [Phone]
2. CTO: [Phone]
3. Head of Cloud Infrastructure: [Phone]
4. On-call engineer: Via GitHub Issues mobile app

# **Appendix H – Device Loss/Theft Procedures**

## **Immediate Actions (Within 1 Hour)**

### **Employee Responsibilities**
1. **Report immediately** to security@pieces.app and manager
2. **Provide details**:
   - Device type and identifier
   - Last known location
   - Circumstances of loss/theft
   - Data stored locally
   - Encryption status
3. **File police report** if theft
4. **Attempt remote wipe** if configured

### **Security Team Actions**
1. **Verify device inventory** and configuration
2. **Revoke access**:
   - Google Workspace session termination
   - GitHub access revocation
   - VPN certificates disabled
   - API keys rotated
3. **Check recent activity**:
   - Last login times
   - Data access patterns
   - Download history

## **Assessment (Within 4 Hours)**

### **Risk Evaluation**
- **Encrypted**: Lower risk, monitor for access attempts
- **Unencrypted**: High risk, assume data compromised
- **Cached credentials**: Rotate all potentially stored secrets
- **Customer data**: Assess exposure and notification requirements

### **Containment Actions**
1. **Password reset** for all accounts
2. **MFA re-enrollment** required
3. **Certificate revocation** for device
4. **Monitor for unauthorized access** (30 days enhanced)

## **Recovery (Within 24 Hours)**

### **Device Replacement**
1. **New device provisioning** per IT standards
2. **Security hardening**:
   - Full disk encryption mandatory
   - MDM enrollment
   - Endpoint protection
3. **Access restoration** after security verification

### **Lessons Learned**
- Document in incident report
- Review security controls
- Update device policies if needed
- Employee security awareness reminder

## **Preventive Measures**

### **Technical Controls**
- **Mandatory encryption**: FileVault (Mac), BitLocker (Windows)
- **Remote wipe capability**: MDM or built-in OS features
- **Automatic lock**: 5-minute timeout
- **Find My Device**: Enabled and tested

### **Administrative Controls**
- **Device inventory**: Maintained in asset management
- **Quarterly attestation**: Employees confirm device security
- **Travel guidance**: Extra precautions for international travel
- **Clean desk policy**: Lock devices when unattended

### **Physical Security Best Practices**
- Never leave devices in vehicles
- Use privacy screens in public
- Cable locks for office use
- Separate device from sensitive documents
- Use company-approved bags with security features

# **Appendix I – Incident Severity Examples**

## **S1 - Critical (Immediate Response)**
- Confirmed ransomware encryption of production systems
- Customer database breach with PII/payment data exposed
- Admin account compromise with active abuse
- Complete production outage affecting all customers
- Confirmed data exfiltration by malicious actor
- Physical security threat to personnel

## **S2 - High (4-hour Response)**
- Critical vulnerability discovered in production (e.g., Log4j, Heartbleed)
- Suspicious admin account activity without confirmed compromise
- Malware detected but contained to single system
- Partial service degradation affecting subset of customers
- Lost unencrypted laptop with access to sensitive systems
- Failed attempt to access production databases

## **S3 - Medium (1 business day)**
- Phishing email reported by multiple employees
- Unusual network traffic patterns requiring investigation
- Non-critical service degradation
- Security tool alerts requiring validation
- Policy violation without data exposure

## **S4 - Low (2 business days)**
- Generic phishing attempts
- Security improvement recommendations
- False positive alerts
- Documentation updates needed
- Security awareness questions
