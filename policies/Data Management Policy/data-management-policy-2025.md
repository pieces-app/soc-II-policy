---
id: POL-0004
title: Data Management Policy
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)
stakeholders:
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Sam Jones (Chief AI Officer)
  - Mark Widman (Chief Technology Officer)
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - ISO/IEC 27001 Annex A: A.5 (Information Security Policies), A.8 (Asset Management)
    - SOC 2 CC1.1, CC1.2, CC1.4, CC6.1, CC6.2, CC6.6
  procedures:
    - Data Classification Standard
    - Data Retention & Secure Disposal Procedure
  controls:
    - NIST SP 800-88 Rev. 1 (Media Sanitization)
repo: https://github.com/pieces-app/soc-II-policy
---

# **Data Management Policy**

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)

**Effective Date:** August 19, 2025

# **Purpose**

To ensure that information is classified, protected, retained, and securely disposed of in accordance with its importance to the organization and applicable legal, regulatory, and contractual requirements.

# **Scope**

All Mesh Intelligent Technologies, Inc. data, information, and information systems, including data processed within Google Workspace, Google Cloud Platform, GitHub, sanctioned SaaS applications, employee endpoints, backups/snapshots, and paper records.

# **Policy**

## **Data Classification Framework**

Mesh Intelligent Technologies, Inc. classifies data and information systems in accordance with legal requirements, sensitivity, and business criticality to ensure appropriate protection. Information systems and applications shall be classified according to the highest classification of data that they store or process. Data owners are responsible for identifying additional requirements or exceptions where necessary.

Classification levels:
- Public: Information intended for public release; no harm if disclosed. Examples: marketing materials, product descriptions, release notes, external-facing policies.
- Internal: Non-public information intended for company use where unauthorized disclosure would cause limited harm. Examples: general internal communications, team notes, routine operational documents that do not contain confidential or regulated data.
- Restricted: Proprietary information requiring thorough protection; access is limited to personnel with a need-to-know. Examples: internal policies and procedures under development, legal documents under negotiation, internal reports and dashboards, certain meeting minutes and internal presentations, contracts, Slack messages and email that include sensitive business context.
- Confidential: Highly sensitive data requiring the highest level of protection; access is restricted to specific roles and requires explicit approval from the data owner or an executive. Examples: customer data, personally identifiable information (PII), financial and banking data, salary/compensation/payroll, strategic plans, incident reports, risk assessments, vulnerability reports, authentication credentials, secrets and private keys, source code, and litigation materials.

Labeling:
- Confidential paper records should be labeled “CONFIDENTIAL” when printed and must be securely stored and disposed of.
- Electronic assets must carry classification labels in inventories and, where supported, tags/labels in systems (e.g., Drive labels, repository topics, cloud tags).
 - Default classification: Unless otherwise designated by the data owner, company information is treated as Restricted.

## **Label-Based DLP Controls**

We enforce label-aware data loss prevention (DLP) using existing classification labels:
- Google Workspace: Confidential documents are restricted from external sharing by default; downloads and link-sharing are limited based on label; exceptions require documented approval and time-bound controls.
- GitHub: Repositories containing Confidential code or secrets are prohibited from public visibility; branch protections and secret scanning are enabled; external collaborator access requires approval.
- Email/Chat: Automatic warnings and/or blocks on messages containing Confidential indicators or patterns (e.g., secrets), with override only by authorized roles and logged.

## **Data Handling Requirements by Classification**

Confidential:
- Access restricted to authorized roles; non-preapproved access requires documented approval from the data owner or executive.
- Systems shall not allow unauthenticated or anonymous access.
- Encryption in transit and at rest per the Cryptography Policy; endpoint full-disk encryption required.
- Confidential customer data shall not be used or stored in non-production environments.
- Mobile devices storing or accessing confidential data must use strong authentication and auto-lock (≤ 5 minutes of inactivity) and be enrolled in MDM where feasible.
- Backups containing confidential data must be encrypted; restoration is restricted and logged.
- Confidential data must not be stored on personal devices or removable media; exceptions require executive approval with compensating controls.
- Paper records created only when necessary; securely stored and securely disposed of.
- Transfer outside the company only per contract and with explicit written permission from management or the data owner.

Restricted:
- Access limited to need-to-know users; systems shall not allow unauthenticated or anonymous access.
- Transfer outside the company requires management approval and must be consistent with contractual or data owner requirements.
- Paper records securely stored and disposed of; devices used to store restricted data must be securely wiped prior to disposal or physically destroyed.

Internal:
- Access limited to company personnel; follow least privilege. Sharing outside the company requires management approval.
- Avoid storage on unmanaged personal devices. Use approved, managed services (e.g., Google Workspace) for storage and collaboration.

