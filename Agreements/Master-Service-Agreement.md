<!-- 
MASTER SERVICE AGREEMENT TEMPLATE
This MSA establishes the framework for ongoing services between Pieces and enterprise customers.
Individual projects/engagements are governed by separate Statements of Work (SOWs) under this MSA.

Key Features:
- Ongoing framework (not time-limited)
- Supports multiple SOWs and projects
- Production-level SLAs and support
- Enterprise-grade terms and conditions
- Flexible commercial models

Fields to complete:
- Customer Legal Name: Full legal entity name
- Jurisdiction: Country/State of incorporation
- Dates: MM/DD/YYYY format
- Initial SOW details (if applicable)
- Contact information for notices
-->

# MASTER SERVICE AGREEMENT

**Effective Date:** _____________________

**Between:**  
**Mesh Intelligent Technologies, Inc. (d/b/a pieces.app)**, a Delaware corporation with principal place of business at 1311 Vine Street, Unit 301, Cincinnati, Ohio 45202, USA ("**Provider**" or "**Pieces**")  

and  

**_______________________________________**, organized under the laws of _____________________ ("**Customer**")

Each a "**Party**" and collectively the "**Parties**"

**Governing Law:** Delaware law. **Venue:** Exclusive jurisdiction and venue in the state and federal courts located in Delaware, USA. The U.N. Convention on Contracts for the International Sale of Goods does not apply.  

**Billing & Merchant of Record:** Payments are processed by **Paddle.com, Inc.** (US) or **Paddle.com Market Ltd** (UK), as applicable (collectively, "**Paddle**"), acting as **Merchant of Record**. Provider will assist Customer in resolving any payment or tax-related issues with Paddle in a timely manner.

This Master Service Agreement (the "**Agreement**" or "**MSA**") establishes the framework under which Provider will provide services to Customer pursuant to one or more Statements of Work, Order Forms, or Service Orders (each, a "**SOW**").

---

## 1. SERVICES AND DELIVERABLES

**1.1 Services.** Provider will provide Customer with access to its **Pieces for Developers** platform, including:
- Native desktop applications (macOS, Windows, and Linux)
- Cloud capabilities and synchronization
- API access and integrations
- Single Sign-On (SSO) and identity management
- Any additional services specified in applicable SOWs
(collectively, the "**Services**")

**1.2 Statements of Work.** Each SOW will specify:
- Specific services and deliverables
- Project timelines and milestones
- Pricing and payment terms specific to that SOW
- Acceptance criteria (if applicable)
- Project-specific terms that supplement this MSA

**1.3 Professional Services.** Provider may provide implementation, customization, training, and consulting services as specified in applicable SOWs ("**Professional Services**").

**1.4 Service Levels.** Provider will maintain the Service Level Agreements specified in Exhibit B and any SOW-specific SLAs. Provider's failure to meet the critical SLA thresholds (as defined in Exhibit B) for three (3) consecutive months, or for a majority of months in a contract term of less than one year, shall constitute a material breach, entitling Customer to terminate the applicable SOW for cause with thirty (30) days written notice and receive a pro-rated refund of any prepaid fees for the unused term. Service credits will be applied to future invoices and do not result in cash refunds. For the avoidance of doubt, this SLA-specific termination right is in addition to, and does not require, the general 30-day cure period specified in Section 11.3, as SLA failures are measured over multi-month periods and cannot be "cured" retroactively.

---

## 2. COMMERCIAL TERMS

**2.1 Fees.** Customer will pay fees as specified in each SOW. Unless otherwise specified:
- **Subscription Fees:** Based on per-user-per-month pricing
- **Professional Services:** Time and materials or fixed fee as specified
- **Support Tiers:** As selected by Customer in applicable SOWs

**2.2 Payment Terms.** 
- **Billing Cycle:** Quarterly in advance for subscriptions (unless otherwise specified in SOW)
- **Payment Terms:** Net 30 days from invoice date
- **Currency:** USD unless otherwise agreed
- **Method:** Via Paddle as Merchant of Record

**2.3 Taxes.** Fees are **exclusive** of all taxes, duties, levies, and similar governmental assessments ("**Taxes**"). As Merchant of Record, **Paddle will calculate, collect, and remit applicable Taxes**. If Customer is tax-exempt, Customer must provide valid exemption certificates to Paddle prior to payment. For any required withholding, the parties will cooperate in good faith to minimize withholding taxes and provide necessary documentation. Customer will only gross-up payments if legally required after such cooperation.

