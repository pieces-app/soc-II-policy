---
title: Information Security Roles and Responsibilities Policy
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
stakeholders:
  - Mark Widman (Chief Technology Officer)
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Sam Jones (Chief AI Officer)
  - Katie Storm (AirCFO - HR)
  - Legal Counsel
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2
    - ISO/IEC 27001
    - NIST Cybersecurity Framework
  procedures:
    - Access Control Policy
    - Risk Management Policy
    - Incident Response Plan
  controls:
    - Google Cloud IAM
    - GitHub Enterprise Security
    - Google Workspace Admin
repo: https://github.com/pieces-app/soc-II-policy
---

# **Information Security Roles and Responsibilities Policy** 

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))

**Effective Date:** August 19, 2025

# **Statement of Policy**

Mesh Intelligent Technologies, Inc. is committed to conducting business in compliance with all applicable laws, regulations, and company policies. Mesh Intelligent Technologies, Inc. has adopted this policy to outline the security measures required to protect electronic information systems and related equipment from unauthorized use.

# **Objective** 

This policy and associated guidance establish the roles and responsibilities within Mesh Intelligent Technologies, Inc., which is critical for effective communication of information security policies and standards. Roles are required within the organization to provide clearly defined responsibilities and an understanding of how the protection of information is to be accomplished. Their purpose is to clarify, coordinate activity, and actions necessary to disseminate security policy, standards, and implementation.

# **Applicability** 

This policy is applicable to all Mesh Intelligent Technologies, Inc. infrastructure, network segments, systems, and employees and contractors who provide security and IT functions.

# **Audience** 

The audience for this policy includes all Mesh Intelligent Technologies, Inc. employees and contractors who are involved with the Information Security Program. Awareness of this policy applies for all other agents of Mesh Intelligent Technologies, Inc. with access to Mesh Intelligent Technologies, Inc. information and infrastructure. This includes, but is not limited to partners, affiliates, contractors, temporary employees, trainees, guests, and volunteers. The titles will be referred collectively hereafter as "Mesh Intelligent Technologies, Inc. community".

# **Roles and Responsibilities**