Public:
- No special handling controls beyond ensuring accuracy and authorization for publication. Public data may be freely distributed.

## **Customer Data, Privacy, and AI Alignment**

- Customer personal data is processed in alignment with our Legal & Security Policies (Customer-Facing), including Data Retention and Data Deletion controls. Customer personal data is not used for model training; we utilize synthetic or non-customer data in accordance with the AI Governance & Data Policy.
- Data subject requests (DSRs) and deletion requests follow the timelines and verification procedures defined in the Legal & Security Policies.
- Personally identifiable information (PII) is collected, used, and retained only for legitimate business purposes and is deleted or de-identified upon verified request unless a legal or contractual obligation requires retention.

## **Data Retention & Deletion**

- Mesh Intelligent Technologies, Inc. retains data as long as there is a business need or to meet regulatory/contractual requirements. Once data is no longer needed, it is securely disposed of or archived per the Data Retention & Secure Disposal Procedure.
- Customer-facing product data retention follows the Legal & Security Policies (Customer-Facing) schedule (e.g., backups ~35 days; security & access logs ≥ 90 days; telemetry typically 180 days) and any contractual commitments.
- Internal corporate records retention is maintained per Appendix B (Internal Data Retention Matrix).
- Personally identifiable information (PII) shall be deleted or de-identified as soon as it no longer has a legitimate business use, subject to legal holds or contractual obligations.
- Deletion from backups: corresponding data is removed or cryptographically rendered inaccessible according to backup retention practices.
- Data owners, in consultation with Legal Counsel, define system- or record-specific retention requirements; any deviations from Appendix B must be documented with rationale and approval.

## **Data & Device Disposal**

- Data classified as Restricted or Confidential must be securely deleted when no longer needed.
- Third-party vendors are assessed for secure data disposal practices in accordance with the Third-Party Management Policy; only vendors meeting our requirements may process or store Restricted or Confidential data.
- Company devices and media containing Restricted or Confidential data must be sanitized or destroyed per NIST SP 800-88 Rev. 1 prior to disposal, reissuance, or gifting.
- Certificates of Destruction (COD) from third parties are retained for at least seven (7) years or longer if required by contract or regulation.

## **Device Management (MDM) Requirements**

- Enrollment: Any device (company-managed or BYOD) that accesses Restricted or Confidential data must be enrolled in Mobile Device Management (MDM).
- Capabilities: Enforced full-disk encryption, screen lock with auto-lock ≤ 5 minutes, remote wipe, OS and security patch enforcement, configuration baselines, and device inventory.
- Access Control: Non-enrolled devices are blocked from accessing Restricted/Confidential systems except under a documented exception with compensating controls and time limits.
- Network Alignment: MDM complements existing VPC/VPN controls by ensuring endpoint posture before access.

## **Legal Holds**

When legal holds apply, data subject to the hold is exempt from standard deletion timelines and must be retained according to instructions from Legal Counsel. Legal holds and their scope are reviewed at least annually with Legal to validate continuing requirements.

## **Annual Review & Compliance**

- This policy is reviewed at least annually. Retention requirements are reviewed during the policy review.
- Compliance with this policy is measured through tool reports (e.g., Google Workspace, Google Cloud, GitHub, Vanta) and internal/external audits.

## **Assurance & Evidence (Audit Readiness)**

We maintain the following evidence to demonstrate compliance:
- Data inventories with classification labels and owners.
- Semiannual access reviews and attestations for Confidential/Restricted systems; audit logs retained ≥ 365 days.
- Backup and restore test records (quarterly) and retention configurations (35-day backups).
- Certificates of Destruction (≥ 7 years) for sanitized/destroyed devices and media.
- Vendor assessments, DPAs, and documented retention/disposal controls for processors.
- DSR/Deletion request logs with timelines (≤ 60 days) and verification records.
- Annual policy review records and personnel training acknowledgments.

## **Assurance & Evidence (Audit Readiness)**

We maintain the following evidence to demonstrate compliance:
- Data inventories with classification labels and owners.
- Access reviews and attestations for Confidential/Restricted systems; audit logs retained ≥ 365 days.
- Backup and restore test records (quarterly) and retention configurations (35-day backups).
- Certificates of Destruction (≥ 7 years) for sanitized/destroyed devices and media.
- Vendor assessments, DPAs, and documented retention/disposal controls for processors.
- DSR/Deletion request logs with timelines (≤ 60 days) and verification records.
- Annual policy review records and personnel training acknowledgments.

## **Exceptions**

