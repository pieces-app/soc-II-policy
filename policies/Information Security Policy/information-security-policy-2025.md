---
title: Information Security Policy
owner:
  - Mack Myers (Corporate Secretary & CPO, Policy Owner)
  - Katie Storm (AirCFO - HR, Co-Owner)
stakeholders:
  - Mark Widman (Chief Technology Officer)
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Sam Jones (Chief AI Officer)
  - Legal Counsel
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 Type II
    - ISO/IEC 27001
    - NIST Cybersecurity Framework
  procedures:
    - All security-related policies
repo: https://github.com/pieces-app/soc-II-policy
---

# Information Security Policy

**Policy Owner:** Mack Myers (Corporate Secretary & CPO), Katie Storm (AirCFO - HR)

**Effective Date:** August 19, 2025

# Overview

This Information Security Policy is intended to protect Mesh Intelligent Technologies, Inc.'s employees, partners and the company from illegal or damaging actions by individuals, either knowingly or unknowingly.

Internet/Intranet/Extranet-related systems, including but not limited to computer equipment, software, operating systems, storage media, network accounts providing electronic mail, web browsing, and file transfers, are the property of Mesh Intelligent Technologies, Inc. These systems are to be used for business purposes in serving the interests of the company, and of our clients and customers in the course of normal operations.

Effective security is a team effort involving the participation and support of every Mesh Intelligent Technologies, Inc. employee or contractor who deals with information and/or information systems. It is the responsibility of every team member to read and understand this policy, and to conduct their activities accordingly.

Our security program is designed to meet SOC 2 Type II requirements and aligns with ISO 27001 and NIST Cybersecurity Framework standards. We maintain continuous compliance monitoring through Vanta and implement a zero-trust security architecture.

# Purpose

The purpose of this policy is to communicate our information security policies and outline the acceptable use and protection of Mesh Intelligent Technologies, Inc.'s information and assets. These rules are in place to protect customers, employees, and Mesh Intelligent Technologies, Inc. Inappropriate use exposes Mesh Intelligent Technologies, Inc. to risks including virus attacks, compromise of network systems and services, financial and reputational risk, and legal and compliance issues.

The Mesh Intelligent Technologies, Inc. "Information Security Policy" is comprised of this policy and all Mesh Intelligent Technologies, Inc. policies referenced and/or linked within this document.

# Scope

This policy applies to the use of information, electronic and computing devices, and network resources to conduct Mesh Intelligent Technologies, Inc. business or interact with internal networks and business systems, whether owned or leased by Mesh Intelligent Technologies, Inc., the employee, or a third party. All employees, contractors, consultants, temporary, and other workers at Mesh Intelligent Technologies, Inc. and its subsidiaries are responsible for exercising good judgment regarding appropriate use of information, electronic devices, and network resources in accordance with Mesh Intelligent Technologies, Inc. policies and standards, and local laws and regulations.

This policy applies to employees, contractors, consultants, temporaries, and other workers at Mesh Intelligent Technologies, Inc., including all personnel affiliated with third parties. This policy applies to all Mesh Intelligent Technologies, Inc.-controlled company and customer data as well as all equipment, systems, networks and software owned or leased by Mesh Intelligent Technologies, Inc.

# Security Incident Reporting

All users are required to report known or suspected security events or incidents, including policy violations and observed security weaknesses. Incidents shall be reported immediately or as soon as possible by sending an email to: security@pieces.app or help@pieces.app.

In your email please describe the incident or observation along with any relevant details. For critical security incidents, use our 24/7 security hotline: (513) 572-3339.

# Whistleblower Anonymous Fraud Reporting

Our Whistleblower Policy is intended to encourage and enable employees and others to raise serious concerns internally so that we can address and correct inappropriate conduct and actions. It is the responsibility of all employees to report concerns about violations of our code of ethics or suspected violations of law or regulations that govern our operations.

It is contrary to our values for anyone to retaliate against any employee who in good faith reports an ethics violation, or a suspected violation of law, such as a complaint of discrimination, or suspected fraud, or suspected violation of any regulation. An employee who retaliates against someone who has reported a violation in good faith is subject to discipline up to and including termination of employment.

