---
title: Access Control Policy
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)
stakeholders:
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Mark Widman (Chief Technology Officer)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Sam Jones (Chief AI Officer)
  - Tsavo Knott (CEO)
  - Georgia Donmoyer (GRC)
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC5.2, CC6.1–CC6.4, CC7.2
    - ISO/IEC 27001 Annex A: A.5 (Information Security Policies), A.6 (Organization of Information Security), A.9 (Access Control)
  procedures:
    - Access Provisioning & Deprovisioning Procedure (Appendix A)
  controls:
    - Google Workspace IdP/SSO, Google Cloud IAM, GitHub SSO (Enterprise), GitHub Advanced Security
repo: https://github.com/pieces-app/soc-II-policy
---

# **Access Control Policy**

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)

**Effective Date:** August 19, 2025

# **Purpose** 

To limit access to information and information processing systems, networks, and facilities to authorized parties in accordance with business objectives.

# **Scope** 

All Mesh Intelligent Technologies, Inc. information systems that process, store, or transmit Confidential or Restricted data as defined in the Mesh Intelligent Technologies, Inc. Data Management Policy. This policy applies to all employees of Mesh Intelligent Technologies, Inc. and to all external parties with access to Mesh Intelligent Technologies, Inc. networks and system resources.

# **Policy**

Access to information computing resources is limited to personnel with a business requirement for such access. Access rights shall be granted, reviewed, modified, and revoked in accordance with this Access Control Policy.

## **Identity and Access Platforms (Authoritative Systems)**

- Google Workspace is the authoritative Identity Provider (IdP) for personnel identities and SSO/MFA enforcement. All feasible systems must integrate with Google Workspace SSO.
- Google Cloud Platform (GCP) access is governed by Google Cloud IAM and Identity-Aware controls, bound to Google Workspace identities and groups.
- GitHub (Enterprise) access is governed via SSO (SAML/OIDC) with GitHub Enterprise Security; branch protections and GitHub Advanced Security (secret/code scanning, Dependabot) are enabled for production repositories.
- Access to other sanctioned SaaS must be integrated with Google Workspace SSO and enforce MFA where supported.
- Sanctioned SaaS examples include Sentry.io, Descope.com, Paddle.com, Satismeter.com, Mixpanel.io, Segment.com, HubSpot.com, Customer.io, and Hugging Face; all must use SSO and enforce MFA where supported.
 - Where supported, SCIM is enabled to automate provisioning/deprovisioning and group-based entitlements.

# **Business Requirements of Access Control**

## **Access Control Policy**

Mesh Intelligent Technologies, Inc. determines the type and level of access granted to individual users based on the principle of least privilege. Permissions and access rights not expressly granted are, by default, prohibited.

Role-Based Access Control (RBAC) is used wherever feasible to assign and maintain consistent access rights via groups/teams. Individual user accounts may be granted additional permissions as needed with approval from the system owner or authorized party.

All privileged access to production infrastructure shall use Multi-Factor Authentication (MFA).

## **Access to Networks and Network Services**

The following security standards govern access to Mesh Intelligent Technologies, Inc. networks and network services:

- Technical access to company networks must be formally documented including the approver, grantor, and date.
- Only authorized employees and third-parties working off a signed contract or statement of work, with a business need, are granted access to production networks and resources.
- Guests may be granted access to guest networks after registering with office staff without a documented request.
- Remote connections to production systems and networks must be encrypted. VPN is required for remote access to internal resources; exceptions must be documented and approved. Where applicable, VPN integrates with SSO/MFA.

# **Customer Access Management**

When configuring cross-account access using cloud IAM roles (e.g., AWS/Azure/GCP equivalents), Mesh Intelligent Technologies, Inc. generates the external ID value used to ensure the integrity of the cross-account role configuration. Partner-generated external IDs ensure malicious parties cannot impersonate a customer's configuration and enforce uniqueness and format consistency across all customers.

- External IDs used must be unique across all customers; re-using external IDs is prohibited.
- Customers must not be able to set or influence external IDs.

Note: Customers are not permitted to set or influence external IDs for cross-account access roles.

