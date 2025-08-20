---
id: POL-0003
title: Asset Management Policy
owner:
  - Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.)
  - Katie Storm (AirCFO; Asset Manager)
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - ISO/IEC 27001 Annex A: A.5, A.8
    - NIST SP 800-88 Rev. 1 (Media Sanitization)
  procedures:
    - Asset Issuance & Return Procedure
    - Media Sanitization Procedure
    - Mobile Device Management (MDM) Procedure
  controls:
    - SOC 2 CC1.1, CC1.2, CC1.4, CC6.1, CC6.2, CC6.6
repo: https://github.com/pieces-app/soc-II-policy
---

# **Asset Management Policy**

**Policy Owner:** Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.), Katie Storm (AirCFO; Asset Manager)

**Effective Date:** August 19, 2025

# **Purpose** 

To identify organizational assets and define appropriate protection responsibilities. To ensure that information receives an appropriate level of protection in accordance with its importance to the organization. To prevent unauthorized disclosure, modification, removal, or destruction of information stored on media.

# **Scope** 

This policy applies to all Mesh Intelligent Technologies, Inc. owned or managed information systems.

# **Policy**

## **Inventory of Assets**

Assets associated with information and information processing facilities that store, process, or transmit classified or confidential information shall be identified and an inventory of these assets shall be created and maintained.

The centralized asset inventory shall include, at minimum: unique asset identifier, asset type (hardware, software, virtual/cloud, media), assigned owner and custodian, location, serial number or instance ID, encryption status, installed OS and version, critical software, last check-in/"last seen" timestamp, data classification, lifecycle status (in service, in repair, retired, disposed), and disposal records.

New assets must be recorded in the inventory within two (2) business days of issuance or provisioning. Retired or disposed assets must be updated in the inventory within two (2) business days of status change. Inventory accuracy is validated at least quarterly via the Vanta agent on endpoints, Google Workspace device management and enterprise Chrome profiles, and cloud inventory reconciliation (Google Cloud), complemented by SSO discovery and finance reconciliation (see Shadow IT Monitoring & Discovery).

The asset inventory covers:

- End-user computing devices (laptops, desktops, mobile devices, authentication tokens)
- Infrastructure and cloud resources (projects, VPCs, instances, databases, buckets, serverless functions)
- Software assets and licenses (including SaaS applications)
- Removable media and other storage devices

### What is an Asset (definition)
Assets include any information, device, system, software, service, credential, key, or medium that supports business operations or stores/processes/transmits company or customer data. Examples: laptops and phones; cloud resources (projects, VMs, databases, buckets); SaaS applications and licenses; source code repositories; service accounts, API keys, certificates; removable media; and documentation containing confidential information.

Responsibilities by inventory domain:
- Hardware assets (end-user devices, peripherals): Asset Manager (AirCFO) owns issuance/return, inventory accuracy, and lifecycle documentation.
- SaaS/software assets and licenses: Security/GRC (with Finance/airCFO support) maintains the software/SaaS inventory and license ledger, ensures access reviews and DPA alignment with Vendor Management.
- Cloud/platform assets (projects, compute, storage, databases, repos, service accounts): Head of Cloud Infrastructure & Security maintains discovery/reconciliation and supports periodic access reviews.

### Authoritative Systems of Record & Tooling
- Endpoints & compliance: Vanta agent, Google Workspace device management, enterprise Chrome profiles
- Identities & collaboration assets: Google Workspace (Gmail, Drive, Docs/Sheets/Slides)
- Source code & CI/CD: GitHub (repos, Actions runners, secrets), with access controls owned by CTO/DevOps
- Cloud infrastructure: Google Cloud Platform (projects, compute, storage, networking, IAM)
- Finance & spend: Silicon Valley Bank (SVB) statements (for SaaS discovery/reconciliation)
All other assets are managed within these systems unless explicitly documented otherwise.