Anonymous reports may be submitted via our anonymous reporting channel or directly to Legal Counsel.

# Mobile Device Policy

All end-user devices (e.g., mobile phones, tablets, laptops, desktops) must comply with this policy. Employees must use extreme caution when opening email attachments received from unknown senders, which may contain malware.

System level and user level passwords must comply with the Access Control Policy. Providing access to another individual, either deliberately or through failure to secure a device is prohibited.

All end-user, personal (BYOD) or company owned devices used to access Mesh Intelligent Technologies, Inc. information systems (i.e. email) must adhere to the following rules and requirements:

- Devices must be locked with a password (or equivalent control such as biometric) protected screensaver or screen lock after 5 minutes of non-use
- Devices must be locked whenever left unattended
- Users must report any suspected misuse or theft of a mobile device immediately to Mesh Intelligent Technologies, Inc.'s Engineering Department or security@pieces.app (within 2 hours of discovery)
- Confidential information must not be stored on mobile devices or USB drives (this does not apply to business contact information, e.g., names, phone numbers, and email addresses)
- Any mobile device used to access company resources (such as file shares and email) must not be shared with any other person
- Upon termination users agree to return all company owned devices and delete all company information and accounts from any personal devices
- All devices must have full-disk encryption enabled (FileVault for macOS, BitLocker for Windows)
- Mobile Device Management (MDM) enrollment is required for devices accessing Restricted/Confidential data
- Security patches must be applied within defined timelines (critical: ≤72 hours, high: ≤7 days, medium: ≤30 days)

# Clear Screen Clear Desk Policy

Users shall not leave confidential materials unsecured on their desk or workspace, and will ensure that screens are locked when not in use.

# Remote Working and Access Policy

Remote working refers to any situation where organizational personnel operate from locations outside the office. This includes teleworking, telecommuting, flexible workplace, virtual work environments, and remote maintenance. Laptops and other computer resources that are used to access the Mesh Intelligent Technologies, Inc. network must conform to the security requirements outlined in Mesh Intelligent Technologies, Inc.'s Information Security Policies and adhere to the following standards:

- Company rules shall be followed while working remote including clear desk protocols, printing, disposal of assets, and information security event reporting to prevent mishandling or accidental exposure of sensitive information
- To ensure mobile devices do not connect a compromised device to the company network, Antivirus policies require the use and enforcement of client-side antivirus software
- Antivirus software must be configured to detect and prevent or quarantine malicious software, perform periodic system scans, and have automatic updates enabled
- Mandate the use of VPN when transmitting confidential information over public Wi-Fi to prevent potential eavesdropping or man-in-the-middle attacks
- When working from a home network, ensure that the default wifi settings are changed, such as name, password and admin access
- For system administrators, it is advised to set up a work specific network with strong WPA3 encryption or at least WPA2 with robust password, together with, if supported, setting up a dedicated VLAN. Additionally, WPS (Wi-Fi Protected Setup) and UPnP (Universal Plug and Play) should be disabled if not specifically required
- Users must not connect to any outside network without a secure, up-to-date software firewall configured on the mobile computer
- Users are prohibited from changing or disabling any organizational security controls such as personal firewalls, antivirus software on systems used to access Mesh Intelligent Technologies, Inc. resources
- Use of remote access software and/or services (e.g., VPN client) is allowable as long as it is provided by the company and configured for multifactor authentication (MFA)
- Unauthorized remote access technologies may not be used or installed on any Mesh Intelligent Technologies, Inc. system
- Users shall use a VPN when transmitting confidential information on public Wi-Fi
- If you access from a public computer (e.g., from a business center, hotel, etc.), log out of the session and don't save anything. Don't check "remember me", collect all printed materials and do not download files to a non-Mesh Intelligent Technologies, Inc. controlled system

# Acceptable Use Policy

