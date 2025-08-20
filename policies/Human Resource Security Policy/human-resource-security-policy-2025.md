---
id: POL-0001
title: Human Resource Security Policy
owner:
  - Katie Storm (AirCFO)
  - Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.)
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards: []
  procedures: []
  controls: []
repo: https://github.com/pieces-app/soc-II-policy
---

# **Human Resource Security Policy** 

**Policy Owner:** Katie Storm (AirCFO), Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.)

**Effective Date:** August 19, 2025 

# **Purpose** 

To ensure that employees and contractors meet security requirements, understand their responsibilities, and are suitable for their roles.

# **Scope** 

This policy applies to all employees of Mesh Intelligent Technologies, Inc., consultants, contractors and other third-party entities with access to Mesh Intelligent Technologies, Inc. production networks and system resources.

# **Policy**

## **Screening**

Background verification checks on Mesh Intelligent Technologies, Inc. personnel shall be carried out in accordance with relevant laws and regulations, and shall be proportional to the business requirements, the classification of the information to be accessed, and the perceived risks. Background screening shall include criminal history checks unless prohibited by local statute, and may include reference verification. All personnel with access to production systems or customer data must complete background screening prior to access. All third-parties with technical privileged or administrative access to Mesh Intelligent Technologies, Inc. production systems or networks are subject to a background check or requirement to provide evidence of an acceptable background, based on their level of access and the perceived risk to Mesh Intelligent Technologies, Inc.

Screening is risk-based and additionally applied to personnel handling sensitive intellectual property, or with access to cloud services, machine learning systems, or infrastructure. Contractors and third parties with equivalent access are screened to the same standard before access is granted. Re-screening may be required upon material role change or where legally or regulatorily required. We do not currently operate in jurisdictions with screening restrictions and will update this policy if that changes.

Evidence location: Contact Katie Storm (AirCFO) for screening records and confirmation.

## **Competence & Performance Assessment**

The skills and competence of employees and contractors shall be assessed by human resources staff and the hiring manager or their designees as part of the hiring process. Required skills and competencies shall be listed in job descriptions and requisitions, and/or aligned with the responsibilities outlined in the Information Security Roles and Responsibilities Policy. Competency evaluations may include reference checks, education and certification verifications, technical testing, and interviews.

All Mesh Intelligent Technologies, Inc. employees will undergo an annual performance review which will include an assessment of job performance, competence in the role, adherence to company policies and code of conduct, and achievement of role-specific objectives.

## **Terms & Conditions of Employment**

Company policies and information security roles and responsibilities shall be communicated to employees and third-parties at the time of hire or engagement, and employees and contractors are required to formally acknowledge their understanding and acceptance of their security responsibilities. Employees and third-parties with access to company or customer information shall sign appropriate non-disclosure, confidentiality, and code-of-conduct agreements. Contractual agreements shall state responsibilities for information security as needed. Employees and relevant third-parties shall follow all Mesh Intelligent Technologies, Inc. information security policies.

All pre-access requirements must be fully met before any access whatsoever is provisioned, including signed Confidentiality/NDA, Code of Conduct, and Acceptable Use acknowledgments. Least-privilege access is granted only after HR completion and required acknowledgments.

## **Management Responsibilities**

Management shall be responsible for ensuring that information security policies and procedures are reviewed at least annually, distributed and available, and that employees and contractors abide by those policies and procedures for the duration of their employment or engagement. Annual policy review shall include a review of any linked or referenced procedures, standards or guidelines.

Management shall ensure that information security responsibilities are communicated to individuals through written job descriptions, policies, or other documented methods which are accurately updated and maintained. Compliance with information security policies and procedures and fulfillment of information security responsibilities shall be evaluated as part of the performance review process wherever applicable.

Management shall consider excessive pressures and opportunities for fraud when establishing incentives and segregating roles, responsibilities, and authorities.

Onboarding is coordinated through airCFO. Access provisioning follows least-privilege principles and occurs only after HR processes are complete and required acknowledgments are signed.

## **Information Security Awareness, Education & Training**

All Mesh Intelligent Technologies, Inc. employees and third-parties with administrative or privileged technical access to Mesh Intelligent Technologies, Inc. production systems and networks shall complete security awareness training at the time of hire and annually thereafter. Management shall monitor training completion and shall take appropriate steps to ensure compliance with this policy. Employees and contractors shall be aware of relevant information security and data privacy policies and procedures. The company shall ensure that personnel receive security and data privacy training appropriate to their role and data handling responsibilities[^2].

In order to maintain a robust level of security awareness, the company will provide security-related updates and communications to company personnel on an ongoing basis through multiple communication channels as needed.

Information security leaders and managers shall ensure appropriate professional development occurs to provide an understanding of current threats and trends in the security landscape. Security leaders and key stakeholders shall attend trainings, obtain and maintain relevant certifications, and maintain memberships in industry groups as appropriate.

New-hire training must be completed within 14 days of start; annual refresher training is due by calendar year-end. Training completion is tracked in Vanta. Role-based modules are not currently required; access risk is additionally managed via strict permissioning in Google Cloud, GitHub Enterprise Security, and Google Workspace. Multi-factor authentication (MFA) is mandatory for all personnel accessing company systems, as defined in the Information Security Policy.

Evidence location: Contact Mack Myers (Corporate Secretary, CPO) for training evidence via Vanta.

## **Termination Process[^3]**