### Lifecycle States
Assets progress through the following defined states: `New` (procured, not yet issued), `In Service` (assigned and active), `In Repair` (temporarily out of service), `Lost/Stolen` (incident opened; remote wipe/rotation initiated), `Retired` (no longer used; pending disposition), `Disposed` (sanitized/destroyed; COD on file), `Gifted` (transferred to the departing employee post-sanitation). State transitions must be reflected in the inventory within two (2) business days.

Annual Verification: In addition to quarterly reconciliations, a formal annual verification of endpoint assignments and cloud/logical asset ownership is performed with owner attestation.

## **Asset Classification & Labeling**

All assets must be assigned a data classification aligned to company standards (e.g., Public, Internal, Confidential, Restricted). Classification determines required safeguards (encryption, access controls, logging, retention). Labels/tags reflecting classification and ownership must be applied in the inventory and, where supported, on the asset itself (e.g., device labels, repository topics, cloud tags).

Minimum required fields for each asset: `owner`, `custodian`, `environment` (prod/stage/dev), `system/application`, `data_classification`, `contains_pii` (Y/N), and `retention_policy`.

### Classification Levels
- Public: Information intended for public release; no harm if disclosed.
- Internal: Company use only; limited harm if disclosed.
- Confidential: Business sensitive or non-public operational data; material harm if disclosed.
- Restricted: Highly sensitive (e.g., regulated, security credentials); significant harm if disclosed.

## **Cloud Tagging & Naming Standards**

Cloud resources must follow approved naming conventions and include mandatory tags/labels for automated governance and cost allocation. Required tags: `Owner`, `System`, `Environment`, `DataClassification`, `PII`, `CostCenter`. Untagged or noncompliant resources are subject to automated quarantine or removal after notification.

## **SaaS Application Onboarding & Offboarding**

All new SaaS applications must be reviewed prior to use. Minimum requirements: security review, DPA and subprocessor review where applicable, SSO (SAML/OIDC) integration, role-based access, SCIM provisioning/deprovisioning where available, and documented data flows. Approved apps are added to the software/SaaS inventory with an identified owner (e.g., CTO, Head of Cloud Infrastructure, Chief AI Officer, Head of DevOps). Upon deprecation, access is removed, exports performed as needed, and records retained per retention policy.

## **Shadow IT Monitoring & Discovery**
The company monitors for unapproved assets via:
- SSO provider logs and Google Workspace admin reports
- Finance reconciliation using Silicon Valley Bank (SVB) statements and expense reports
- Enterprise Chrome management and device software scans (via Vanta/MDM)
- DNS/proxy telemetry where available

Unapproved assets are reviewed promptly and either onboarded through the standard process or removed.

## **Ownership of Assets**

Assets maintained in the inventory shall be owned by a specific individual or group within Mesh Intelligent Technologies, Inc. Asset owners are accountable for ensuring appropriate classification, access control, and protection throughout the asset lifecycle. Custodians (e.g., IT/Cloud Infrastructure) are responsible for day-to-day safeguards, monitoring, and recordkeeping.

## **Acceptable Use of Assets**

Rules for the acceptable use of information, assets, and information processing facilities shall be identified and documented in the Information Security Policy and Acceptable Use Policy. Users must comply with all signed agreements and company policies when accessing or using company assets.

## **Loss or Theft of Assets**

All Mesh Intelligent Technologies, Inc. personnel must immediately report the loss or suspected theft of any information systems, including portable or laptop computers, smartphones, PDAs, authentication tokens (keyfobs, one-time-password generators, or personally owned smartphones or devices with a Mesh Intelligent Technologies, Inc. software authentication token installed) or other devices that can store and process or help grant access to Mesh Intelligent Technologies, Inc. data.

Personnel must notify IT/Security without delay (target: within 24 hours). IT/Security will initiate remote lock/wipe where feasible, rotate credentials/keys as needed, and open an incident per the Incident Response procedures. Police reports are filed when appropriate.

Reporting channels: security@pieces.app and the Security Hotline (513) 572-3339 for urgent incidents.
Recordkeeping: For confirmed thefts, retain police report numbers and incident tickets alongside inventory entries.

