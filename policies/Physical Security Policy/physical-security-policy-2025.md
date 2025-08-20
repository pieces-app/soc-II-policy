---
title: Physical Security Policy
owner:
  - Katie Storm (AirCFO - HR, Policy Owner)
  - Mack Myers (Corporate Secretary & CPO, Co-Owner)
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC6.x (Logical and Physical Access Controls)
    - ISO/IEC 27001 Annex A.11 (Physical and Environmental Security)
  procedures:
    - Visitor Management Procedure
    - Facility Access Review Procedure
    - Shipping & Receiving Procedure
repo: https://github.com/pieces-app/soc-II-policy
---

# Physical Security Policy

**Policy Owner:** Katie Storm (AirCFO - HR), Mack Myers (Corporate Secretary & CPO)

**Effective Date:** August 19, 2025

# Purpose

To prevent unauthorized physical access or damage to the organization's information and information processing facilities.

# Scope

All Mesh Intelligent Technologies, Inc. offices and locations, including our headquarters at 1311 Vine Street, Unit 301, Cincinnati, Ohio (within Union Hall managed by Centrifuse). As a remote-first company, this policy emphasizes device-level physical security controls for our distributed workforce. This policy applies to all employees of Mesh Intelligent Technologies, Inc., and to all external parties with physical access to Mesh Intelligent Technologies, Inc. owned or leased facilities. Where Mesh Intelligent Technologies, Inc. utilizes third-party office providers or shared/coworking spaces, the provider's physical security controls are assessed and governed under the Third-Party Management Policy, and this policy applies to our obligations and internal procedures.

# Policy

## Remote-First Device Security

As a remote-first organization, physical security primarily occurs at the device level. All company devices and employee-owned devices accessing company data must implement:
- Automatic screen lock (≤ 5 minutes of inactivity) with strong authentication (biometric or complex password)
- Full-disk encryption (FileVault on macOS, BitLocker on Windows, or equivalent) - AES-256 standard per Legal Policy §5.2
- Multi-factor authentication (MFA) for all company accounts, with preference for phishing-resistant factors (hardware security keys/WebAuthn/FIDO2)
- Password-protected hardware/firmware where available, including hardware security modules where supported
- Device tracking and remote wipe capabilities (Find My Mac, Google Workspace MDM, GitHub device management, Vanta agent)
- Regular OS and security updates applied within defined timelines (critical: ≤ 72 hours, high: ≤ 7 days, medium: ≤ 30 days per Legal Policy §5.7)
- VPN requirements for secure remote access to company resources
- Endpoint detection and response (EDR) tools where deployed

Employees working from home or remote locations must:
- Secure devices when unattended (locked room or cabinet)
- Position screens away from public view
- Use privacy screens in public spaces when handling Confidential/Restricted data
- Report lost or stolen devices immediately (within 2 hours of discovery) to enable remote wipe
- Maintain secure home network configurations (WPA2/WPA3, strong passwords, updated firmware)
- Prohibit use of public WiFi for accessing Confidential data without VPN
- Follow clean desk policy for printed materials containing company data

## Physical Security Perimeter

Our headquarters at Union Hall benefits from building-provided security controls including badge access, front desk management, and common area surveillance. Physical offices and processing facilities shall meet all local building codes for construction materials for walls, windows, doors, and access control mechanisms. Some interior zones may be identified as secure areas where physical access is further restricted to a subset of Mesh Intelligent Technologies, Inc. personnel; such as private offices, wiring closets, print and server rooms, and server racks. Physical security designs must consider theft, misuse, environmental threats, and unauthorized access.

## Physical Entry Controls

Secure areas shall be protected by appropriate entry controls to ensure that only authorized personnel are allowed access. At our Cincinnati headquarters, we rely on Union Hall/Centrifuse building-provided access controls, supplemented by our internal procedures. Where feasible, Mesh Intelligent Technologies, Inc. access control systems shall be tied to a centralized system that provides granular access control for individual personnel. Access events shall be appropriately logged and reviewed according to risk. Cameras and intrusion detection systems shall be used at facilities that store or process production or sensitive internal company data, where feasible.

Minimum requirements:
- Individual, revocable credentials for each authorized person (building-provided badges at Union Hall)
- Prompt deprovisioning of access (target ≤ 24 hours) upon role change or separation
- Periodic (at least semiannual) review of facility access lists by the Policy Owner or delegate
- Exception reports from building management requested only when security incidents or concerns arise
- Access logs retained for at least 1 year where available; video surveillance per building provider standards