Mesh Intelligent Technologies, Inc. proprietary and customer information stored on electronic and computing devices, whether owned or leased by Mesh Intelligent Technologies, Inc., the employee or a third party, remains the sole property of Mesh Intelligent Technologies, Inc. for the purposes of this policy. Employees and contractors must ensure through legal or technical means that proprietary information is protected in accordance with the Data Management Policy. The use of Google Drive/Google Workspace for business file storage is required for users of laptops or company issued devices. Storing important documents on the file share is how you "backup" your laptop.

You have a responsibility to promptly report the theft, loss, or unauthorized disclosure of Mesh Intelligent Technologies, Inc. proprietary information or equipment. You may access, use or share Mesh Intelligent Technologies, Inc. proprietary information only to the extent it is authorized and necessary to fulfill your assigned job duties. Employees are responsible for exercising good judgment regarding the reasonableness of personal use of company-provided devices.

For security and network maintenance purposes, authorized individuals within Mesh Intelligent Technologies, Inc. may monitor equipment, systems and network traffic at any time.

Mesh Intelligent Technologies, Inc. reserves the right to audit networks and systems on a periodic basis to ensure compliance with this policy.

This Acceptable Use Policy works in conjunction with our Code of Conduct to ensure professional and ethical behavior across all company systems and communications.

## Unacceptable Use

The following activities are, in general, prohibited. Employees may be exempted from these restrictions during the course of their legitimate job responsibilities with properly documented Management approval. Under no circumstances is an employee of Mesh Intelligent Technologies, Inc. authorized to engage in any activity that is illegal under local, state, federal or international law while utilizing Mesh Intelligent Technologies, Inc.-owned resources or while representing Mesh Intelligent Technologies, Inc. in any capacity. The list below is not exhaustive, but attempts to provide a framework for activities which fall into the category of unacceptable use.

All behaviors identified as unacceptable in our Code of Conduct also apply to the use of company information systems and resources.

1. Violations of the rights of any person or company protected by copyright, trade secret, patent, or other intellectual property, or similar laws or regulations, including, but not limited to, the installation or distribution of "pirated" or other software products that are not appropriately licensed for use by Mesh Intelligent Technologies, Inc.
2. Unauthorized copying of copyrighted material including, but not limited to, digitization and distribution of photographs from magazines, books, or other copyrighted sources, copyrighted music, and the installation of any copyrighted software for which Mesh Intelligent Technologies, Inc. or the end user does not have an active license
3. Accessing data, a server, or an account for any purpose other than conducting Mesh Intelligent Technologies, Inc. business, even if you have authorized access, is prohibited
4. Exporting software, technical information, encryption software, or technology, in violation of international or regional export control laws, is illegal. The appropriate management shall be consulted prior to export of any material that is in question
5. Introduction of malicious programs into the network or systems (e.g., viruses, worms, Trojan horses, email bombs, etc.)
6. Revealing your account password to others or allowing use of your account by others. This includes family and other household members when work is being done at home
7. Using a Mesh Intelligent Technologies, Inc. computing asset to actively engage in procuring or transmitting material that is in violation of sexual harassment or hostile workplace laws
8. Making fraudulent offers of products, items, or services originating from any Mesh Intelligent Technologies, Inc. account
9. Making statements about warranty, expressly or implied, unless it is a part of normal job duties
10. Effecting security breaches or disruptions of network communication. Security breaches include, but are not limited to, accessing data of which the employee is not an intended recipient, or logging into a server or account that the employee is not expressly authorized to access, unless these duties are within the scope of regular duties. For purposes of this section, "disruption" includes, but is not limited to, network sniffing, pinged floods, packet spoofing, denial of service, and forged routing information for malicious purposes
11. Port scanning or security scanning is expressly prohibited unless prior notification to the Mesh Intelligent Technologies, Inc. engineering team is made
12. Executing any form of network monitoring which will intercept data not intended for the employee's host, unless this activity is a part of the employee's normal job/duty
13. Circumventing user authentication or security of any host, network, or account
14. Introducing honeypots, honeynets, or similar technology on the Mesh Intelligent Technologies, Inc. network
15. Interfering with or denying service to any user other than the employee's host (for example, denial of service attack)
16. Using any program/script/command, or sending messages of any kind, with the intent to interfere with, or disable, a user's session, via any means
17. Providing information about, or lists of: Mesh Intelligent Technologies, Inc. employees, contractors, partners, or customers to parties outside Mesh Intelligent Technologies, Inc. without authorization