## **Return of Assets**

All employees and third-party users of Mesh Intelligent Technologies, Inc. equipment shall return all organizational assets within their possession upon termination of their employment, contract, or agreement. Returns must occur on or before the final day; in involuntary terminations, assets are collected within 24 hours. IT documents chain of custody, removes devices from MDM, securely sanitizes or reimages devices before re-issue, and updates the inventory.

## **Handling of Assets**

Employees and users who are issued or handle Mesh Intelligent Technologies, Inc. equipment are expected to use reasonable judgment and exercise due care in protecting and maintaining the equipment.

Employees are responsible for ensuring that company equipment is secured and properly attended to whenever it is transported or stored outside of company facilities. Devices must use full-disk encryption, automatic screen locking, and up-to-date security patches. Physical safeguards (e.g., cable locks) are used where appropriate. Sharing of user accounts is prohibited.

All mobile devices shall be handled in accordance with the Information Security Policy. Excepting employee-issued devices, no company computer equipment or devices may be moved or taken off-site without appropriate authorization from management.

Travel & Remote Use: When traveling, devices should not be left unattended in public areas, must be stored in carry-on baggage where possible, and should avoid connecting to untrusted networks without VPN. Border crossings may require additional precautions (e.g., travel devices); consult IT/Security in advance for high-risk destinations.

## **Mobile Devices & BYOD (MDM Requirements)**

Company-issued and BYOD devices used to access company resources must enroll in Mobile Device Management (MDM) prior to access. Minimum controls include: full-disk encryption, screen lock with strong PIN/password/biometric, remote lock/wipe, automatic updates, and malware protection where supported. Corporate data on BYOD must be containerized when feasible and is subject to remote wipe of corporate data upon separation.

BYOD Agreement: Personnel using personal devices for company work must sign the BYOD/MDM consent acknowledging monitoring limited to corporate profiles, the right to remotely wipe corporate data, and adherence to acceptable use requirements. Records of consent are maintained.

## **Endpoint Security Baseline**

All endpoints (company-issued and BYOD accessing company data) must meet the following minimum controls:
- Full-disk encryption enabled (e.g., FileVault on macOS)
- Automatic screen lock with password/biometric
- Supported OS versions (n-1 major, with security updates applied within 30 days of release; critical within 7 days)
- Company-approved endpoint protection (malware detection and behavioral monitoring)
- Enterprise Chrome profile with policy controls when Chrome is used for company access
- Vanta agent installed and healthy for compliance reporting on managed devices

Baseline Hardening: Devices should follow vendor security baselines and applicable CIS recommendations where feasible without impairing business operations (e.g., firewall enabled, disk encryption enforced, automatic updates, restricted kernel extensions).

Browser Extensions: Enterprise Chrome policies enforce an approved list of extensions for business use; unapproved extensions that access company data are blocked.

## **Software Asset Management**

Only approved and licensed software may be installed on company devices. IT maintains a software inventory and license records. Admin privileges are limited to IT or authorized personnel. Software must be kept current; critical security updates are applied within defined patch windows.

End-of-Life/End-of-Support (EOL/EOS): Unsupported software and operating systems are prohibited on production devices and services. Identified EOL/EOS items must be upgraded, replaced, or isolated with compensating controls on a documented timeline (target remediation ≤ 90 days; critical items expedited).

Owner Attestations: Asset owners attest at least quarterly to the accuracy of assigned assets, access appropriateness, and classification correctness.

## **Media Handling**

Removable media use is restricted to approved business purposes. Confidential data stored on removable media must be encrypted. Physical media is stored securely with access limited to authorized personnel. Media is tracked in the inventory where applicable.

## **Cloud & Logical Assets**

Cloud resources (e.g., Google Cloud projects, buckets, databases) and logical assets (e.g., GitHub repositories, API keys, service accounts) are inventoried and assigned owners. Access follows least privilege, with periodic (at least quarterly) reviews. Keys and credentials are rotated per the Information Security Policy. Departed personnel access is revoked immediately upon separation.