# **User Access Management**

Mesh Intelligent Technologies, Inc. requires that all personnel have a unique user identifier for system access, and that credentials are not shared. Users with multiple levels of access (e.g., administrators) should be given separate accounts for normal system use and for administrative functions wherever feasible. Root, service, and administrator accounts may use an approved password manager for business continuity purposes only. Administrators shall only use shared administrative accounts as needed. If a password is compromised or suspected of compromise, report immediately to Security (security@pieces.app) and change the password.

## **User Registration and Deregistration**

Only authorized administrators may create new user IDs upon documented requests from authorized parties. User provisioning requests must include approval from data owners or management authorized to grant system access. Prior to account creation, administrators verify that the account does not violate segregation of duties, fraud prevention measures, or access rights restrictions.

User IDs shall be promptly disabled or removed when users leave the organization or contract work ends in accordance with SLAs. User IDs shall not be re-used.

## **User Access Provisioning**

- New employees and/or contractors are not granted access to any production systems until after completion of all HR onboarding tasks, which include signed employment/contractor agreements, confidentiality/NDA, and acknowledgement of company information security policies.
- Access is restricted to only what is necessary to perform job duties (least privilege).
- No access may be granted earlier than the official start date.
- Access requests and rights modifications are documented in a ticket or tracked email; no permissions are granted without approval from the system or data owner or management.
- Records of all permission and privilege changes are maintained for no less than one year.

### **Lifecycle Automation (SCIM)**

- When available, SCIM connectors are used to automatically create, update, and disable accounts and to synchronize group membership from the IdP. Manual exceptions must be documented and reconciled back to IdP groups within one business day.

## **Management of Privileged Access**

Mesh Intelligent Technologies, Inc. ensures that the allocation and use of privileged access rights are restricted and managed judiciously:

- Identify and validate users who require privileged access for each system and process.
- Allocate privileged rights based on specific needs and competencies, adhering strictly to this policy.
- Maintain authorization records for all privileged access allocations.
- Enforce strong authentication: MFA is required for all privileged access.
- Prevent use of generic administrative user IDs; when unavoidable, implement strict logging, approvals, and time-bound usage.
- Time-bound access: Grant elevated access only for the necessary duration to accomplish specific tasks and revoke upon task completion.
- Ensure logging and auditing: Log all privileged logins and activity; logs are retained ≥ 365 days.

### **Just-in-Time (JIT) and Break-Glass Access**

- JIT Elevation: Prefer workflow-based, time-bound elevation for administrative tasks with explicit approvals; avoid permanent standing admin rights where feasible.
- Break-Glass Accounts: Disabled by default and excluded from routine use. Credentials are vaulted and rotated at least quarterly. Any activation requires CEO or delegate approval, a ticket reference, MFA, and is time-bound; all usage is logged and reviewed within one business day with immediate post-use revocation.

## **User Access Reviews**

Administrators perform access rights reviews of user, administrator, and service accounts on a quarterly basis to verify that access is limited to systems required for job functions. Access reviews are documented. Reviews include group/role membership and any exception-based permissions. Access rights are also reviewed upon job role change (promotion, demotion, transfer).

## **Removal & Adjustment of Access Rights**

Access rights are promptly removed upon termination of employment or contract, or when rights are no longer needed due to a role change. Maximum allowable time period for access termination is 24 business hours.

## **Access Provisioning, Deprovisioning, and Change Procedure**

The Access Management Procedure for Mesh Intelligent Technologies, Inc. systems is defined in Appendix A of this policy and governs provisioning, change, and deprovisioning workflows and evidence retention.

## **Segregation of Duties**

Conflicting duties and areas of responsibility are segregated to reduce opportunities for unauthorized or unintentional modification or misuse of assets. When provisioning access, care is taken that no single person can access, modify, or use assets without authorization or detection. The initiation of an event is separated from its authorization. The possibility of collusion is considered when determining access levels for individuals and groups.

## **System and Application Access**

### **Information Access Restriction**