| Roles | Responsibilities |
| :---- | :---- |
| CEO (Tsavo Knott) | • Ultimate accountability for security program effectiveness<br>• Approves security policies and major risk acceptances<br>• Serves as executive sponsor for security initiatives<br>• Communicates security priorities to the organization<br>• Handles customer security concerns (with CPO)<br>• Reports security posture to Board of Directors |
| Board of Directors | • Oversight of Cyber-Risk and internal control for information security, privacy and compliance<br>• Consults with Executive Leadership to understand Mesh Intelligent Technologies, Inc. IT mission and risks and provides guidance to align business, IT, and security objectives<br>• Reviews quarterly security reports and annual risk assessments<br>• Approves strategic security initiatives and risk appetite<br>• Ensures appropriate resources are allocated to security programs<br>• Reviews material security incidents and breach notifications |
| Executive Leadership (CEO, CTO, CPO) | • Approves Capital Expenditures for Information Security and Privacy programs and initiatives<br>• Oversight over the execution of the information security and Privacy risk management program and risk treatments<br>• Communication Path to Mesh Intelligent Technologies, Inc. Board of Directors<br>• Aligns Information Security and Privacy Policy and Posture based on Mesh Intelligent Technologies, Inc.'s mission, strategic objectives and risk appetite<br>• Champions security culture throughout the organization |
| Head of Cloud Infrastructure & Security (Hiro Tamada) | • Oversight over the implementation of information security controls for infrastructure and IT processes<br>• Responsible for the design, development, implementation, operation, maintenance and monitoring of IT security controls<br>• Ensures IT puts into practice the Information Security Framework<br>• Responsible for conducting IT risk assessments, documenting identified threats and maintaining risk register<br>• Communicates information security risks to executive leadership<br>• Reports information security risks quarterly to Mesh Intelligent Technologies, Inc.'s leadership and gains approvals to bring risks to acceptable levels<br>• Coordinates the development and maintenance of information security policies and standards<br>• Works with applicable executive leadership to establish an information security framework and awareness program<br>• Serve as liaison to the Board of Directors, Law Enforcement, Internal Audit and General Counsel<br>• Oversight over Identity Management and Access Control processes<br>• Manages GCP security configurations and monitoring (including Cloud Security Command Center)<br>• Oversees vulnerability management with defined SLAs (Critical: 72 hours, High: 7 days, Medium: 30 days)<br>• Ensures patch management per criticality (Critical: immediate, High: 30 days, Medium: 60 days)<br>• Manages incident response with RTO of 4 hours and RPO of 24 hours<br>• Oversees quarterly penetration testing and annual third-party assessments<br>• Maintains security log retention (minimum 90 days, 365 days for audit logs)<br>• Ensures 99.9% uptime target for production services |
| Chief Technology Officer (Mark Widman) | • Oversight over information security in the software development process<br>• Responsible for the design, development, implementation, operation, maintenance and monitoring of development and commercial cloud hosting security controls<br>• Responsible for oversight over policy development related to systems and software under their control<br>• Responsible for implementing risk management in the development process aligned with company goals<br>• Ensures secure architecture and design principles are followed<br>• Oversees Secure Software Development Lifecycle (SSDLC) including:<br>  - Threat modeling for new features (STRIDE methodology)<br>  - Security requirements tracking throughout development<br>  - SAST/DAST/SCA integration in CI/CD pipelines<br>  - Code review with security checklists (OWASP guidelines)<br>  - Security test cases in QA processes<br>• Oversees technology stack security and AI/ML security controls<br>• Ensures API security architecture (OAuth 2.0, rate limiting, input validation)<br>• Manages Software Bill of Materials (SBOM) transparency |
| Head of CI/CD & DevOps (Nathan Courtney) | • Implements and maintains secure CI/CD pipelines<br>• Manages GitHub Enterprise Security configurations<br>• Oversees code signing and artifact attestation processes<br>• Ensures secure software supply chain practices<br>• Manages secrets and credentials in CI/CD workflows<br>• Implements infrastructure as code security controls<br>• Coordinates deployment security and change management |
| Chief AI Officer (Sam Jones) | • Oversees AI/ML model security and governance<br>• Ensures responsible AI practices and bias mitigation<br>• Manages model versioning and rollback capabilities<br>• Implements adversarial protection for AI systems<br>• Oversees training data governance and privacy<br>• Ensures synthetic data methodology for model training (no customer PII in training)<br>• Maintains comprehensive data lineage tracking for abuse detection<br>• Manages model performance monitoring with drift detection<br>• Coordinates AI risk assessments and compliance<br>• Manages Hugging Face repository security<br>• Leads model validation and testing through AI/ML team<br>• Ensures ethical AI practices without formal committee<br>• Oversees opt-in telemetry controls for performance monitoring |
| VP of Global Customer Support | • Oversight and implementation, operation and monitoring of information security tools and processes in customer production environments<br>• Execution of customer data retention and deletion processes in accordance with company policy and customer requirements<br>• Coordinates with customers on security incidents and notifications<br>• Manages customer-specific security configurations<br>• Ensures compliance with customer security requirements<br>• Maintains support SLAs (P1: 4hr, P2: 8hr, P3: 12hr, P4: 24hr initial response)<br>• Manages data export requests (30-day bulk export for enterprise)<br>• Coordinates quarterly business reviews for enterprise accounts<br>• Ensures root cause analysis for all P1/P2 incidents |
| Corporate Secretary & CPO (Mack Myers) | • Responsible for compliance with the company's contractual commitments<br>• Responsible for maintaining compliance with relevant data privacy and information security laws and regulations (e.g. GDPR, CCPA/CPRA, NIS2)<br>• Responsible for adherence to company adopted information security and data privacy standards and frameworks including SOC 2 Type II, ISO 27001<br>• Manages Vanta platform for compliance automation and evidence collection<br>• Manages customer security questionnaires and assessments<br>• Serves as primary customer success contact for security matters (with CEO)<br>• Coordinates external audits and certifications (annual SOC 2 Type II renewal)<br>• Oversees privacy program and data subject requests (30-45 day response timeline)<br>• Manages vendor security assessments and maintains vendor inventory<br>• Acts as Data Protection focal point in absence of dedicated DPO<br>• Ensures GDPR breach notifications within 72 hours when required<br>• Maintains Data Processing Addenda (DPAs) with subprocessors<br>• Oversees data retention and deletion procedures (30-day standard processing)<br>• Manages customer notification for security incidents (24-hour target) |
| Chief Financial Officer (Katie Storm - AirCFO) | • Oversight of financial controls and budget for security programs<br>• Review and approval of security-related expenditures<br>• Ensures appropriate cyber insurance coverage through At-Bay Specialty Insurance Company<br>• Manages cyber insurance relationship and annual renewals<br>• Partners with CPO on vendor contract reviews<br>• **HR Responsibilities:**<br>  • Ensuring employees and contractors are qualified and competent for their roles<br>  • Ensuring appropriate testing and background checks are completed (where legally permissible)<br>  • Ensuring that employees and relevant contractors are presented with company policies and the Code of Conduct (CoC)<br>  • Ensuring that employee performance and adherence to the CoC is periodically evaluated<br>  • Ensuring that employees receive appropriate security awareness training (onboarding and annually)<br>  • Managing employee onboarding and offboarding processes<br>  • Ensuring immediate access revocation upon separation (≤24 hours for employees, immediate for third-parties)<br>  • Conducting security-focused exit procedures including asset return<br>  • Coordinating 90-day post-departure monitoring for anomalous activities<br>  • Coordinating insider threat awareness programs |
| Legal Counsel | • Reviews and approves security-related contracts and agreements<br>• Advises on regulatory compliance requirements<br>• Manages breach notification requirements<br>• Oversees incident response legal considerations<br>• Reviews and approves security policies from legal perspective<br>• Manages intellectual property protection<br>• Coordinates with law enforcement when necessary |
| Security/GRC Function (distributed) | • Security operations distributed across engineering teams<br>• Head of Cloud Infrastructure leads infrastructure security<br>• CPO maintains GRC platform (Vanta) and evidence collection<br>• HR (AirCFO) coordinates security awareness training programs<br>• Engineering teams perform security assessments and code reviews<br>• CPO manages security metrics and reporting<br>• CEO and CPO respond to customer security questionnaires<br>• Engineering teams maintain security documentation and runbooks |
| Systems/Data Owners | • Maintain the confidentiality, integrity and availability of the information systems for which they are responsible in compliance with Mesh Intelligent Technologies, Inc. policies on information security and privacy<br>• Approval of technical access and change requests for non-standard access to systems under their control<br>• Define data classification and handling requirements<br>• Participate in risk assessments for their systems<br>• Ensure appropriate controls are implemented |
| Engineering Team | • Implements secure coding practices<br>• Participates in security design reviews<br>• Remediates identified vulnerabilities<br>• Follows secure development lifecycle<br>• Reports security issues through appropriate channels<br>• Maintains security of development environments<br>• Implements security requirements in features<br>• **Security Champions (Hiro Tamada, Mark Widman):**<br>  • Lead security initiatives within engineering<br>  • Promote security best practices<br>  • Coordinate security training for developers<br>  • Act as security focal points for their teams |
| All Employees, Contractors, and Third Parties | • Acting at all times in a manner which does not place at risk the health and safety of themselves, other persons in the workplace, and the information and resources they have use of<br>• Helping to identify areas where risk management practices should be adopted<br>• Taking all practical steps to minimize Mesh Intelligent Technologies, Inc.'s exposure to contractual and regulatory liability<br>• Adhering to company policies and standards of conduct<br>• Reporting incidents and observed anomalies or weaknesses<br>• Completing required security awareness training<br>• Protecting credentials and authentication methods<br>• Following data handling and classification requirements |
| External Auditors & Pen Testers | • Conduct annual penetration tests and security assessments<br>• Provide independent validation of security controls<br>• Issue findings and recommendations for improvement<br>• Validate remediation of identified vulnerabilities<br>• Support compliance certification efforts |
| Key Technology Vendors (Google, GitHub) | • Provide security guidance and best practices for their platforms<br>• Direct communication channels for security issues<br>• Platform security updates and threat intelligence<br>• Support for security configurations and hardening<br>• Incident response coordination when platform-related |