**2.4 Late Payment.** Overdue amounts accrue interest at the lesser of 1.5% per month or the maximum allowed by law. Provider may suspend Services for invoices more than 30 days overdue after written notice, except where the overdue amount is subject to a good faith dispute. Services will be reinstated promptly upon payment or resolution of the dispute.

**2.5 Disputes.** Customer must dispute charges in writing within 30 days of the invoice date, providing detailed reasons. Undisputed amounts remain due.

---

## 3. LICENSE AND SEAT MANAGEMENT

**3.1 License Grant.** Subject to this Agreement and payment of fees, Provider grants Customer a non-exclusive, non-transferable license to use the Services during the Term for Customer's internal business purposes. Notwithstanding the foregoing, Customer may transfer the license in connection with a merger, acquisition, or sale of substantially all assets, with prior written notice to Provider.

**3.2 User Management.** 
- Customer may add users at any time (pro-rated charges apply)
- Seat reductions take effect at the next renewal period
- Customer may reassign seats among authorized users
- Usage reports available upon request

**3.3 Authorized Use.** The Services are licensed for use by Customer's employees and authorized contractors who have agreed to confidentiality terms no less protective than those herein.

**3.4 Restrictions.** Customer will not:
- Reverse engineer or attempt to derive source code
- Remove proprietary notices
- Use the Services to build competitive products
- Exceed licensed usage limits
- Share access credentials
- Use for illegal purposes or in violation of the Acceptable Use Policy (Exhibit D)

---

## 4. SUPPORT AND MAINTENANCE

**4.1 Support Tiers.** Provider offers multiple support tiers as detailed in Exhibit B:
- **Standard Support:** Business hours support via email and GChat/Discord/Slack/Teams
- **Premium Support:** Extended hours with priority response
- **Enterprise Support:** 24/7 support with dedicated resources

**4.2 Maintenance.** Provider will:
- Provide regular updates and patches
- Conduct scheduled maintenance with advance notice
- Minimize service disruptions
- Maintain backward compatibility where feasible

**4.3 Communication Channels.** Based on Customer's selected support tier:
- Dedicated Slack/Discord/Teams/Google Chat channel for Premium and Enterprise
- Email support for all tiers
- Cell phone emergency contact for Enterprise tier
- Access to knowledge base and documentation

---

## 5. DATA PROTECTION AND SECURITY

**5.1 Data Ownership.** Customer retains all rights, title, and interest in Customer Data. Provider has a limited license to process Customer Data solely to provide the Services, including ephemeral cloud processing for AI features as configured by Customer.

**5.2 Data Processing.** Provider will:
- Process Customer Data in accordance with Customer's instructions and configuration preferences
- Use cloud processing for AI/LLM features only as authorized (blended mode, SSO-locked, BYOK, or disabled)
- **Air-Gapped Mode Clarification:** A 100% on-device air-gapped mode is available **only** when using local SLMs with **no** cloud LLMs and **no** BYOK. BYOK configurations **require** Provider's cloud proxy services and are therefore **not** air-gapped. BYOK traffic will transit Provider's cloud proxy infrastructure even when Customer supplies its own LLM API keys. Customer acknowledges that BYOK data will transit Provider's cloud infrastructure even when using Customer's own LLM API keys. Provider will notify Customer of any changes to the technical architecture that may affect data residency or security. If Customer's regulatory requirements change and cannot be met due to this limitation, Customer may terminate the affected SOW with a pro-rated refund.
- Not retain ephemerally processed data in cloud infrastructure after processing completion
- Implement appropriate technical and organizational security measures
- Maintain industry-standard information security practices
- Execute a separate Data Processing Agreement (DPA) upon request

**5.3 Security Measures.** Provider maintains comprehensive security measures including:
- Encryption in transit (TLS 1.2+) and at rest (AES-256)
- Multi-factor authentication
- Regular security assessments and penetration testing
- Vulnerability management program
- Security incident response procedures
- SOC 2 Type II compliance (or equivalent)

**5.4 Subprocessors.** Provider may use subprocessors to assist in providing the Services. Provider:
- Maintains a list of subprocessors (available upon request)
- Remains responsible for subprocessor performance
- Will notify Customer of material changes to subprocessors with at least thirty (30) days advance written notice

**5.5 Security Incidents.** Provider will:
- Notify Customer without undue delay (and in any event within 24 hours) of a confirmed security incident affecting Customer's Personal Data
- Provide reasonable cooperation in incident investigation
- Implement measures to prevent recurrence
- Maintain incident logs available for audit