Applications must restrict access to program functions and information to authorized users and support personnel in accordance with this policy. The level and type of restrictions applied by each application are based on individual application requirements, as identified by the data owner, and must conform to company policies regarding access controls and data management.

Prior to implementation, evaluation criteria are applied to determine necessary access controls and data policies, including:

- Sensitivity and classification of data.
- Risk to the organization of unauthorized access or disclosure of data.
- Ability and granularity of control(s) on user access rights to the application and data stored within the application.
- Restrictions on data outputs, including filtering sensitive information, controlling output, and restricting information access to authorized personnel.
- Controls over access rights between the evaluated application and other applications and systems.
- Programmatic restrictions on user access to application functions and privileged instructions.
- Logging and auditing functionality for system functions and information access.
- Data retention and aging features.

All unnecessary default accounts must be removed or disabled before making a system available on the network. Vendor default passwords and credentials must be changed on all systems, devices, and infrastructure prior to deployment, including those used by operating systems, security software, application/system accounts, and SNMP community strings where feasible.

### **Secure Log-on Procedures**

Secure log-on controls are designed and selected in accordance with the sensitivity of data and the risk of unauthorized access based on the totality of the security and access control architecture.

### **Password Management System**

Systems for managing passwords should be interactive and assist personnel in maintaining password standards by enforcing password strength criteria including minimum length and complexity where feasible. All storage and transmission of passwords is protected using appropriate cryptographic protections (hashing or encryption). See the Cryptography Policy for algorithm requirements and provider controls.

### **Session Management**

- Provider Defaults: We adhere to provider-default session configurations across Google Workspace, GCP, GitHub, and sanctioned SaaS; we do not override timeouts unless risk requires.
- Reauthentication: Require reauthentication/step-up MFA for sensitive operations and privilege elevation where supported.
- Anomalies: Trigger step-up authentication for anomalous activity.
- Device Posture: Where supported, restrict access to Confidential/Restricted systems to devices meeting MDM posture (encryption, screen lock, OS updates).

### **Use of Privileged Utility Programs**

Use of utility programs, system files, or other software capable of overriding controls or altering configurations is restricted to the minimum personnel required. Systems maintain logs of all use of system utilities or alteration of configurations. Extraneous system utilities or other privileged programs are removed or disabled as part of the system build and configuration process. Management approval is required prior to installation or use of any ad hoc or third-party system utilities.

### **Access to Program Source Code**

Access to program source code and associated items (designs, specifications, verification/validation plans) is strictly controlled to prevent introduction of unauthorized functionality, avoid unintentional changes, and protect intellectual property. All access to source code is based on business need and logged for review and audit. GitHub Enterprise Security enforces branch protections and code review.

### **GitHub Enterprise Controls (Repositories and CI/CD)**

- Branch Protection: Protected branches require pull request reviews, status checks, up-to-date branches, and (where feasible) signed commits. Dismiss stale approvals on new commits. Require CODEOWNERS for critical repositories.
- Reviews: Require at least 1–2 approvers (not the author) for production repositories; enforce required reviewers via organization policy.
- Secrets & Push Protection: Enable GHAS secret scanning and push protection for all repositories; delegated bypass is limited to documented exceptions.
- Environments & Deployments: Use protected environments with required reviewers and deployment gates for production; require approvals before promotion. Restrict self-hosted runners by labels and repositories; use OIDC/workload identity instead of long-lived cloud credentials.
- Actions Hardening: Pin actions by commit SHA; restrict repository and organization-level secrets; prefer environment secrets with minimal scopes.

### **Google Cloud IAM Controls**

- Group-Based IAM: Bind permissions to Google Groups mapped to roles. Direct user bindings are permitted with documented justification and approval; they are reviewed quarterly and migrated to groups where feasible. Use predefined roles where possible; custom roles are narrowly scoped.
- IAM Conditions & Deny/Org Policies: Scope access by resource or context; apply IAM Deny and Organization Policies to block risky permissions globally where appropriate.
- Service Accounts: Prefer Workload Identity Federation (e.g., GitHub OIDC) for workloads. Avoid long-lived keys; if unavoidable, store keys in an approved secret manager (e.g., Google Secret Manager or GitHub Secrets with repo/org/environment scoping), restrict access, and rotate promptly. Disable unused service accounts and keys.
- Audit Logs: Ensure Admin, Data Access (where feasible), and System Event logs are enabled and retained ≥ 365 days; consider Access Transparency logs where available.