Employee and contractor termination and offboarding processes shall ensure that physical and logical access is promptly revoked in accordance with company SLAs and policies, and that all company issued equipment is returned. Logical access must be disabled immediately upon separation or role change. Company assets must be returned within one week unless otherwise specified; when assets are retained, the operating system must be wiped to factory settings prior to reuse or retention. airCFO retains offboarding documents; authoritative artifacts are stored in Carta and Google Drive data rooms.

Evidence location: Contact Katie Storm (AirCFO) for offboarding documentation; artifacts are stored in Carta and Google Drive data rooms.

Any security or confidentiality agreements which remain valid after termination shall be communicated to the employee or contractor at time of termination.

## **Disciplinary Process**

Employees and third-parties who violate Mesh Intelligent Technologies, Inc. information security policies shall be subject to the Mesh Intelligent Technologies, Inc. progressive disciplinary process, up to and including termination of employment or contract.

# **Exceptions**

Requests for an exception to this policy must be submitted to HR (airCFO) and Security/GRC for approval. Nuanced exceptions require approval by the CEO (Tsavo Knott). Non-critical exceptions may be approved by Katie Storm (AirCFO) or Mack Myers (Corporate Secretary, CPO). Exceptions are time-bound and reviewed upon or before expiration.

# **Violations & Enforcement**

Any known violations of this policy should be reported to HR (airCFO). Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company policies up to and including termination of employment.

## References
- Training system of record: Vanta (contact: Mack Myers)
- Offboarding evidence: Carta and Google Drive data rooms (contact: Mack Myers, Co-Founder and Corporate Secretary or Katie Storm, Our outsourced Head of HR from AirCFO)

## TSC Mapping (for auditor traceability)

- Security (Common Criteria): CC1.1, CC1.2, CC1.4, CC2.2, CC5.2, CC6.1–CC6.4, CC7.2

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| 1.0.0 | 14-Dec-2022 | First Version | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |
| 1.2.0 | 19-Aug-2025 | Added SLAs | Executive Leadership | Tsavo Knott (CEO) |
| | | | |

[^2]:  Training appropriate to roles added for v2

[^3]:  Termination process added for v2



## Definitions (TSC Footnotes)

- Trust Services Criteria (TSC): AICPA-defined criteria used to evaluate the design and operating effectiveness of controls for SOC 2. Security (Common Criteria, “CC”) applies to all SOC 2 reports.
- CC1.1: The entity demonstrates a commitment to integrity and ethical values, forming the foundation of the control environment.
- CC1.2: The board/oversight body demonstrates independence from management and exercises oversight of the development and performance of internal control.
- CC1.4: The entity demonstrates a commitment to attract, develop, and retain competent individuals in alignment with objectives (includes roles/responsibilities and performance management).
- CC2.2: The entity internally communicates information, including objectives and responsibilities for internal control, necessary to support the functioning of internal control.
- CC5.2: The entity restricts logical access to information assets to authorized users, processes, and devices, and to authorized activities and transactions (least-privilege and authorization).
- CC6.1: The entity implements logical access security measures to protect information assets (identification and authentication).
- CC6.2: The entity authorizes, establishes, and maintains logical access to protect information assets (provisioning and approvals).
- CC6.3: The entity enforces appropriate segregation of duties and minimizes incompatible access (role design and conflict management).
- CC6.4: The entity restricts the transmission, movement, and removal of information to authorized internal and external users, processes, and devices (session, network, device controls as applicable).
- CC7.2: The entity implements security awareness training and communication so personnel can carry out their responsibilities related to internal control.

## Other Definitions

- Employee: Direct hire of Mesh Intelligent Technologies, Inc.
- Contractor: Individual engaged via a third-party/vendor; not an employee.
- Third party: External organization with access to company systems or data.
- Onboarding: Process to provision a person for work, including access approvals.
- Offboarding: Process to remove a person’s access and recover assets at separation.
- Material role change: Change that alters data/system access risk (e.g., promotion to admin).
- Background check: Lawful verification(s) conducted pre-access for defined roles.
- Re-screening: Follow-up background check triggered by material role change or law.
- Access provisioning: Granting system access based on approved requests and least-privilege.
- Deprovisioning: Disabling/removing system access at or before separation.
- Least privilege: Grant minimum access required to perform job duties.
- Privileged access: Elevated permissions (e.g., admin, production, security tooling).
- Role-based access control (RBAC): Access determined by role and approved entitlements.
- Segregation of duties (SoD): Separation of incompatible responsibilities/permissions.
- Logical access: Access to information systems, applications, or data (non-physical).
- Production environment: Systems that process live customer or business data.
- Acceptable Use: Rules for appropriate use of company systems and data.
- Confidential information: Non-public company information requiring protection.
- Customer data: Any data provided by or about customers processed by the company.
- Personal data (PII): Information that identifies or can identify an individual.
- Security awareness training: Required training at hire and annually thereafter.
- System of record (SoR): Authoritative system holding the official record/evidence.
- Evidence: Artifacts proving control operation (tickets, logs, reports).
- Exception: Approved, time-bound deviation from a policy or standard.
- Compensating control: Alternative control that mitigates risk when a primary control cannot be met.
- SLA: Service level target for completion (e.g., deprovision within 24 hours).
- Business day vs calendar day: Timelines (e.g., “within one week (7 calendar days)”).
- Identity provider (IdP): Central authentication service (e.g., SSO/MFA).
- MFA: Multi-factor authentication required for privileged access.
- Incident: Event that compromises confidentiality, integrity, or availability.
- Data room: Controlled repository for sensitive artifacts (e.g., Carta, Google Drive).