## Securing Offices, Rooms & Facilities

Physical security for offices, rooms and facilities shall be designed and applied to protect from theft, misuse, environmental threats, unauthorized access, and other threats to the confidentiality, integrity, and availability of classified data and systems. Sensitive assets (e.g., spare laptops, security tokens) shall be stored in locked cabinets or rooms with restricted access.

## Protecting Against External & Environmental Threats

Physical protection against natural disasters, malicious attack or accidents shall be designed and applied. Secure areas shall be monitored through the use of appropriate controls, such as intrusion detection systems, alarms, and/or video surveillance systems, where feasible. Visitor and third-party access to secure areas shall be restricted to reduce the risk of information loss and theft.

Production processing facilities (including cloud infrastructure) shall be equipped with appropriate environmental and business continuity controls:
- Fire-suppression systems and smoke detection
- Climate control and monitoring systems (temperature/humidity)
- Emergency backup power systems (UPS and generators)
- Water damage detection and prevention systems
- Physical intrusion detection and alerting

Physical information system hardware and supporting infrastructure shall be regularly serviced and maintained in accordance with the manufacturer's recommendations. For cloud infrastructure, we rely on Google Cloud Platform's SOC 2, ISO 27001, and FedRAMP certified data centers (per Legal Policy §5.1) which provide enterprise-grade physical security including:
- 24/7 security personnel and surveillance
- Multi-factor physical access controls
- Environmental monitoring and redundant systems
- Geographic redundancy across multiple availability zones (us-east5 Ohio region per Legal Policy §7.1)

## Working in Secure Areas / Visitor Management

Visitors, delivery personnel, outside support technicians, and other external agents shall not be permitted access to secure areas without escort and/or appropriate oversight. Visitor management is handled digitally through calendar invitations and Union Hall front desk procedures. Third-parties in secure areas shall be escorted or monitored by Mesh Intelligent Technologies, Inc. personnel. Mesh Intelligent Technologies, Inc. personnel observing unescorted visitors should approach the visitor, confirm their status, and ensure they return to approved areas, or report the observation to the responsible authority as needed. External party access to secure areas shall be confirmed with appropriate Mesh Intelligent Technologies, Inc. personnel prior to being granted access. Mesh Intelligent Technologies, Inc. personnel providing access to external parties into secure areas are responsible for ensuring that the third-party personnel adhere to all security requirements, and are accountable for all actions taken by outsiders they provide with access. Visitors may be allowed to work unescorted provided that the Mesh Intelligent Technologies, Inc. sponsoring party can ensure that they will not have unauthorized access to Mesh Intelligent Technologies, Inc. information systems, networks, or data.

Minimum requirements:
- Visitor identity verified; visitors wear visible identification while onsite
- Digital visitor logs maintained through calendar systems and building front desk records
- Deliveries and contractors pre-authorized; escorted for work in secure areas

## Delivery & Loading Areas

Access points such as delivery and loading areas and other points where unauthorized persons could enter secure areas shall be controlled and, if possible, isolated from information processing facilities to avoid unauthorized access.

Shipping and receiving procedures:
- Pre-authorization required for all technology deliveries
- Verification of sender/recipient for sensitive equipment
- Inspection of packages for tampering or damage
- Chain-of-custody documentation for devices containing Confidential/Restricted data
- Secure storage of received items pending distribution
- Shipping and receiving records maintained for at least 1 year

For remote employees:
- Direct shipment to employee addresses with tracking and signature confirmation
- Return shipping labels provided for device returns with monitored tracking
- Secure packaging requirements for devices containing company data
- Immediate device collection upon termination (≤ 24 hours notification)

## Supplier, Vendor, and Third-Party Security

Suppliers, vendors, and third-parties shall comply with Mesh Intelligent Technologies, Inc. physical security and environmental controls requirements. Mesh Intelligent Technologies, Inc. shall assess the adequacy of third-party physical security controls as part of the vendor management process, in accordance with the Third-Party Management Policy. This includes periodic assessment of Union Hall/Centrifuse security controls and any other coworking or office space providers used by employees.

## Business Continuity & Physical Resilience

In alignment with Legal Policy §4 (Business Continuity & Disaster Recovery), physical security measures support our recovery objectives:
- Recovery Time Objective (RTO): 4 hours for core services restoration
- Recovery Point Objective (RPO): Maximum 24-hour data loss in catastrophic events
- Multi-Availability Zone architecture with automatic failover (GCP us-east5)
- Encrypted daily backups in geographically separate locations
- Quarterly restore testing to verify recoverability