# **Security Governance Structure**

## **Security Steering Committee**
- Meets quarterly to review security posture and initiatives
- Members: CEO, CTO, CPO, Head of Cloud Infrastructure, Chief AI Officer
- Reviews risk register, incident trends, and compliance status
- Approves security budget and strategic initiatives

## **Operational Security Team**
- Meets weekly to review operational security matters
- Members: Head of Cloud Infrastructure, Head of CI/CD & DevOps, Engineering Security Champions
- Reviews vulnerabilities, patches, and ongoing incidents
- Coordinates security operations and improvements
- Engineering teams handle day-to-day security operations

## **Incident Response Team**
- Activated as needed per Incident Response Plan
- Core team: Head of Cloud Infrastructure (Lead), CTO, CPO, Legal Counsel
- Extended team engaged based on incident type
- Maintains 24/7 on-call rotation

# **Accountability and Escalation**

## **RACI Matrix for Key Security Activities**

| Activity | Responsible | Accountable | Consulted | Informed |
| :------- | :---------- | :---------- | :-------- | :------- |
| Policy Development | CPO | CEO | Legal, CTO | All Staff |
| Risk Management | Head of Cloud Infra | CEO | CTO, CPO | Board |
| Incident Response | Head of Cloud Infra | CTO | Legal, CPO | CEO, Board |
| Access Management | System Owners | Head of Cloud Infra | HR (AirCFO) | CPO |
| Vulnerability Management | Head of Cloud Infra | CTO | DevOps | CPO |
| Compliance (Vanta) | CPO | CEO | Legal | Board |
| Security Training | HR (AirCFO) | CPO | All Managers | All Staff |
| Vendor Security | CPO | CFO (AirCFO) | Legal, CTO | Engineering |
| Pen Testing | Head of Cloud Infra | CTO | CPO | CEO, Board |
| Customer Security | CEO/CPO | CEO | CTO | Sales/Success |
| AI/ML Security | Chief AI Officer | CTO | Head of Cloud | CPO |