## Email and Communication Activities

When using company resources to access and use the Internet, users must realize they represent the company and act accordingly.

The following activities are strictly prohibited, with no exceptions:

1. Sending unsolicited email messages, including the sending of "junk mail", or other advertising material to individuals who did not specifically request such material (email spam)
2. Any form of harassment via email, telephone, or texting, whether through language, frequency, or size of messages
3. Unauthorized use, or forging, of email header information
4. Solicitation of email for any other email address, other than that of the poster's account, with the intent to harass or to collect replies
5. Creating or forwarding "chain letters", "Ponzi", or other "pyramid" schemes of any type
6. Use of unsolicited email originating from within Mesh Intelligent Technologies, Inc. networks or other service providers on behalf of, or to advertise, any service hosted by Mesh Intelligent Technologies, Inc. or connected via Mesh Intelligent Technologies, Inc.'s network
7. Posting the same or similar non-business-related messages to large numbers of Usenet newsgroups (newsgroup spam)

# Additional Policies and Procedures Incorporated by Reference

Personnel are responsible for reading and complying with all policies relevant to their roles and responsibilities.

| Policy | Purpose |
| :---- | :---- |
| Access Control Policy | To limit access to information and information processing systems, networks, and facilities to authorized parties in accordance with business objectives. |
| Asset Management Policy | To identify organizational assets and define appropriate protection responsibilities. |
| Business Continuity & Disaster Recovery Plan | To prepare Mesh Intelligent Technologies, Inc. in the event of extended service outages caused by factors beyond our control (e.g., natural disasters, man-made events), and to restore services to the widest extent possible in a minimum time frame. |
| Code of Conduct | To foster inclusive, collaborative and safe working conditions and define expected professional behavior for all staff. |
| Cryptography Policy | To ensure proper and effective use of cryptography to protect the confidentiality, authenticity and/or integrity of information. |
| Data Management Policy | To ensure that information is classified and protected in accordance with its importance to the organization. |
| Human Resources Security Policy | To ensure that employees and contractors meet security requirements, understand their responsibilities, and are suitable for their roles. |
| Incident Response Plan | Policy and procedures for suspected or confirmed information security incidents. |
| Operations Security Policy | To ensure the correct and secure operation of information processing systems and facilities. |
| Physical Security Policy | To prevent unauthorized physical access or damage to the organization's information and information processing facilities. |
| Risk Management Policy | To define the process for assessing and managing Mesh Intelligent Technologies, Inc.'s information security risks in order to achieve the company's business and information security objectives. |
| Secure Development Policy | To ensure that information security is designed and implemented within the development lifecycle for applications and information systems. |
| Third-Party Management Policy | To ensure protection of the organization's data and assets that are shared with, accessible to, or managed by suppliers, including external parties or third-party organizations such as service providers, vendors, and customers, and to maintain an agreed level of information security and service delivery in line with supplier agreements. |
| Information Security Roles and Responsibilities Policy | To define security roles and responsibilities within the organization for effective communication and implementation of security policies and standards. |

# API Security

## Authentication & Authorization
- OAuth 2.0 with JWT tokens for API authentication
- API keys with granular permission scoping
- Rate limiting per API key and endpoint
- Token rotation and expiration policies (access: ≤60 min, refresh: ≤30 days)

## API Security Controls
- Input validation and sanitization
- Output encoding to prevent injection attacks
- API versioning and deprecation notices (minimum 6 months)
- API documentation with security considerations
- Web Application Firewall (WAF) protection

## API Monitoring
- API usage analytics and anomaly detection
- Rate limit monitoring and alerting
- API error rate tracking
- Security event correlation

# Insider Threat Management

