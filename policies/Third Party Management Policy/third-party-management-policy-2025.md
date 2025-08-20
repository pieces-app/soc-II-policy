---
id: POL-0003
title: Third-Party Management Policy
owner:
  - Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.)
  - Security/GRC
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards: []
  procedures: []
  controls: []
repo: https://github.com/pieces-app/soc-II-policy
---

# **Third-Party Management Policy** 

**Policy Owner:** Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.), Security/GRC

**Effective Date:** August 19, 2025 

# **Purpose** 

To ensure protection of Mesh Intelligent Technologies, Inc.'s data and assets that are shared with, accessible to, or managed by suppliers, including external parties or third-party organizations such as service providers, vendors, and customers, and to maintain an agreed level of information security and service delivery in line with supplier agreements.

This document outlines a baseline of security controls that Mesh Intelligent Technologies, Inc. expects partners and other third-party companies to meet when interacting with Mesh Intelligent Technologies, Inc. Confidential data.

# **Scope** 

All data and information systems owned or used by Mesh Intelligent Technologies, Inc. that are business critical and/or process, store, or transmit Confidential data. This policy applies to all employees of Mesh Intelligent Technologies, Inc. and to all external parties, including but not limited to Mesh Intelligent Technologies, Inc. consultants, contractors, business partners, vendors, suppliers, partners, outsourced service providers, and other third-party entities with access to Mesh Intelligent Technologies, Inc. data, systems, networks, or system resources.

# **Policy**

## **Roles & Responsibilities**

- Corporate Secretary (Mack Myers): Owns vendor governance, contract security terms, recordkeeping, and approval workflow.
- Security/GRC (function): Performs security due diligence, risk tiering, reviews external audit reports, and defines compensating controls. Contact: security@pieces.app.
- System Owners/Requestors: Define intended use, data types, required permissions, and ensure least-privilege access.
- HR (airCFO): Co-approves HR/finance-related vendors and ensures agreements align with onboarding/offboarding processes.
- Head of Cloud Infrastructure & Security (Hiro Tamada): Owns cloud service security posture, CSP responsibility-matrix controls, and technical validation of vendor security integrations (SSO/MFA, logging, network, encryption).
- CTO (Mark Widman): Approves security architecture for strategic vendors, oversees AI/ML vendor governance and native/client security, and adjudicates compensating controls for time-sensitive implementations.

Information security requirements for mitigating the risks associated with supplier's access to the organization's assets shall be agreed with the supplier and documented.

For all service providers who may access Mesh Intelligent Technologies, Inc. Confidential data, systems, or networks, proper due diligence shall be performed prior to provisioning access or engaging in processing activities. Information shall be maintained regarding which regulatory or certification requirements are managed by or impacted by each service provider, and which are managed by Mesh Intelligent Technologies, Inc. as required. Applicable regulatory or certification requirements may include ISO 27001, SOC 2, PCI DSS, CCPA, GDPR or other frameworks, compliance standards, or regulations.

# **Information Security in Third-Party Relationships**

## **Addressing Security in Agreements**

Relevant information security requirements shall be established and agreed upon with each supplier that may access, process, store, transmit, or impact the security of Confidential data and systems, or provide physical or virtual IT infrastructure components for Mesh Intelligent Technologies, Inc.

For all service providers who may access Mesh Intelligent Technologies, Inc. production systems, or who may impact the security of the Mesh Intelligent Technologies, Inc. production environment, written agreements shall be maintained that include the service provider's acknowledgment of their responsibilities for the confidentiality of company and customer data, and any commitments regarding the integrity, availability, and/or privacy controls that they manage in order to meet the standards and requirements that Mesh Intelligent Technologies, Inc. has established in accordance with Mesh Intelligent Technologies, Inc.’s information security program or any relevant framework.

## **Technology Supply Chain**

Mesh Intelligent Technologies, Inc. will consider and assess risk associated with suppliers and the technology supply chain. Where warranted, agreements with suppliers shall include requirements to address the relevant information security risks associated with information and communications technology services and the product supply chain.

## **Vendor Risk Tiering**

Vendors are classified by inherent risk using the following criteria: data sensitivity (e.g., customer data, PII), system criticality, production access, and transaction volume.

- High risk: Access to production systems, customer data, or Confidential data at scale (e.g., cloud/IaaS, IdP, core security tooling). Reassess at least annually and upon a material change.
- Medium risk: Access to limited Confidential data or internal systems with moderate impact (e.g., HRIS, CRM). Reassess at least every 2 years and upon material change.
- Low risk: No access to Confidential data or production systems (e.g., marketing utilities). Reassess on contract renewal or material change.

AI/ML and LLM providers are further evaluated on: model/data usage practices, dataset provenance, evaluation rigor (safety, bias, privacy), prompt/abuse safeguards, and subprocessor GPU/region dependencies.

## **Due Diligence & Security Requirements by Tier**

Prior to access or data sharing, the following evidence is requested proportionate to vendor risk:

- External assurance: SOC 2 Type II report or ISO 27001 certificate (high/medium); SOC 3 or other attestation (low as applicable).
- Technical posture: Penetration test summary (last 12 months), vulnerability management policy/cadence, encryption at rest/in transit, MFA for administrative access, SSO support.
- Privacy & data handling: Data Processing Agreement (if processing personal data), subprocessor list and change notification process, data location/regions, data retention/deletion timelines, breach notification commitments.
- Operational controls: Incident response summary, business continuity/disaster recovery statements, logging/monitoring practices.
- Contractual terms: Right to audit/review security reports, 72-hour breach notification (or sooner if required by law), termination assistance and certified data deletion upon request.

Compensating controls may be applied (e.g., limited scope integrations, tokenization, additional monitoring) where a vendor cannot meet a requirement and the residual risk is acceptable.

## **AI/ML and LLM-Specific Requirements**

When engaging AI/ML or LLM providers or features, Mesh Intelligent Technologies, Inc. requires proportionate controls in addition to baseline due diligence:

- Data usage & retention
  - No training on Mesh Intelligent Technologies, Inc. proprietary or customer data without explicit written approval; default is opt-out from model training and analytics beyond service provision.
  - Clear data retention and deletion timelines; ability to request deletion and receive confirmation within 30 days.
  - Separation of customer/tenant data; confidentiality protections in inputs, outputs, and logs. Redaction of sensitive data in logs where feasible.
- Privacy & legal
  - Executed Data Processing Agreement (if processing personal data), including subprocessor transparency and change notifications.
  - Cross-border data transfer safeguards and declared data residency/regions.
- Security & access
  - SSO/MFA for console and administrative access; role-based permissions; customer-scoped API keys; rate limiting and abuse prevention.
  - Encryption in transit and at rest for prompts, embeddings, and outputs; key management disclosures.
- Model governance & evaluations
  - Provider documentation (e.g., model card or equivalent) including intended use, limitations, and evaluation summaries.
  - Evidence of safety, privacy, and bias testing appropriate to use case; disclosure of jailbreak mitigations and content filtering.
  - Dataset provenance statements for training and fine-tuning; licensing and IP compliance representations.
- Supply chain & operations
  - Disclosure of material subprocessors (including GPU/accelerator providers) and geography.
  - Incident notification within 72 hours (or sooner where required) with commitments to share scope, data impacted, and mitigations.
- Self-hosted/open-source models
  - Container/image provenance and vulnerability scanning; timely patching cadence.
  - Network isolation and egress controls; no external telemetry collection unless approved by Security/GRC.

# **Third-Party Service Delivery Management**

## **Monitoring & Review of Third-Party Services**

Mesh Intelligent Technologies, Inc. shall regularly monitor, review, and audit supplier service delivery. Supplier security and service delivery performance shall be reviewed at least annually.

Ongoing activities include: calendar-based reassessments per tier; review of SOC/ISO reports and remediation of noted exceptions; monitoring of incident disclosures; review of subprocessor updates; and verification of continued need for access.

## **Management of Changes to Third-Party Services**

Changes to the provision of services by suppliers, including changes to agreements, services, technology, policies, procedures, or controls, shall be managed, taking account of the criticality of the business information, systems, and processes involved. Mesh Intelligent Technologies, Inc. shall assess the risk of any material changes made by suppliers and make appropriate modifications to agreements and services accordingly.

# **Third-Party Risk Management**

Mesh Intelligent Technologies, Inc. will ensure that potential risks posed by sharing Confidential data or providing access to company systems are identified, documented and addressed according to this policy. Risk management plays an integral part in the governance and management of the organization at a strategic and operational level. The purpose of a partner and third-party security policy is to ensure that partnerships and services achieve their business plan aims and objectives, and are consistent with Mesh Intelligent Technologies, Inc.’s requirements for information security.

Mesh Intelligent Technologies, Inc. shall not share or transmit Confidential data to a third-party without first performing a third-party risk assessment and fully executing a written contract, statement of work or service agreement which describes expected service levels and any specific information security requirements.

## **Vendor Onboarding & Access Provisioning**

- Initiation: Requestor documents intended use, data types, and access needs; Security/GRC assigns a risk tier.
- Assessment: Due diligence collected proportionate to tier; gaps and compensating controls documented by Security/GRC.
- Approval: Corporate Secretary and Security/GRC approve access; HR (airCFO) co-approves HR/finance vendors.
- Provisioning: Least-privilege access granted only after approvals and contract execution; inventory updated.

## **Vendor Offboarding & Data Return/Deletion**

- Access removal: Vendor access to systems and data is revoked within 24 hours of contract termination or when no longer needed.
- Asset/data handling: Vendor returns or deletes company data per contract; certificate of destruction obtained when applicable within 30 days.
- Inventory update: Vendor inventory and records updated to reflect termination and evidence archived.

# **Information security for use of cloud services**

This section outlines the fundamental parameters for managing and mitigating risks related to cloud service usage. 