## **Escalation Path**
1. Operational Issues → Head of Cloud Infrastructure
2. Policy Exceptions → CPO → CEO
3. Major Incidents → CTO → CEO → Board (if material)
4. Compliance Issues → CPO → CEO → Board (if material)
5. Legal/Regulatory → Legal Counsel → CEO → Board

# **Performance Metrics**

Security role effectiveness is measured through:
- Quarterly access reviews completion rate (target: 100%)
- Security training completion rate (target: 100% within 30 days)
- Time to provision/deprovision access (target: <24 hours)
- Incident response time (per severity SLAs in IRP)
- Policy review and update cycle adherence (annual)
- Vulnerability remediation within SLAs (per Operations Security Policy)
- Audit finding closure rate (target: 100% within agreed timeframes)
- Support response times (P1: 4hr, P2: 8hr, P3: 12hr, P4: 24hr)
- Customer incident notification time (target: 24 hours)
- GDPR breach notification (within 72 hours when required)
- Data deletion request processing (30 days standard, 60 days complex)

# **Training and Awareness**

- All role holders receive role-specific security training upon appointment
- Annual refresher training required for all security roles
- Quarterly tabletop exercises for incident response team
- Monthly security awareness topics for all staff
- Specialized training for high-risk roles (admins, developers, data handlers)

# **Policy Compliance** 

The Corporate Secretary & CPO (Mack Myers) will measure compliance to this policy through various methods, including but not limited to:
- Internal and external audits (including annual penetration tests)
- Vanta compliance automation platform monitoring
- Review of role assignments and access rights
- Training completion reports from HR (AirCFO)
- Incident post-mortems and lessons learned
- Security metrics dashboards and KPIs
- Direct feedback from Google and GitHub vendor relationships
- Customer security questionnaire responses and feedback

Exceptions to the policy must be approved by the CEO (Tsavo Knott) in advance and documented with business justification, compensating controls, owner, and expiration date.

Non-compliance will be addressed with management and Human Resources (AirCFO) and can result in disciplinary action in accordance with company procedures up to and including termination of employment.

# **Compliance Roadmap Responsibilities**

## **Current Certifications**
- SOC 2 Type II: Annual renewal (CPO responsible, target: September 2025)
- GDPR Compliance: Maintained with documented procedures (CPO/Legal)
- CCPA/CPRA: Compliant with data subject request procedures (CPO)