Requests for exceptions to this policy must be submitted to the Corporate Secretary (Policy Owner) or the Chief Product Officer (CPO) for review and must be approved by the CEO (Tsavo Knott), the CPO, or the Corporate Secretary. Exceptions must define scope, compensating controls, and expiration. Exceptions applicable to specific products, AI systems, or infrastructure must include sign-off by the accountable stakeholder (e.g., CTO for engineering systems, Head of Cloud Infrastructure for platform or network, Chief AI Officer for model/AI data usage).

## **Violations & Enforcement**

Report suspected violations to security@pieces.app, the Corporate Secretary, or the Chief Product Officer (CPO). Violations may result in suspension of privileges and/or disciplinary action up to and including termination.

## **Training & Acknowledgment**

All personnel must review and acknowledge this policy during onboarding and annually thereafter. Role-specific training is provided for data owners and custodians.

## **Roles & Responsibilities**

- Corporate Secretary & CPO (Mack Myers): Owns this policy, approves exceptions, ensures annual review and training completion.
- Head of Cloud Infrastructure (Hiro Tamada): Implements logging, backups, data retention enforcement, and secure disposal technical controls.
- Chief Technology Officer (Mark Widman): Oversees engineering adherence to data handling requirements and SSDLC alignment.
- Chief AI Officer (Sam Jones): Ensures AI data usage aligns with privacy and training restrictions; validates synthetic/non-customer data usage for model improvement.
- Legal Counsel: Manages legal holds and advises on retention requirements.

## **TSC Mapping**

- CC1.1, CC1.2, CC1.4: Governance, policy management, roles & responsibilities; see Roles & Responsibilities, Annual Review & Compliance.
- CC2.2: Communication and training; see Training & Acknowledgment, Label-Based DLP Controls.
- CC6.1, CC6.2: Access restrictions and authentication; see Data Handling Requirements, Device Management (MDM) Requirements.
- CC6.6: Data protection and retention; see Data Retention & Deletion, Data & Device Disposal, Assurance & Evidence.

## **References**

- Legal & Security Policies (Customer-Facing): Data Retention, Data Deletion, Privacy, AI Governance & Data Policy
- Asset Management Policy (classification labels, device controls)
- Third-Party Management Policy (vendor assessments, DPAs)
- NIST SP 800-88 Rev. 1 (Media Sanitization)
 - Cryptography Policy

## **Change Log**

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 08-Mar-2023 | First Version | Mack Myers | Tsavo Knott (CEO) |
| 1.1.0 | 13-Jul-2023 | Updated Data Retention Matrix | Georgia Donmoyer | Mack Myers |
| 1.2.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |

---

# **APPENDIX A – Internal Retention and Secure Disposal Procedure**

Engineering and Security are responsible for enforcing data retention and secure disposal for company-managed systems and devices.

Customer Accounts (product data):
1. Customer accounts and associated product data are deleted per the Legal & Security Policies timelines, and in all cases no later than sixty (60) days after a verified deletion request or contract termination; backups are aged out according to standard retention (typically ~35 days).

Employee Devices:
1. Devices are collected promptly upon termination. For remote employees, return is coordinated via pre-paid shipping with tracking.
2. Returned devices are sanitized (secure erase) and re-provisioned, or removed from inventory. Where a factory reset is insufficient, secure wiping is performed. Certificates of Destruction are obtained for third-party destruction and retained ≥ 7 years.
3. Device images may be retained at management discretion for legitimate business purposes consistent with retention schedules.

Destroying devices or electronic media:
- If a device cannot be erased due to damage, an e-waste provider with data destruction and COD is used. Full Disk Encryption reduces recovery risk but does not replace sanitization requirements.
- CODs are retained ≥ 7 years.

This procedure is reviewed at least annually.

---

# **APPENDIX B – Internal Data Retention Matrix**

Note: Customer-facing product data retention is defined in the Legal & Security Policies (Customer-Facing). The matrix below applies to internal corporate records and operational data.

| System or Record | Retention Period | Notes |
| :--- | :---: | :--- |
| Information Security Records | 1 year after archive | May be extended by legal hold |
| Security & Access Logs | ≥ 365 days | Aligns with 2023 baseline and Legal Policy minimums |
| Audit Logs | ≥ 1 year | System/application/infrastructure audit trails |
| Telemetry & Diagnostics | 180 days (rolling) | Operational monitoring |
| Customer Support Tickets | Indefinite | May be reduced per contract or privacy requirements; extended by legal hold |
| Support & Communications (excluding Customer Support Tickets) | 2 years after case closure | Customer service defensibility |
| Internal User Data (corporate) | 1 year | Non-product data |
| Audit Reports | 2 years | Internal/external assessments |
| Other Records | 2 years or as required by regulation | Subject to legal hold |

---