## Preventive Controls
- Background checks for employees with access to sensitive data (where legally permissible)
- Separation of duties for critical functions
- Least privilege access model
- Regular access reviews and certification

## Detective Controls
- User behavior analytics (UBA) monitoring
- Privileged account monitoring
- Data exfiltration detection
- Anomalous access pattern alerts

## Response Procedures
- Insider threat investigation protocols
- Evidence preservation procedures
- Coordination with Legal and HR
- Post-incident analysis and control improvements

# Network Security

## Network Segmentation
- Production/staging/development environment separation
- VPC isolation for different workloads
- Private subnets for sensitive resources
- Bastion hosts for administrative access

## Network Monitoring
- Network flow analysis
- Intrusion detection/prevention systems (IDS/IPS)
- DDoS protection via Google Cloud Armor
- SSL/TLS certificate monitoring

## Remote Access Security
- VPN with MFA for administrative access
- Just-in-time (JIT) access for privileged operations
- Session recording for high-risk activities
- Regular review of remote access logs

# Supply Chain Security

## Software Supply Chain
- SLSA Level 3 target for build provenance
- Software Bill of Materials (SBOM) maintained and updated
- Dependency scanning via GitHub Dependabot
- Container image scanning for vulnerabilities
- Code signing with HSM-backed keys
- Artifact attestations via GitHub/Sigstore

## Third-Party Risk Management
- Vendor security assessments per Third-Party Management Policy
- Minimal vendor dependencies (GCP, GitHub, Sentry, Descope, Paddle, etc.)
- SOC 2/ISO 27001 attestations required for critical vendors
- Annual vendor risk reviews
- Data Processing Addenda (DPAs) for all data processors

# Business Continuity & Disaster Recovery

## Recovery Objectives
- Recovery Time Objective (RTO): 4 hours for core services
- Recovery Point Objective (RPO): Maximum 24-hour data loss
- Multi-Availability Zone architecture with automatic failover
- Daily encrypted backups with 35-day retention
- Quarterly restore testing

## Incident Response Capabilities
- 24/7 security incident hotline: (513) 572-3339
- Incident Response Team with defined roles per IRP
- Communication templates and escalation procedures
- Post-incident reviews and lessons learned
- Regulatory notification within 72 hours for GDPR if required

# Zero Trust Architecture

## Core Principles
- Never trust, always verify - all access requests authenticated and authorized
- Least privilege access - minimal permissions required for job functions
- Assume breach - design security assuming attackers are already in the network
- Verify explicitly - authenticate based on all available data points

## Implementation
- Identity-based perimeter using Google Workspace SSO
- Device trust verification through MDM and Vanta agent
- Micro-segmentation of network resources
- Continuous verification of user and device posture
- Context-aware access policies based on risk signals

# Secure Software Development Lifecycle (SSDLC)

## Security by Design
- Threat modeling for all new features using STRIDE methodology
- Security requirements defined in design phase
- Privacy by design principles for data processing

## Secure Coding Practices
- OWASP Top 10 awareness and prevention
- Input validation and output encoding
- Secure secrets management (no hardcoded credentials)
- Code security training for all developers

## Security Testing
- Static Application Security Testing (SAST) via GitHub Advanced Security
- Dynamic Application Security Testing (DAST) in staging
- Software Composition Analysis (SCA) for dependencies
- Security test cases in QA process

## Deployment Security
- Infrastructure as Code (IaC) security scanning
- Container security scanning before deployment
- Signed artifacts and provenance attestations
- Progressive rollout with monitoring

# Data Loss Prevention (DLP)

## Technical Controls
- Label-based DLP in Google Workspace (Confidential/Restricted labels)
- GitHub secret scanning and push protection
- Email DLP rules blocking external sharing of sensitive data
- USB port blocking on managed devices for Confidential data

## Administrative Controls
- Data classification training for all employees
- Regular audits of data sharing permissions
- Quarterly reviews of external sharing
- Incident response for DLP violations

# Security Metrics & KPIs