## **12-Month Targets**
- ISO 27001 Certification: Target December 2025 + 6 months (CPO/Head of Cloud Infrastructure)
- Annual third-party penetration testing (Head of Cloud Infrastructure)
- Zero Trust Architecture implementation (Head of Cloud Infrastructure/CTO)

## **24-Month Targets**
- HIPAA Compliance: BAA capability on customer demand (CPO/Legal)
- ISO 27017 (Cloud Security): Extension for cloud controls (Head of Cloud Infrastructure)

## **On-Demand**
- Custom compliance support for customer requirements (CPO)
- Industry framework alignment (NIST, CIS Controls) as needed (Security/GRC)
- Attestation letters for specific controls (CPO/Legal)

# **Key Vendor Relationships**

Critical vendors requiring security oversight:
- **Infrastructure**: Google Cloud Platform, GitHub Enterprise (Head of Cloud Infrastructure)
- **Monitoring**: Sentry (crashlytics), Google Cloud Security Command Center (Engineering)
- **Authentication**: Descope (Head of Cloud Infrastructure)
- **Payments**: Paddle (CFO/CPO)
- **Analytics**: Mixpanel, Segment, Satismeter (Engineering/Product)
- **Customer Support**: HubSpot, Customer.io (VP of Global Customer Support)
- **Compliance**: Vanta (CPO)
- **Cyber Insurance**: At-Bay Specialty Insurance Company (CFO/CPO)
  - Address: 3500 Lenox Road, Suite 1425, Atlanta, GA 30326
  - Annual policy review and renewal coordination
  - Incident notification within 24 hours for potential claims
  - Risk assessment collaboration and recommendations

Each vendor relationship includes:
- Security assessment and ongoing monitoring (CPO)
- Data Processing Addenda maintenance (Legal/CPO)
- Incident notification procedures (Head of Cloud Infrastructure)
- Annual security posture review (CPO)

# **Related Documents**

- Access Control Policy
- Risk Management Policy
- Incident Response Plan
- Operations Security Policy
- Business Continuity and Disaster Recovery Plan
- Third-Party Management Policy
- Data Management Policy
- Code of Conduct
- Legal & Security Policies (Customer-Facing) - LEGAL_POLICY_2025_COUNSEL_VERIFIED.md

# **Emergency Contacts**

- **Security Hotline**: (513) 572-3339 (Critical security incidents only)
- **Executive Escalation**: tsavo@pieces.app (CEO)
- **Security Reports**: security@pieces.app
- **Privacy/Data Requests**: privacy@pieces.app
- **General Support**: support@pieces.app
- **Cyber Insurance Claims**: At-Bay Specialty Insurance Company (contact CFO for policy details)

# **Data Residency & Architecture Responsibilities**

- **Primary Data Location**: Google Cloud Ohio region (us-east5) - Head of Cloud Infrastructure
- **Multi-Tenant Isolation**: Row-level security and tenant validation - Engineering Team
- **Data Export Capabilities**: Self-service and bulk export support - VP of Global Customer Support
- **Self-Hosting Support**: Container deployment options for enterprise - Head of CI/CD & DevOps
- **Regional Compliance**: Data residency requirements per customer - CPO/Legal

# **Definitions**

- **Information Security**: Protection of information and information systems from unauthorized access, use, disclosure, disruption, modification, or destruction
- **GRC**: Governance, Risk, and Compliance
- **RACI**: Responsible, Accountable, Consulted, Informed
- **System Owner**: Individual responsible for the operation and security of a specific system or application
- **Data Owner**: Individual responsible for the classification and protection requirements of specific data
- **RTO**: Recovery Time Objective - maximum tolerable downtime (4 hours target)
- **RPO**: Recovery Point Objective - maximum tolerable data loss (24 hours target)
- **DPA**: Data Processing Addendum - contract governing personal data handling
- **BAA**: Business Associate Agreement - HIPAA-required contract for health information
- **SSDLC**: Secure Software Development Lifecycle
- **SLA**: Service Level Agreement
- **P1-P4**: Priority levels for support tickets (P1 most critical)

# **Revision History**

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0 | 01-Jan-2023 | Initial Version | Georgia Donmoyer | Tsavo Knott |
| 1.1 | 19-Aug-2025 | 2025 Refresh | Mack Myers | Tsavo Knott (CEO) |