Responsibilities and Risk Management:

* Roles and responsibilities related to the use and management of cloud services can be found in the *Roles and Responsibilities Policy*.  
* Information security risks associated with cloud services use shall be managed in accordance with this policy and the *Risk Management Policy*.

Security Requirements and Control:

* Mesh Intelligent Technologies, Inc. shall be responsible for all customer controls as defined in cloud service providers’ responsibility matrices.

Service Selection and Usage Scope:

* Reviews of cloud service agreements for inherently high risk providers shall be performed annually to ensure they align with company requirements. 

Incident Management:

* Information security incidents related to cloud services are managed in accordance with the Incident Response Plan. 

Service Review and Exit Strategy:

* Risks related to exit and vendor lock-in should be evaluated prior to the acquisition as part of the vendor security assessment.

Provider and Customer Agreement:

* Agreements with cloud service providers will specify protections for Mesh Intelligent Technologies, Inc.’s data and service availability, even though they might be predefined and non-negotiable.  
* Where possible, Mesh Intelligent Technologies, Inc. will seek advance notification from providers concerning substantive changes in service delivery, including changes in technical infrastructure, data storage location, or usage of sub-contractors.

Ongoing Management and Assurance:

* Information regarding how to obtain and utilize information security capabilities provided by the cloud service provider should be assessed as part of the vendor review at time of acquisition.

## **Ongoing Monitoring & Reassessment**

- Reassess vendors per risk tier cadence and upon material change (e.g., incident, service scope change, subprocessor change).
- Review audit reports and track remediation; document exceptions and compensating controls.
- Confirm continued need for access and adjust permissions per least-privilege.

# **Third-Party Security Standards**

All third-parties must maintain reasonable organizational and technical controls as assessed by Mesh Intelligent Technologies, Inc.

Assessment of third-parties which receive, process, or store Confidential data or access Mesh Intelligent Technologies, Inc.’s resources shall consider the following controls as applicable based on the service provided and the sensitivity of data stored, processed or exchanged.

## **Information Security Policy**

Third-parties maintain information security policies supported by their executive management, which are regularly reviewed.

## **Risk Assessment & Treatment**

Third-parties maintain programs that assess, evaluate, and manage information and technology risks. 

## **Operations Security**

Third-parties implement commercially reasonable practices and procedures designed, as appropriate, to maintain operations security. Protections may include:

* Technical testing  
* Protection against malicious software  
* Network protection and management  
* Technical vulnerability management  
* Logging and monitoring  
* Incident response  
* Business continuity planning

## **Access Control**

Third-parties maintain a technical access control program.

## **Secure System Development**

Third-parties maintain a secure development program consistent with industry software and systems development best practices including risk assessment, formal change management, code standards, code review and testing.

## **Physical & Environmental Security**

If third-parties are storing or processing confidential data, their physical and environmental security controls should meet the requirements of the Mesh Intelligent Technologies, Inc. Physical Security Policy[^1].

## **Human Resources**

Third-parties maintain human resource policies and processes which include criminal background checks for any employees or contractors who access Mesh Intelligent Technologies, Inc. confidential information.

## **Compliance & Legal**

Mesh Intelligent Technologies, Inc. shall consider all applicable regulations and laws when evaluating suppliers and third parties who will access, store, process or transmit Mesh Intelligent Technologies, Inc. confidential data.  Third-party assessments should consider the following criteria:

* Protection of customer data, organizational records, and records retention and disposition  
* Privacy of Personally Identifiable Information (PII)

# **Exceptions**

Requests for an exception to this policy must be submitted to the Corporate Secretary (Mack Myers) and Security/GRC for approval. Material exceptions require approval by the CEO (Tsavo Knott). Exceptions are time-bound and reviewed upon or before expiration.

# **Violations & Enforcement**

Any known violations of this policy should be reported to the Corporate Secretary (Mack Myers) or Security/GRC. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment. 

## **References**
- Vendor inventory and assessments: Vanta Vendor Management module (contact: Mack Myers)
- Contracts and security addenda: Google Drive data room (contact: Mack Myers)
- DPA and privacy terms: Contract repository (contact: Mack Myers)
- AI/LLM vendor evaluations and evidence: Maintained by Head of Cloud Infrastructure & Security (Hiro Tamada) with oversight by CTO (Mark Widman)
- Security/GRC contact: security@pieces.app 

## **TSC Mapping**
- CC1.2 (Oversight), CC2.2 (Communication), CC3.2–CC3.4 (Risk Assessment), CC5.2 (Access), CC7.2 (Training)

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :---: | :---: | :---: |
| 1.0.0 | 14-Dec-2022 | First Version | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | Mesh-specific vendor governance, tiering, due diligence, onboarding/offboarding, monitoring | Executive Leadership | Tsavo Knott (CEO) |
|  |  |  |  |  |

[^1]:  This is a reference to another Vanta policy. If you are not planning on using this policy, describe your company’s physical and environmental security controls here.