## Compliance Metrics
- Policy acknowledgment rate (target: 100%)
- Security training completion (target: 100% within 30 days)
- Access review completion (target: 100% quarterly)
- MFA adoption rate (target: 100%)

## Operational Metrics
- Mean Time to Detect (MTTD) security incidents
- Mean Time to Respond (MTTR) to incidents
- Patch compliance rate by severity
- Vulnerability remediation within SLA
- Phishing simulation click rate (target: <5%)

## Risk Metrics
- Critical vulnerabilities open >30 days (target: 0)
- Percentage of systems with current patches
- Third-party vendors with valid attestations
- Audit findings closure rate

# Security Framework & Technical Controls

## Cloud Infrastructure Security (Google Cloud Platform)
- All production workloads deployed in us-east5 (Ohio) region
- Customer-Managed Encryption Keys (CMEK) for Cloud SQL, GCS, BigQuery, and Pub/Sub
- VPC Service Controls and Identity-Aware Proxy for network security
- Cloud Security Command Center for threat detection
- Audit logs retained for minimum 365 days

## Development & Repository Security (GitHub Enterprise)
- GitHub Advanced Security enabled for vulnerability scanning and secret detection
- Branch protection rules enforced on main branches
- Mandatory code review before merge (minimum 1 reviewer)
- Signed commits required for production code
- OIDC/Workload Identity for CI/CD authentication
- Dependency review for pull requests
- Secret scanning with push protection enabled
- Code scanning with CodeQL
- Security advisories and Dependabot alerts
- Audit log streaming to SIEM

## Identity & Access Management
- Single Sign-On (SSO) via Google Workspace for all internal tools
- Multi-factor authentication (MFA) mandatory for all accounts
- Preference for phishing-resistant factors (security keys/WebAuthn/FIDO2)
- Quarterly access reviews with management attestation
- Principle of least privilege enforced

## AI/ML Governance
- Synthetic data methodology for model training (no customer PII)
- Model versioning and rollback capabilities
- Performance monitoring and drift detection
- Responsible AI practices overseen by Chief AI Officer

## Security Monitoring & Incident Response
- 24/7 security monitoring via Google Cloud Security Command Center
- Sentry for application performance and error tracking
- GitHub Advanced Security for code vulnerability detection
- Incident classification and response per Incident Response Plan
- Target response times: Critical (4 hours), High (8 hours), Medium (12 hours)

## Vulnerability Management
- Annual third-party penetration testing
- Weekly automated vulnerability scans
- Patch management SLAs: Critical (72 hours), High (7 days), Medium (30 days)
- Dependency scanning via GitHub Dependabot and SBOM tracking

## Data Protection & Privacy
- Data classification: Public, Internal, Restricted, Confidential
- Encryption at rest (AES-256) and in transit (TLS 1.3 preferred, TLS 1.2 minimum)
- GDPR and CCPA compliance with documented procedures
- Data retention and deletion per Data Management Policy
- Label-based DLP controls in Google Workspace and GitHub

# Platform-Specific Security Configurations

## Google Workspace Security
- 2-Step Verification enforced for all users
- Security keys preferred for admin accounts
- Context-Aware Access policies based on device trust
- Data Loss Prevention (DLP) rules for sensitive content
- Alert center monitoring for suspicious activities
- Vault retention policies for legal holds
- Admin console audit logging
- Third-party app access restricted via OAuth allowlisting

## Sentry Configuration
- PII scrubbing enabled by default
- Data retention limited to 90 days
- Rate limiting configured
- Project-level access controls
- Audit logging for configuration changes
- Integration with alerting systems

## Descope Authentication Platform
- JWT signing with RS256/ES256
- Token lifetimes: Access ≤60 minutes, Refresh ≤30 days
- Automatic key rotation (quarterly)
- Session timeout after 8 hours of inactivity
- Risk-based authentication with step-up for sensitive operations
- Audit logging for all authentication events

## 1Password Configuration
- Business account with mandatory 2FA
- Secret Key required for new device authorization
- Travel Mode for crossing borders
- Watchtower monitoring for compromised credentials
- Shared vaults for team secrets
- Integration with SSO via Google Workspace