# **User Responsibility for the Management of Secret Authentication Information**

Control and management of individual user passwords is the responsibility of all personnel and third-party users. Users shall protect secret authentication information in accordance with the Information Security Policy and Cryptography Policy.

# **Password Policy**

Where feasible, passwords for Confidential/Restricted systems shall be configured for at least:

- Eight (8) or more characters, at least one uppercase letter, and at least one number (or stronger per provider baseline).
- Systems should be configured to remember and prohibit reuse of the last 16 passwords where supported.
- Accounts lock after 6 failed attempts; lockout duration per provider best practice.
- Initial passwords must be set to a unique value and changed after first log in for any systems that issue initial passwords.
- For manual password resets, a user’s identity must be verified prior to changing passwords.
- Do not limit the permitted characters that can be used; allow long passphrases.
- Do not limit the length of the password to anything below 64 characters where feasible.
- Do not use secret questions as a sole password reset requirement.
- Require email or SSO verification for a password change request.
- Require the current password in addition to the new password during password change.
- Verify newly created passwords against common/leaked password lists where supported.
- Check existing user passwords for compromise regularly where supported.
- Store passwords only in a hashed and salted format using industry-standard, provider-managed one-way hash functions; plaintext storage is prohibited. No custom/homegrown password hashing.
- Enforce appropriate account lockout and brute-force protections on account access.

Note: Periodic forced expiration is generally discouraged unless required by a platform or regulation; rotation occurs upon suspicion of compromise or policy exception requirements.

# **Strong Authentication (SSO/MFA) for Internal SaaS**

- Enforcement: All internal SaaS used for development and operations (e.g., Google Workspace/GCP, GitHub Enterprise, Sentry, Segment, Mixpanel) must enforce SSO with multi-factor authentication (MFA).
- Factors: Security keys (WebAuthn/FIDO2) preferred; TOTP (RFC 6238) allowed as fallback; SMS is disallowed except as a break-glass method with documented, time-bound approval.
- Scope: MFA is mandatory for all personnel accessing company systems. Privileged roles (e.g., cloud admins, repo admins, CI/CD maintainers) must use MFA at all times.
- Privileged Factors: Privileged roles must enroll and use phishing-resistant factors (e.g., FIDO2/WebAuthn security keys) where feasible; TOTP is permitted only as a secondary factor.
- Review: Semiannual reviews verify MFA enforcement policies across providers and removal of non-compliant accounts; evidence is retained.

# **Security Monitoring & Log Retention**

- Security and access logs are retained for a minimum of 90 days across systems to support forensic analysis and compliance needs.
- IAM, administrative, and privileged activity logs are retained for ≥ 365 days (e.g., Google Cloud Admin/Data Access/System Event logs; GitHub audit logs) to ensure traceability of sensitive operations.
- Maintain audit trails for system access, data modifications, and administrative actions; ensure availability and integrity of logs for investigations.
- Monitoring platforms include Google Cloud Security Command Center, GitHub Advanced Security, and Sentry; continuous posture and access governance monitoring is performed via Vanta where applicable.

# **Exceptions**

Requests for an exception to this policy must be submitted to Security/GRC and approved by the CEO (Tsavo Knott) or delegate. Exceptions are time-bound and must include scope, rationale, compensating controls, owner, and expiration.

# **Violations & Enforcement**

Report suspected violations to security@pieces.app, the Corporate Secretary (CPO), or Head of Cloud Infrastructure. Violations may result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action up to and including termination of employment.

## **Assurance & Evidence (Audit Readiness)**

We maintain the following evidence:

- Quarterly access review records (Google Workspace groups, GCP IAM roles, GitHub team/repo access), with approvals and remediation.
- SSO/MFA enforcement screenshots or configuration exports across providers; semiannual attestations.
- Provisioning/deprovisioning tickets and change logs; termination deprovision completed within 24 business hours.
- GitHub Advanced Security reports (secret scanning, Dependabot, code scanning) and remediation tracking; branch protection settings.
- Cloud audit logs for IAM changes and privileged access (≥ 365 days retention).
- Password policy configurations from IdP/SaaS where applicable.
 - Session policy exports and admin console timeout settings; break-glass usage logs and quarterly credential rotation evidence.

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 14-Feb-2023 | First Version | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh; aligned SSO/MFA, GCP/GitHub, assurance evidence | Executive Leadership | Tsavo Knott (CEO) |

## **TSC Mapping (SOC 2)**

- CC5.2: Restricts logical access to authorized users, processes, and devices (least privilege, RBAC, IdP/SSO, MDM posture).
- CC6.1–CC6.4: Identification, authentication, authorization, segregation of duties, session and privilege management (MFA, JIT, break-glass, reviews).
- CC7.2: Security awareness and responsibilities (references to HR/training and enforcement).

## **References**

- Legal & Security Policies (Customer-Facing): Access Controls, Logging & Retention, BCP/DR (RTO/RPO), Privacy, Deletion timelines.
- Cryptography Policy: TLS, password hashing, KMS/Secrets, token/session security.
- Data Management Policy: Classification, DLP, retention (internal logs ≥ 365 days; product-facing minimums per Legal Policy).
- Asset Management Policy: MDM/device posture, inventory, disposal.
- Risk Management Policy: Governance, access-related risks, review cadence.

# **APPENDIX A – Access Provisioning, Deprovisioning, and Change Procedure**

1. HR Onboarding Trigger
   - HR (airCFO) completes screening and collects required acknowledgments (NDA/Confidentiality, Code of Conduct, Acceptable Use, policy acknowledgments).
   - HR notifies Security/IT via ticket/email to initiate access provisioning.
2. Baseline Provisioning (Least Privilege)
   - Create/enable Google Workspace account; assign baseline group(s) per role (Employee, Engineering, Sales, etc.); enforce SSO/MFA at first login.
   - Provision Google Cloud IAM predefined roles via groups mapped to job role; no direct user roles unless approved.
   - Add to GitHub via SSO; assign to GitHub teams with least-privilege repository access; branch protections and required reviews enforced.
   - Provision additional SaaS (CRM, Expense, Sentry, Segment/Mixpanel) through Google Workspace SSO and role-based groups.
3. Privileged Access
   - Privileged access requires manager/system owner approval. Grant via group membership, time-bound where feasible; log all grants.
   - Break-glass accounts are disabled by default and monitored; usage requires incident/ticket reference and post-use review.
4. Changes
   - Access changes follow the same approval and documentation requirements. Track in ticketing system with approver, grantor, and date.
5. Deprovisioning (Separation or Role Change)
   - Disable Google Workspace account and revoke sessions; remove from groups within 24 business hours (target immediate for terminations).
   - Remove GCP IAM roles/groups; revoke service accounts/keys if applicable.
   - Remove GitHub team/repo access; disable SSO for the user.
   - Revoke access to all SaaS (CRM, Expense, Sentry, Segment/Mixpanel) via SSO groups; rotate shared credentials if any.
   - Coordinate device return with HR; ensure device and data handling per Data Management Policy.
6. Records & Evidence
   - Retain provisioning/deprovisioning records for ≥ 1 year; maintain audit logs ≥ 365 days.

# **APPENDIX B – Access Matrix**

| Role | Google Workspace (incl. Email) | Expense Tool | CRM | GCP (Infrastructure) | GitHub (Repos & Actions) |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Employee | x | x |  |  |  |
| Engineer | x | x |  | x | x |
| Engineer Sprvs | x | x |  | x | x |
| ML Engineer / Data Scientist | x | x |  | x (data roles only) | x |
| Sales & Business Dev | x | x | x |  |  |
| Growth & Marketing | x | x |  |  |  |

Note: CI/CD and vulnerability scanning are included in GitHub (Repos & Actions). GHAS is enabled for production repositories; protected environments and deployment approvals are enforced for production.