**5.6 Data Portability.** Customer may export Customer Data at any time during the Term and for 60 days after termination via provided APIs or export tools. Data exports will be provided in commonly used, machine-readable formats including Markdown (.md), JSON, or CSV as technically feasible based on data type. Provider will provide documentation on export formats and procedures.

**5.7 Data Deletion.** Upon termination, Provider will delete Customer Data from cloud production systems within 30-60 days and from cloud backups within 35 days thereafter, except as required by law. Data stored on Customer's on-device installations is Customer's responsibility to delete.

**5.8 Compliance.** Provider will comply with applicable data protection laws and regulations. Upon Customer's request, Provider and Customer shall execute a Data Processing Agreement (DPA) in accordance with applicable data protection laws prior to processing any personal data. The parties will execute appropriate data transfer agreements as required.

---

## 6. INTELLECTUAL PROPERTY

**6.1 Provider IP.** Provider and its licensors retain all rights in the Services, including all software, documentation, and any derivatives or improvements.

**6.2 Customer IP.** Customer retains all rights in Customer Data and any Customer-provided materials.

**6.3 Feedback.** Customer may provide suggestions, feedback, or recommendations ("**Feedback**"). Provider may use Feedback without restriction and without obligation to Customer.

**6.4 Residual Knowledge.** Provider may use general knowledge, skills, and experience gained in performing Services, provided it does not disclose Customer Confidential Information.

---

## 7. WARRANTIES AND REPRESENTATIONS

**7.1 Mutual Warranties.** Each party warrants that it:
- Has full authority to enter into this Agreement
- Will comply with applicable laws and regulations
- Will perform its obligations in a professional and workmanlike manner

**7.2 Service Warranties.** Provider warrants that:
- The Services will perform materially in accordance with documentation
- The Services will be free from material defects
- It will not introduce malicious code
- It maintains appropriate insurance coverage as detailed in the Insurance Schedule below

**7.2.1 Insurance Schedule.** Provider maintains the following minimum coverage:
- **Technology E&O/Cyber:** $2,000,000 aggregate
- **Commercial General Liability:** $1,000,000 per occurrence  
- **Workers' Compensation/Employer's Liability:** Statutory/$500,000
- **Umbrella/Excess:** $2,000,000 aggregate
- Certificates available upon request

**7.3 Warranty Remedies.** For breach of Service warranties, Provider will use commercially reasonable efforts to correct the non-conformity. If Provider cannot correct it within 30 days, Customer may terminate the affected SOW and receive a pro-rated refund.

**7.4 Disclaimers.** EXCEPT AS EXPRESSLY PROVIDED, PROVIDER DISCLAIMS ALL OTHER WARRANTIES, EXPRESS OR IMPLIED, INCLUDING MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.

---

## 8. INDEMNIFICATION

**8.1 Provider Indemnification.** Provider will defend, indemnify, and hold harmless Customer from third-party claims that the Services infringe intellectual property rights, except to the extent arising from:
- Customer's modifications or misuse
- Combination with non-Provider products/services, unless such combination is required or reasonably anticipated by the Agreement or Documentation
- Use of outdated versions after notice of updates
- Customer Data or Customer-provided materials

**8.2 Customer Indemnification.** Customer will defend, indemnify, and hold harmless Provider from claims arising from:
- Customer Data
- Customer's breach of this Agreement
- Customer's use of the Services in violation of law or the Acceptable Use Policy

**8.3 Indemnification Procedure.** The indemnified party will:
- Promptly notify the indemnifying party
- Provide reasonable cooperation
- Allow the indemnifying party sole control of defense and settlement

---

## 9. LIMITATION OF LIABILITY

**9.1 Liability Cap.** Except for Excluded Claims, each party's total liability will not exceed the total fees paid or payable by Customer under this Agreement and all related SOWs in the 12 months immediately preceding the claim. For purposes of this calculation, "fees" includes all subscription fees, professional services fees, and other amounts paid or owed to Provider, but excludes taxes, third-party costs, and expenses. Notwithstanding the foregoing, Provider's liability for data loss or corruption caused by its gross negligence or willful misconduct shall not exceed three (3) times the amount that would otherwise apply under this Section 9.1.

**9.2 Consequential Damages.** Except for Excluded Claims, neither party will be liable for indirect, incidental, special, consequential, or punitive damages, or lost profits, revenue, or data.