Approved Regions & Residency: Cloud resources must be provisioned in approved regions consistent with our Data Residency commitments (e.g., primary in us-east5 unless otherwise approved). Data location choices must be documented where configurable.

## **Keys & Secrets Management**
Secrets (API keys, service account keys, tokens, certificates) must be stored in approved secret managers (e.g., cloud KMS/Secrets Manager) and never in source code or local plaintext. Prefer short‑lived, federated credentials (e.g., GitHub Actions OIDC to mint cloud tokens) over long‑lived static secrets. Rotation follows criticality‑based schedules, with immediate rotation upon compromise or role change. Example cadences: production machine credentials ≤ 90 days; CI/CD tokens ≤ 180 days; certificates per CA policy; human access via SSO/MFA with no shared passwords. Secrets must be linked to their owning system in the inventory.

## **Backup & Snapshot Assets**

Backups and snapshots are considered assets and must be encrypted, inventoried where feasible (scope, retention, location), and protected to the same or higher standard as source data. Retention and restore testing are performed per Business Continuity & Disaster Recovery policy.

## **AI/ML Asset Lifecycle & Governance**

AI/ML assets (models, datasets, embeddings, vector stores, prompts, evaluation sets) are inventoried and classified. Dataset provenance and licensing are documented. Customer personal data is not used for model training; we utilize synthetic and other non‑customer sources in accordance with the AI Governance & Data Policy. Any evaluation or benchmarking that uses customer data must adhere to privacy and contractual commitments and, where applicable, use de‑identified or aggregated data. Access to AI/ML assets is role‑based and logged. Retirement of models/datasets includes removal from serving, revocation of access, and archival or deletion per retention policies. Alignment with the AI Governance & Data Policy is required, including constraints on training data and bias monitoring practices.

## **Asset Disposal & Re-Use**

Company devices and media that stored or processed confidential data shall be securely disposed of when no longer needed. Data must be erased prior to disposal or re-use, using an approved technology in order to ensure that data is not recoverable. A Certificate of Destruction (COD) must be obtained for devices destroyed by a third-party service.

Please refer to NIST Special Publication 800-88 Revision 1 “Guidelines for Media Sanitization” to select appropriate methods. Disposal or re-use actions (method, date, responsible party, COD reference) must be documented in the asset inventory.

Certificates of Destruction and disposal records are retained for at least seven (7) years or the duration required by contract or regulation, whichever is longer.

## **Third-Party & Contractor Assets**

Third-party and contractor personnel accessing company systems must use devices meeting the same control requirements (encryption, patching, MDM where feasible). Where MDM enrollment is not possible, access must occur via approved virtualized workspaces with data egress controls, and must exclude storage of company data on unmanaged endpoints. Contracts must include security obligations and the right to audit. Access is time-bound and reviewed at least quarterly.

## **Procurement & Decommissioning Workflow**

All new hardware purchases are requested through the Asset Manager, recorded in the inventory at order and again at issuance. We do not affix physical asset labels; instead, we track via Apple corporate account/Apple Business Manager, serial numbers, and MDM enrollment linked to assigned personnel. Decommissioning includes backup/transfer as needed, sign-off by owner, inventory status update, and sanitization or vendor RMA with COD retained.

### Gifting Post-Factory Reset
When an employee departs, the company may gift their assigned device to them provided all of the following are completed: (1) full factory reset and MDM unenrollment; (2) verification that all company data, accounts, profiles, and encryption keys are removed; (3) removal from Apple Business Manager/DEP where applicable; (4) inventory updated to state `Gifted` with date and approver; (5) ownership transfer recorded and the device removed from active tracking and support obligations. Gifting may be initiated by any member of the Executive Leadership Team and must be approved by either the CEO (Tsavo Knott) or AirCFO.

## **Temporary/Loaner Assets**

Loaner devices follow the same security baseline (encryption, MDM, standard image). Temporary assignments are time-bound and tracked to the assignee in the inventory. Upon return, devices are reimaged and inventory updated.