## Segment & Mixpanel Configuration
- TLS 1.3 for all data transmission
- Minimal PII collection (no SSN, financial data)
- Data retention aligned with privacy policy
- User consent management
- Data deletion API integration

# Policy Compliance

Mesh Intelligent Technologies, Inc. will measure and verify compliance to this policy through various methods, including but not limited to:
- Continuous monitoring via Vanta compliance platform
- Annual SOC 2 Type II audits
- Annual penetration testing and security assessments
- Quarterly security metrics review by Security Steering Committee
- Semiannual access reviews and policy attestations
- Internal and external audits

# Security Awareness & Training

All personnel must complete security awareness training:
- New employees: Within 30 days of hire
- Annual refresher training for all staff
- Role-specific training for privileged users, developers, and data handlers
- Phishing simulation exercises (quarterly)
- Incident response tabletop exercises (bi-annually for response team)
- Training completion tracked in Vanta with 100% compliance target

Training topics include:
- Data classification and handling
- Password and authentication best practices
- Phishing and social engineering awareness
- Secure remote work practices
- Incident reporting procedures
- Acceptable use of company resources
- Physical security requirements
- Privacy and data protection

# Exceptions

Requests for an exception to this policy must be submitted to the Policy Owner (Mack Myers) for approval, with final approval from the CEO (Tsavo Knott). Exceptions must include:
- Business justification and risk assessment
- Compensating controls to mitigate risk
- Exception duration (maximum 12 months)
- Owner and review schedule
All exceptions are tracked in GitHub and reviewed quarterly.

# Roles & Responsibilities

Security responsibilities are distributed across the organization as defined in the Information Security Roles and Responsibilities Policy. Key roles include:
- CEO (Tsavo Knott): Ultimate accountability for security program
- Policy Owner (Mack Myers, Corporate Secretary & CPO): Policy governance and compliance oversight
- Co-Owner (Katie Storm, AirCFO - HR): Security awareness training and HR security controls
- Head of Cloud Infrastructure (Hiro Tamada): Infrastructure security and monitoring
- CTO (Mark Widman): Development security and architecture
- CPO (Mack Myers): Compliance management and Vanta platform
- Chief AI Officer (Sam Jones): AI/ML security and governance
- All Employees: Comply with policies and report security concerns

# Assurance & Evidence (Audit Readiness)

Mesh Intelligent Technologies, Inc. maintains comprehensive evidence for SOC 2 Type II compliance:
- Security awareness training completion records (100% target)
- Access review attestations (quarterly)
- Penetration test reports and remediation evidence (annual)
- Vulnerability scan results and patch compliance metrics
- Incident response logs and post-mortem reports
- MFA enforcement reports across all systems
- Device compliance reports from MDM
- Code signing and commit verification logs
- Security configuration baselines for GCP and GitHub
- DLP policy violation reports and remediation
- Backup test results (quarterly)
- Vendor security assessments
- Policy acknowledgment records
- Vanta continuous monitoring dashboards

# Violations & Enforcement

Any known violations of this policy should be reported to the Policy Owner (Mack Myers), HR (Katie Storm - AirCFO), or security@pieces.app. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

Disciplinary actions will be coordinated with HR (AirCFO) and may include verbal counseling, written warnings, suspension, performance improvement plans, reassignment of duties, loss of access privileges, and termination of employment. This enforcement aligns with our Code of Conduct disciplinary procedures.

It is a violation of this policy to retaliate against any person making a complaint or participating in the investigation of any alleged violation. Any retaliation or intimidation may be subject to punitive action up to and including termination.

# Change Log

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 01-Jan-2023 | First Version | Georgia Donmoyer | Tsavo Knott |
| 1.1.0 | 13-Jul-2023 | Updated Mobile Device Policy and Remote Access requirements | Georgia Donmoyer | Tsavo Knott |
| 1.2.0 | 19-Aug-2025 | 2025 Refresh | Mack Myers | Tsavo Knott (CEO) |