**9.3 Excluded Claims.** The limitations above do not apply to:
- Breach of confidentiality obligations
- Indemnification obligations
- Customer's payment obligations
- Gross negligence or willful misconduct
- Violation of the other party's intellectual property rights

---

## 10. CONFIDENTIALITY

**10.1 Definition.** "**Confidential Information**" means non-public information disclosed by one party to the other that is marked confidential or reasonably should be considered confidential.

**10.2 Obligations.** The receiving party will:
- Use Confidential Information only for Agreement purposes
- Protect it using at least reasonable care
- Limit disclosure to employees/contractors with a need to know
- Not disclose to third parties without written consent

**10.3 Exceptions.** Obligations do not apply to information that:
- Is or becomes publicly available through no breach
- Was rightfully known without confidentiality obligations
- Is independently developed without use of Confidential Information
- Must be disclosed by law (with notice if permitted)

**10.4 Duration.** Confidentiality obligations survive for 5 years after termination (perpetually for trade secrets). For any Customer Data containing personal information subject to data protection laws, confidentiality obligations shall survive as long as required by applicable law.

---

## 11. TERM AND TERMINATION

**11.1 Term.** This MSA begins on the Effective Date and continues until terminated. Each SOW has its own term as specified therein.

**11.2 Termination for Convenience.** Either party may terminate this MSA on 90 days' written notice, provided all SOWs have expired or been terminated.

**11.3 Termination for Cause.** Either party may terminate for material breach if the breach remains uncured 30 days after written notice.

**11.4 Effect of Termination.** Upon termination:
- Customer's access to Services ceases
- Parties return or destroy Confidential Information
- Accrued obligations survive
- Customer may retrieve Customer Data per Section 5.6

**11.5 Survival.** Sections addressing payment, confidentiality, intellectual property, indemnification, limitation of liability, and general provisions survive termination.

---

## 12. GENERAL PROVISIONS

**12.1 Entire Agreement.** This MSA, including all Exhibits and SOWs, constitutes the entire agreement between the parties.

**12.2 Amendment.** Amendments must be in writing and signed by both parties.

**12.3 Assignment.** Neither party may assign without consent, except to an affiliate or acquirer of substantially all assets. In the event of assignment by Provider, Provider will ensure that the assignee is bound by all obligations under this Agreement, including data protection and security standards.

**12.4 Force Majeure.** Neither party is liable for delays due to causes beyond reasonable control.

**12.5 Relationship.** The parties are independent contractors.

**12.6 Notices.** Legal notices must be in writing to:
- **Provider:** legal@pieces.app
- **Customer:** _______________________

**12.7 Severability.** If any provision is unenforceable, the remainder continues in effect.

**12.8 Waiver.** Waiver of any breach is not a waiver of subsequent breaches.

**12.9 Governing Law.** This Agreement is governed by Delaware law.

**12.10 Order of Precedence.** In case of conflict: (1) SOW, (2) MSA body, (3) Exhibits. No SOW may reduce Customer's rights or protections under the MSA or Exhibits unless expressly agreed in writing and signed by both parties.

---

## 13. DEFINITIONS

**"Acceptable Use Policy"** means the usage restrictions in Exhibit D.

**"Customer Data"** means data submitted by Customer to the Services.

**"Documentation"** means Provider's user guides and technical documentation.

**"Services"** means the Pieces for Developers platform and related services.

**"SOW"** means a Statement of Work, Order Form, or Service Order executed under this MSA.

**"Support"** means technical support services per the selected tier.

---

### SIGNATURES

**PROVIDER:**  
Mesh Intelligent Technologies, Inc. (d/b/a pieces.app)

By: _________________________________  
Name: _______________________________  
Title: ______________________________  
Date: _______________________________

**CUSTOMER:**  
__________________________________________

By: _________________________________  
Name: _______________________________  
Title: ______________________________  
Date: _______________________________

---

# EXHIBIT A - SERVICE DESCRIPTION

## Pieces for Developers Platform

**Core Platform Components:**
- **Native Desktop Applications:** High-performance applications for macOS (12+), Windows (10/11), and Linux (Ubuntu 20.04+)
- **Cloud Synchronization:** Secure data sync across devices
- **API Access:** RESTful APIs for integration
- **Browser Extensions:** Chrome, Firefox, Edge, Safari support
- **IDE Integrations:** VS Code, JetBrains, Visual Studio, and more

**Enterprise Features:**
- **Single Sign-On (SSO):** SAML 2.0 and OIDC support
- **SCIM Provisioning:** Automated user lifecycle management
- **Advanced Analytics:** Usage metrics and insights
- **Admin Dashboard:** Centralized management console
- **Custom Integrations:** API access for enterprise systems