## **Evidence & Audit Artifacts**

The following evidence is maintained to demonstrate policy adherence:

- Asset inventory export with required fields and last-updated timestamps
- Quarterly owner attestation records and access review sign-offs
- MDM compliance reports (encryption, lock, OS version, last check-in)
- BYOD consent records and device enrollment logs
- SaaS onboarding reviews (security, DPA) and application inventory
- Cloud tag compliance and discovery/reconciliation reports
- Secrets manager inventory and rotation logs (non-secret metadata)
- Disposal Certificates of Destruction and sanitization logs
- Hardware allocation CSV maintained by AirCFO (device, serial, assignee, dates)

Location of hardware inventory CSV (self-contained reference): `policies/Asset Management Policy/Asset Tracker SOC II - Tracker.csv`
Minimum CSV fields: device type, make/model, serial number, OS version, assignee, assigned date, returned date, status, notes.
Classification: Treat the hardware inventory CSV as Confidential and restrict access to need-to-know personnel.

## **Record Retention for Asset Evidence**

- Asset inventory exports, owner attestations, access reviews: retained ≥ 24 months
- BYOD/MDM consent records: retained for employment duration + 7 years
- Secrets rotation metadata (non-secret): retained ≥ 24 months
- Certificates of Destruction and disposal records: retained ≥ 7 years (or longer if required by contract/regulation)

## **Training & Acknowledgment**

All personnel must review and acknowledge this Asset Management Policy during onboarding and at least annually thereafter. Role-specific training is provided for asset owners and custodians.

## **Customer Asset Return**

Any physical assets owned by customers shall be promptly returned to the customer following service termination in accordance with the terms of contract or service agreement. Chain of custody and shipping records are retained.

## **Roles & Responsibilities**

- CEO (Approver): Final authority on policy approval and material exceptions.
- Corporate Secretary (Policy Owner): Oversees implementation, maintenance, and periodic review of this policy.
- Asset Manager (Katie Storm, AirCFO): Primary owner of the physical and logical asset inventory; enforces MDM; issues/recovers devices; manages software/SaaS licensing; coordinates sanitization/disposal and documentation.
- Cloud Infrastructure SME (Hiro Tamata): Advises on cloud and platform asset discovery and reconciliation; ensures cloud inventory alignment with responsibility matrices and supports access reviews.
- CTO (Mark Widman): Oversees asset standards for engineering platforms (cloud, source control, build systems) and approves exceptions with CEO.
- Chief AI Officer (Sam Jones): Defines AI/ML asset classification standards (models, datasets, embeddings, vector stores) and lifecycle requirements.
- Head of CI/CD & DevOps (Nathan Courtney): Ensures CI/CD platform assets (runners, secrets, artifact stores) are inventoried, access-controlled, and monitored; enforces signing and provenance (SBOM, attestations).
- All Personnel: Safeguard assigned assets, follow acceptable use, and promptly report loss/theft or damage.

# **Exceptions**

Requests for an exception to this policy must be submitted to the Corporate Secretary and Head of Cloud Infrastructure for review. Material or time-bound exceptions require approval by the CEO (Tsavo Knott). Exceptions must document scope, compensating controls, and expiration.

# **Violations & Enforcement**

Any known violations of this policy should be reported to IT/Security or the Corporate Secretary. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## **References**

- Information Security Policy; Acceptable Use Policy; Incident Response Procedures
- Legal & Security Policies (Customer-Facing) – Encryption, Access Controls, Vendor Management, AI Governance & Data Policy, BCP/DR (Backups)
- NIST SP 800-88 Rev. 1 – Media Sanitization
 - ISO/IEC 27001 Annex A controls for Asset Management and Operations
 - Vendor & Third-Party Management Policy (SaaS onboarding, DPA alignment)

## **TSC Mapping**

- CC1.1, CC1.2, CC1.4, CC2.2, CC6.1, CC6.2, CC6.6

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| 1.0 | 14-Dec-2022 | First Version | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |

---