Physical incident response procedures:
1. Detection & Classification: Immediate assessment of physical security incidents
2. Containment: Isolation of affected areas/devices, remote wipe if necessary
3. Recovery: Restoration from verified clean backups with integrity validation
4. Post-Incident Analysis: Root cause determination and preventive measures

Emergency response capabilities:
- 24/7 security incident hotline: (513) 572-3339 (critical incidents only)
- Executive escalation: tsavo@pieces.app
- Cyber insurance notification: CFO contacts At-Bay Specialty Insurance Company within 24 hours for covered incidents
- Status page updates for service disruptions
- Regulatory notifications within 72 hours for GDPR if personal data impacted

## Roles & Responsibilities

- Policy Owner (Katie Storm, AirCFO - HR): Overall policy governance, annual review, coordination of physical security audits, and semiannual access list reviews.
- Co-Owner (Mack Myers, Corporate Secretary & CPO): Policy compliance oversight and coordination with Vanta platform.
- Head of Cloud Infrastructure (Hiro Tamada): Physical security assessments for data center and cloud providers, ensuring alignment with SOC 2 Type II requirements (per Legal Policy §5.1).
- Security/GRC Team: Maintains security monitoring systems, coordinates incident response, manages Vanta compliance platform for continuous monitoring (per Legal Policy §5.3).
- IT/Engineering: Manages device security configurations, MDM deployment, remote wipe procedures, and VPN access.
- Chief Technology Officer (Mark Widman): Approves physical security architecture and major control changes.
- Head of CI/CD & DevOps (Nathan Courtney): Ensures secure deployment practices and infrastructure hardening.
- All Personnel: Comply with this policy, complete annual security awareness training (per Legal Policy §5.8), and report suspicious activity or violations promptly to security@pieces.app.

## Assurance & Evidence (Audit Readiness)

Mesh Intelligent Technologies, Inc. maintains the following evidence for SOC 2 Type II compliance:
- Facility access lists with semiannual review attestations (aligned with Legal Policy §5.8)
- Building provider security assessments and contracts (Union Hall/Centrifuse) with SOC 2/ISO 27001 attestations where available
- Digital visitor logs through calendar systems and building front desk records (retained ≥ 1 year)
- Shipping and receiving records with chain-of-custody documentation (≥ 1 year retention)
- Device security configurations tracked in Vanta (per Legal Policy §5.3):
  - Encryption status (AES-256 full-disk encryption per Legal Policy §5.2)
  - MDM enrollment and compliance status
  - Remote wipe capability verification
  - Patch compliance (critical: ≤ 72 hours per Legal Policy §5.7)
- Lost/stolen device incident reports with:
  - Time of discovery and notification (target ≤ 24 hours per Legal Policy §5.5)
  - Remote wipe confirmation logs
  - Post-incident analysis and preventive measures (per Legal Policy §4.4)
- Employee attestations:
  - Annual security awareness training completion (per Legal Policy §5.8)
  - Remote work security requirements acknowledgment
  - Clean desk policy compliance
  - Device security configuration verification
  - Background verification records where applicable (per Legal Policy §5.8)
- Physical security testing:
  - Annual review of building security controls
  - Bi-annual tabletop exercises for physical incidents (per Legal Policy §4.6)
  - Quarterly review of device compliance metrics
  - Annual third-party assessments where applicable (per Legal Policy §5.7)

## Exceptions

Requests for an exception to this policy must be submitted to the Policy Owner for review and approved by the CEO (Tsavo Knott). Exceptions must define:
- Specific requirement being excepted
- Business justification and risk assessment
- Compensating controls to mitigate risk (aligned with Legal Policy §5.3 principle of least privilege)
- Exception duration (maximum 12 months)
- Exception owner and review schedule

All exceptions are tracked in GitHub and reviewed quarterly. Exceptions for Confidential data on portable/removable media require additional approval from the Chief Technology Officer and are strictly limited to specific business-critical scenarios with documented encryption (AES-256) and tracking requirements.

## Violations & Enforcement

Any known violations of this policy should be reported to the Policy Owner or security@pieces.app. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## References

- Third-Party Management Policy
- Asset Management Policy
- Data Management Policy
- Access Control Policy
- Cryptography Policy
- Incident Response Plan

## Change Log

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 14-Dec-2022 | First Version | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 01-Jan-2023 | 2023 Update | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.2.0 | 19-Aug-2025 | 2025 Refresh | Operations & Security | Tsavo Knott (CEO) |