**Security Features:**
- End-to-end encryption
- Zero-knowledge architecture options
- Audit logging
- Role-based access control
- Data residency options

**Deployment Options:**
- **Cloud:** Multi-tenant SaaS (standard deployment)
- **Enterprise Cloud Configuration:** SSO-locked models, BYOK integration (requires cloud proxy services)
- **Future Roadmap:** Containerized on-premises deployment (not currently available)

---

# EXHIBIT B - SERVICE LEVEL AGREEMENT

## 1. Service Availability

**1.1 Uptime Commitment:** 
- **Standard Tier:** 99.5% monthly uptime
- **Premium Tier:** 99.7% monthly uptime  
- **Enterprise Tier:** 99.9% monthly uptime

**1.2 Exclusions:** Downtime does not include:
- Scheduled maintenance (with 72-hour notice)
- Customer-caused issues
- Force majeure events
- Third-party service failures

## 2. Support Response Times

**2.1 Priority Levels:**
- **P1 (Critical):** Production system down, no workaround
- **P2 (High):** Major functionality impaired
- **P3 (Medium):** Moderate impact with workaround
- **P4 (Low):** Minor issues or questions

**2.2 Response Time SLAs:**

| Priority | Standard | Premium | Enterprise |
|----------|----------|---------|------------|
| P1 | 4 hours | 1 hour | 30 minutes |
| P2 | 8 hours | 4 hours | 2 hours |
| P3 | 24 hours | 12 hours | 8 hours |
| P4 | 48 hours | 24 hours | 24 hours |

**2.3 Support Hours:**
- **Standard:** Business hours (9 AM - 5 PM ET, Mon-Fri)
- **Premium:** Extended hours (7 AM - 9 PM ET, Mon-Fri)
- **Enterprise:** 24/7/365

## 3. Service Credits

**3.1 Availability Credits:** For each 0.1% below the uptime commitment, Customer receives a 5% service credit for the affected month, up to 50% maximum.

**3.2 Credit Request:** Customer must request credits within 30 days of the incident.

**3.3 Credit Application:** Credits apply to future invoices and do not result in refunds.

---

# EXHIBIT C - DATA PROCESSING TERMS

**Exhibit C reserved.** The Parties agree that the stand-alone **Data Processing Agreement** governs all data protection and privacy obligations and **controls** in the event of conflict with the MSA.

---

# EXHIBIT D - ACCEPTABLE USE POLICY

## Prohibited Uses
Customer will not use the Services to:

**1. Illegal Activities:**
- Violate any applicable laws or regulations
- Facilitate illegal activities
- Violate intellectual property rights

**2. Harmful Content:**
- Distribute malware or malicious code
- Conduct phishing or social engineering
- Store or transmit harmful or offensive content

**3. System Abuse:**
- Attempt unauthorized access
- Interfere with service operation
- Circumvent usage limits or security measures
- Conduct security testing without permission

**4. Regulated Data:**
Unless explicitly authorized in writing, do not process:
- Protected Health Information (PHI)
- Payment Card Industry (PCI) data
- Classified government information
- Data subject to specialized compliance regimes

If Customer requires processing of regulated data, such as PHI or PCI data, this must be explicitly authorized in writing by Provider and may require additional agreements or certifications.

## Fair Use
- Respect rate limits and usage quotas
- Use services for intended purposes
- Follow Documentation and best practices

## Enforcement
Provider may suspend or terminate access for violations after notice and opportunity to cure (except for severe violations requiring immediate action).

---

# EXHIBIT E - STATEMENT OF WORK TEMPLATE

**SOW Number:** _______  
**SOW Date:** _______  
**Project Name:** _______

## 1. Services and Deliverables
[Detailed description of services, deliverables, and acceptance criteria]

## 2. Timeline and Milestones
[Project schedule with key dates and dependencies]

## 3. Fees and Payment
- Service Fees: $_______
- Payment Schedule: _______
- Additional Terms: _______

## 4. Resources and Responsibilities
**Customer Responsibilities:**
- [List specific responsibilities]

**Provider Responsibilities:**
- [List specific responsibilities]

## 5. Project-Specific Terms
[Any SOW-specific terms that supplement or modify the MSA]

## 6. Contacts
**Customer:** _______  
**Provider:** _______

**ACCEPTED AND AGREED:**

Customer: _______________________ Date: _______

Provider: _______________________ Date: _______
