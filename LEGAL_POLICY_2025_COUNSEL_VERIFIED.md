# **Pieces Legal & Security Policies (Customer-Facing)**

Version: 1.2  
Effective Date: August 1, 2025  
Contacts: support@pieces.app

---

## **Document Control**

Owner: Information Security  
Approved By: Legal Counsel  
Next Review Date: Sep 1, 2025 + 12 months  
Classification: External / Public

---

## **Table of Contents**

1. Data Retention Policy  
   1.1 Scope  
   1.2 Guiding Principles  
   1.3 Default Retention Schedule  
   1.4 Model Training & Improvement Data  
   1.5 Backups & Snapshots  
   1.6 Review & Audit  
2. Data Deletion Policy  
   2.1 Self-Service Deletion  
   2.2 Enterprise & Bulk Requests  
   2.3 Timelines  
   2.4 Exceptions & Legal Holds  
   2.5 Verification & Proof  
3. Privacy Policy  
   3.1 Overview  
   3.2 Data We Collect  
   3.3 How We Use Data  
   3.4 Legal Bases (GDPR)  
   3.5 Sharing & Disclosure  
   3.6 International Transfers  
   3.7 Your Rights  
   3.8 Cookies & Local Storage  
   3.9 Children's Data  
   3.10 Changes to This Policy  
   3.11 Data Portability & Export Rights  
4. Business Continuity & Disaster Recovery (BCP/DRP)  
   4.1 Objectives (RTO/RPO)  
   4.2 Scope & Risks  
   4.3 Redundancy & Backups  
   4.4 Incident Response Alignment  
   4.5 Communication & Transparency  
   4.6 Testing & Maintenance  
   4.7 Vendor & Subprocessor Resilience  
   4.8 Roles & Responsibilities  
5. Information Security Policy  
   5.1 Security Framework & Certifications  
   5.2 Encryption Standards & Data Protection  
   5.3 Access Controls & Identity Management  
   5.4 Security Monitoring & Logging  
   5.5 Incident Response & Forensic Capabilities  
   5.6 Availability & Uptime Commitments  
   5.7 Penetration Testing & Vulnerability Management  
   5.8 Personnel Security & Insider Threat Management  
   5.9 Secure Software Development Lifecycle  
   5.10 API Security Architecture  
6. AI Governance & Data Policy  
   6.1 AI Training Data Practices  
   6.2 Model Transparency & Bias Prevention  
7. Data Residency & Infrastructure  
   7.1 Data Location & Sovereignty  
   7.2 Cloud Infrastructure & Self-Hosting Options  
   7.3 Multi-Tenant Architecture & Isolation  
8. Vendor & Supply Chain Security  
   8.1 Third-Party Dependencies  
   8.2 Software Bill of Materials (SBOM)  
9. Compliance & Audit Support  
   9.1 Audit Capabilities  
   9.2 Regulatory Compliance  
   9.3 Compliance Roadmap  
10. Financial Assurance & Risk Transfer  
    10.1 Cyber Insurance Coverage  
    10.2 Financial Health  
    10.3 Support Response Commitments  
11. Appendices  
    A. Definitions  
    B. Request Channels  
    C. Change Log

---

## **1. Data Retention Policy**

### **1.1 Scope**

This policy applies to all data collected, generated, or processed by Pieces in the ordinary course of business operations, subject to applicable laws and contractual obligations. The scope encompasses:

* Account and billing information maintained for legitimate business purposes  
* User-generated content (including but not limited to snippets, notes, screenshots, and files) as voluntarily provided by users  
* Telemetry and diagnostic data collected in accordance with user consent preferences  
* Security and system logs generated during normal system operations  
* Support communications and related documentation

### **1.2 Guiding Principles**

Our data retention practices are guided by the following principles, applied in accordance with applicable legal requirements and industry best practices:

* Data Minimization & Purpose Limitation: We endeavor to retain only such data as is reasonably necessary to deliver, secure, and improve our services, subject to legitimate business requirements and applicable legal obligations.  
* User Autonomy: Users may delete content through available self-service mechanisms; enterprise administrators may request bulk deletions where technically feasible and commercially reasonable.  
* Legal Compliance: Data may be retained for such additional periods as may be required by applicable laws, regulations, legal process, or contractual obligations.  
* Industry Alignment: Our retention practices are designed to align with those commonly employed by similar AI productivity tools, while maintaining appropriate safeguards for user privacy and data protection.

### **1.3 Default Retention Schedule**

The following schedule represents our standard data retention practices, subject to modification as required by applicable law, contractual obligations, or legitimate business requirements:

| Data Category | Examples | Standard Retention Period | Notes |
| :---- | :---- | :---- | :---- |
| Account & Billing Data | Registration details, invoices, tax identifiers | Account duration + 7 years post-termination | Required for tax, audit, and regulatory compliance purposes. |
| User-Generated Content | Snippets, Copilot Chats, notes, screenshots, files that are *Explicitly backed up by the user to Cloud | Until user deletion or account termination; backup retention up to 35 days | Reflects industry norms for user data control. |
| Telemetry & Diagnostics | System logs, performance metrics | 180 days (rolling basis) | Adequate for performance analysis and abuse detection. |
| Security & Access Logs | Authentication records, API access logs | 90 days (rolling basis) | Consistent with SOC 2 and ISO 27001 practices. |
| De-identified/Aggregated Data | Usage statistics, model evaluation datasets | Until no longer required for legitimate business purposes | Opt-out controls available. |
| Support & Communications | Service requests, correspondence | 2 years following case closure | Standard customer service defensibility period. |

Enterprise Customization: Alternative retention schedules, including zero-retention policies and bespoke arrangements, may be available through separate Data Processing Addenda (DPA) or Enterprise Service Agreements, subject to technical feasibility and commercial terms.

### **1.4 Model Training & Improvement Data**

* We may utilize de-identified or aggregated data for the purpose of improving features and models, subject to applicable privacy laws and contractual obligations.  
* Opt-Out Controls: Individual users may disable this data usage through in-application settings, and enterprise customers may exclude their content via contractual arrangements where technically feasible.  
* Training pipelines are designed with appropriate segregation and access controls in accordance with industry best practices.

### **1.5 Backups & Snapshots**

* We maintain encrypted daily backups with a standard 35-day rolling retention period, unless otherwise specified in applicable service agreements.  
* Quarterly restore testing is performed to validate data recoverability in accordance with our business continuity procedures.

### **1.6 Review & Audit**

* This policy is subject to annual review, and additionally following any significant regulatory or architectural changes that may impact data retention practices.  
* Internal audits are conducted at least annually to verify adherence to policy requirements and applicable regulatory standards.

---

## **2. Data Deletion Policy**

### **2.1 Self-Service Deletion**

* Item-Level Deletion: Users may delete individual content items directly within the product interface, subject to system capabilities and any applicable restrictions.  
* Account-Level Deletion: Users may request comprehensive account deletion through available settings interfaces or by contacting support@pieces.app, subject to verification procedures and applicable legal requirements.

### **2.2 Enterprise & Bulk Requests**

* Enterprise administrators may request project-wide or workspace-level deletions through designated support channels or available Enterprise API functionality, where technically feasible.  
* Written confirmation of deletion completion will be provided following successful processing, subject to any applicable legal restrictions.

### **2.3 Processing Timelines**

* Standard Requests: Deletion requests are typically processed within 30 calendar days of receipt and verification, subject to system capabilities and legal requirements.  
* Complex or Large-Scale Requests: Processing may extend to 60 calendar days for technically complex requests, unless alternative timelines are mutually agreed.  
* Backup Systems: Corresponding data in backup systems is deleted or cryptographically rendered inaccessible within 35 days following primary system deletion, subject to technical limitations.

### **2.4 Legal Exceptions & Holds**

Data subject to legal, regulatory, or contractual retention requirements will be isolated from operational processing systems while remaining accessible solely for compliance purposes, in accordance with applicable legal obligations.

### **2.5 Verification & Documentation**

Upon reasonable request, we will provide written confirmation of deletion or anonymization completion, noting any applicable legal exceptions or technical limitations that may preclude complete removal.

---

## **3. Privacy Policy**

### **3.1 Overview**

Pieces processes personal data in accordance with applicable privacy laws and regulations, including but not limited to the General Data Protection Regulation (GDPR) and California Consumer Privacy Act (CCPA/CPRA). This section outlines our data collection, processing, and protection practices, as well as individual rights regarding personal data.

### **3.2 Data We Collect**

We collect and process the following categories of data in connection with our services:

* Information Provided by Users:  
  * Registration and billing information provided during account creation and maintenance  
  * User-generated content (including snippets, notes, and files) voluntarily stored within our platform  
* Automatically Collected Information:  
  * Device and operating system information, crash reports, and feature usage metrics collected through technical means  
  * Authentication and security event data generated during normal system operations  
* Third-Party Integrations & Desktop Applications:  
  * Data transmitted by IDE plugins, browser extensions, and desktop applications in accordance with this policy and applicable consent mechanisms  
  * Local caching data stored on user devices (including encrypted local storage), which may be managed through application settings

### **3.3 Data Processing Purposes**

We process personal data for the following purposes, subject to applicable legal bases and contractual obligations:

* Provision, maintenance, and improvement of our services in accordance with our terms of service  
* Personalization of user experience, troubleshooting technical issues, and platform security maintenance  
* Training or evaluation of models using exclusively de-identified data, or pursuant to explicit user consent or contractual agreements with appropriate safeguards  
* Communication of product updates, billing notices, and security alerts to authorized users  
* Compliance with applicable legal obligations and enforcement of our contractual agreements

### **3.4 Legal Bases for Processing (GDPR)**

Where applicable, our processing activities rely upon the following legal bases:

* Performance of contractual obligations with users  
* Pursuit of legitimate business interests, balanced against individual privacy rights  
* User consent, where specifically obtained for optional processing activities  
* Compliance with applicable legal and regulatory obligations

### **3.5 Data Sharing & Disclosure**

* We do not engage in the sale of personal data for commercial purposes.  
* Authorized subprocessors (including cloud hosting, analytics, and payment providers) are subject to rigorous vetting procedures and bound by comprehensive Data Processing Addenda (DPAs) with appropriate safeguards.  
* Data disclosure in response to legal process is subject to careful review for scope and legitimacy, with customer notification provided whenever legally permissible.

### **3.6 International Data Transfers**

Cross-border personal data transfers are conducted utilizing Standard Contractual Clauses (SCCs) or equivalent legal safeguards as approved by relevant supervisory authorities, ensuring adequate protection for personal data.

### **3.7 Individual Rights**

* Individuals may possess rights to access, correct, delete, or restrict processing of their personal data, as well as rights to object to processing and request data portability, as provided under applicable privacy laws.  
* To exercise these rights, individuals may contact us at support@pieces.app. We endeavor to respond within applicable statutory timeframes (typically 30–45 days, subject to legal requirements).

### **3.8 Cookies & Local Storage Technologies**

* We utilize cookies and local storage technologies for authentication, user preference management, and analytics purposes, subject to applicable consent requirements.  
* These technologies may be managed through browser or application settings. We honor "Do Not Track" signals where technically feasible and legally required.

### **3.9 Children's Privacy**

Our services are not intended for individuals under 13 years of age (or equivalent minimum age in applicable jurisdictions). In the event personal data from a child is inadvertently collected, please contact us promptly to request its removal.

### **3.10 Policy Modifications**

We may update this policy periodically to reflect legal, technical, or business developments. Material changes will be communicated with appropriate advance notice as required by applicable law (for example, via email or in-application notification).

### **3.11 Data Portability & Export Rights**

Self-Service Data Export:

* Users may export their data at any time through our cloud or local APIs, or via the UI in industry-standard formats (JSON, CSV).  
* Comprehensive Export: All user-generated content, metadata, and configuration settings are included in exports.  
* No Vendor Lock-in: We do not use proprietary formats; all exports utilize open standards for maximum compatibility.

Enterprise Export Capabilities:

* Bulk Export: Full organizational data export available within 30 days of verified request.  
* Format Options: JSON, CSV, SQL dump, or other industry-standard formats as technically feasible.  
* Data Dictionary: Comprehensive documentation of data schemas, field definitions, and relationships provided with exports.  
* API Access: RESTful APIs available for programmatic data retrieval and migration.

Export Support & Assistance:

* Documentation: Detailed export guides and data migration documentation available in our knowledge base.  
* Technical Support: Assistance available for enterprise customers during data export and migration processes.  
* Retention Post-Export: Exported data remains available for re-download for 30 days after initial export completion.

---

## **4. Business Continuity & Disaster Recovery (BCP/DRP)**

### **4.1 Recovery Objectives (RTO/RPO)**

Our business continuity planning is designed to meet the following objectives, subject to the nature and scope of any disruption:

* Recovery Time Objective (RTO): Restoration of core services within 4 hours of a qualifying incident, where technically feasible.  
* Recovery Point Objective (RPO): Limitation of data loss to no more than 24 hours in catastrophic events, subject to the nature of the disruption and available recovery mechanisms.

### **4.2 Scope & Risk Assessment**

* This policy applies to production systems, cloud infrastructure, and critical third-party services that support our platform operations.  
* Identified Risk Categories: These include but are not limited to cloud or network outages, distributed denial-of-service attacks, credential compromise incidents, vendor service failures, and natural disasters.

### **4.3 Redundancy & Backup Infrastructure**

* We utilize multi-Availability Zone architecture with automatic failover capabilities where technically and commercially feasible.  
* Encrypted daily backups are maintained in geographically separate locations, with quarterly restore testing conducted to verify recoverability and system integrity.

### **4.4 Incident Response Procedures**

Our incident response follows a structured approach designed to minimize service disruption:

1. Detection and Classification of incident severity based on established criteria.  
2. Containment and Threat Elimination using automated and manual procedures as appropriate.  
3. System Recovery from verified clean backups with comprehensive data integrity validation.  
4. Post-Incident Analysis including root cause determination and preventive measure implementation.

### **4.5 Communication & Stakeholder Coordination**

* Internal Coordination: We maintain dedicated incident communication channels, on-call rotations, and escalation procedures for internal team coordination.  
* Customer Communication: Status page updates and direct customer notifications are provided in accordance with Service Level Agreement requirements, with regulatory notifications issued if personal data is potentially impacted.  
* External Relations: Media communications and legal inquiries are managed by executive leadership and legal counsel as appropriate.

### **4.6 Testing & Maintenance Procedures**

* Tabletop disaster simulation exercises are conducted bi-annually to validate response procedures and team readiness.  
* Comprehensive failover testing is performed annually in staging or production-equivalent environments to verify system recovery capabilities.  
* This BCP/DR policy undergoes review and updates following any major incident or at minimum annually, whichever occurs first.

### **4.7 Vendor & Subprocessor Resilience Assessment**

* We conduct periodic assessments of critical vendors' and subprocessors' business continuity and disaster recovery capabilities as part of our risk management framework.  
* Contingency plans for migration or replacement of critical vendor services are maintained where commercially reasonable and technically feasible.

### **4.8 Organizational Roles & Responsibilities**

* Policy Owner: Head of Legal & Information Security (or designated delegate) maintains responsibility for policy oversight and approval authority.  
* Incident Commander: Designated senior engineering or security personnel assume leadership of incident response activities during service disruptions.  
* Communications Coordinator: Product or Support team leadership manages customer communications during incident response activities.  
* Compliance & Audit: Legal and Compliance team personnel document exercise activities and maintain evidence for regulatory and audit purposes.

---

## **5. Information Security Policy**

### **5.1 Security Framework & Certifications**

* We maintain SOC 2 Type II certification and are committed to, at minimum annual, renewal cycles to ensure continuous compliance with applicable standards, subject to certification body requirements.  
* Our security practices are designed to align with ISO 27001 standards and NIST Cybersecurity Framework principles, adapted to our specific operational environment.  
* We utilize Google Cloud Platform's and GitHub’s enterprise-grade security infrastructure, thereby inheriting the benefit of their SOC 2, ISO 27001, and FedRAMP certifications, subject to their respective terms and limitations.

### **5.2 Encryption Standards & Data Protection**

* Data in Transit: All data transmissions utilize TLS 1.3 encryption with forward secrecy, implemented in accordance with current industry standards.  
* Data at Rest: We employ AES-256 encryption for stored data, utilizing Google Cloud's default encryption mechanisms and key management services.  
* Enhanced Security Architecture: For qualifying enterprise deployments, we implement enhanced encryption protocols designed to prevent unauthorized access, subject to technical feasibility and contractual arrangements.  
* Device-Level Security: On-device data storage leverages and extends end-user device security protocols, including hardware security modules where available and supported.

### **5.3 Access Controls & Identity Management**

We implement access controls through enterprise-grade systems and procedures:

* Identity Management: Google Workspace, GitHub, Hugging Face, all internal SaaS toolings, with mandatory multi-factor authentication (MFA) for all personnel accessing company systems.  
* Code Repository Security: GitHub Enterprise with branch protection, mandatory code review requirements, and comprehensive access logging.  
* Compliance Monitoring: Vanta platform deployment for continuous security posture monitoring and access governance activities.  
* Network Security: Dedicated employee devices with VPN requirements for secure remote access to company resources.  
* Principle of Least Privilege: Role-based access controls designed to ensure personnel access only those systems necessary for their designated job functions.

### **5.4 Security Monitoring & Logging**

We maintain security monitoring capabilities across our operational systems:

* Cloud Infrastructure: Google Cloud Security Command Center and GitHub Enterprise Security Systems, with real-time threat detection and automated incident response capabilities.  
* Application Monitoring: Sentry deployment for application performance monitoring and error tracking with security event correlation.  
* Code Security: GitHub Advanced Security for vulnerability scanning, secret detection, and dependency analysis activities.  
* Audit Logging: Comprehensive audit trails for system access, data modifications, and administrative actions, designed to support forensic investigation.  
* Log Retention: Security logs are retained for a minimum of 90 days to support forensic analysis and regulatory compliance requirements.

### **5.5 Incident Response & Forensic Capabilities**

Incident Classification & Response Procedures:

1. Detection: Automated monitoring systems provide real-time threat detection and alerting capabilities.  
2. Assessment: Our security team classifies incidents based on severity, scope, and potential impact to customer data and operations.  
3. Containment: Immediate isolation of affected systems using established automated and manual procedures.  
4. Investigation: Advanced forensic capabilities including:  
   * Comprehensive log analysis and correlation using industry-standard tools  
   * Digital evidence preservation with appropriate chain of custody procedures  
   * Root cause analysis using established methodologies  
   * Engagement of third-party forensic expertise when circumstances require

Customer Notification Procedures:

* Timeline: We endeavor to notify affected customers within 24 hours of confirming a security incident that may reasonably impact their data, subject to investigation requirements and legal constraints.  
* Communication: Direct notification to designated customer contacts with available incident details, impact assessment, and remediation measures being undertaken.  
* Collaboration: We provide reasonable cooperation in customer security investigations, including access to relevant logs and forensic evidence, subject to legal limitations and technical feasibility.  
* Transparency: Regular updates throughout incident resolution with final post-incident reports provided where appropriate.

Regulatory Compliance:

* GDPR breach notifications to supervisory authorities within 72 hours when required by applicable law.  
* Compliance with industry-specific notification requirements (including NIS2, state breach notification laws) as applicable to our operations.

### **5.6 Availability & Uptime Commitments**

Service Level Objectives:

* Target Availability: We target 99.9% uptime for production services, measured on a monthly basis, subject to exclusions.  
* Measurement: Availability is calculated as the percentage of time the service is accessible and functional during a calendar month.  
* Scheduled Maintenance: Up to 4 hours per month of scheduled maintenance, conducted during designated windows with minimum 72-hour advance notice.

Service Credits & Remedies:

* Service credits may be available for availability below SLA targets, subject to applicable terms and conditions in customer agreements.  
* Exclusions: Force majeure events, customer-caused issues, third-party service outages, and scheduled maintenance windows.  
* Reporting: Monthly uptime reports available to enterprise customers through designated channels.

### **5.7 Penetration Testing & Vulnerability Management**

Third-Party Security Assessments:

* Annual Penetration Testing: Independent third-party penetration tests conducted at least annually across application, infrastructure, and API surfaces.  
* Scope Coverage: Tests include OWASP Top 10, authentication mechanisms, authorization controls, input validation, and infrastructure security.  
* Remediation Timelines: Critical findings remediated within 30 days, high-severity within 90 days, subject to technical feasibility.

Continuous Security Monitoring:

* Automated Scanning: Weekly automated vulnerability scans across all production systems using industry-standard tools.  
* Dependency Scanning: Continuous monitoring of third-party dependencies for known vulnerabilities with automated alerting.  
* Patch Management: Security patches applied according to criticality: critical within 72 hours, high within 7 days, medium within 30 days.

Transparency & Reporting:

* Executive summaries of penetration test results available to enterprise customers under appropriate confidentiality agreements.  
* Vulnerability management metrics included in quarterly security posture reports where applicable.

### **5.8 Personnel Security & Insider Threat Management**

Employee Screening & Onboarding:

* Background Verification: Criminal background checks and reference verification for all personnel with access to production systems or customer data, where legally permissible.  
* Confidentiality Agreements: All personnel sign comprehensive confidentiality and acceptable use agreements prior to system access.  
* Security Training: Mandatory security awareness training during onboarding and annually thereafter, with role-specific technical training as appropriate.

Access Governance & Reviews:

* Principle of Least Privilege: Access rights granted based on job responsibilities with documented approval workflows.  
* Quarterly Reviews: Privileged access reviews conducted quarterly with management attestation.  
* Segregation of Duties: Critical functions separated to prevent unauthorized activities.  
* Activity Monitoring: User activity logging for privileged accounts with anomaly detection capabilities.

Separation Procedures:

* Immediate Revocation: System access terminated immediately upon employee separation or role change.  
* Third-Party/Vendor Access: Vendor and third-party system access removed immediately (target ≤ 24 hours) upon contract termination, role change, or when access is no longer required.  
* Exit Interviews: Security-focused exit procedures including return of all company assets and data.  
* Post-Departure Monitoring: Continued monitoring of systems for 90 days post-separation for anomalous activities.

### **5.9 Secure Software Development Lifecycle (SSDLC)**

Security by Design Principles:

* Threat Modeling: Comprehensive threat modeling for all new features and significant architectural changes using STRIDE or similar methodologies.  
* Security Requirements: Security requirements defined and tracked throughout the development lifecycle.  
* Architecture Reviews: Security architecture reviews for all major system components and integrations.

Secure Coding Practices:

* Code Standards: Enforced secure coding standards based on OWASP guidelines and language-specific best practices.  
* Peer Review: Mandatory code reviews with security-specific checklists before merge to main branches.  
* Security Champions: Designated security champions embedded within development teams for ongoing security guidance.

Security Testing Integration:

* Static Analysis (SAST): Automated static code analysis on every commit with build-breaking rules for critical issues.  
* Dynamic Testing (DAST): Dynamic application security testing performed in staging environments before each release.  
* Software Composition Analysis: Continuous scanning of dependencies for known vulnerabilities and license compliance.  
* Security Test Cases: Dedicated security test scenarios included in QA processes.

### **5.10 API Security Architecture**

Authentication & Authorization:

* Standards-Based: OAuth 2.0 implementation with short-lived access tokens and secure refresh token handling.  
* API Keys: Unique API keys per application with granular permission scoping and rotation capabilities.  
* Multi-Factor Authentication: MFA available for API access to sensitive operations where technically feasible.

Rate Limiting & Abuse Prevention:

* Tiered Limits: Rate limiting implemented based on subscription tiers and operation sensitivity.  
* Adaptive Throttling: Dynamic rate adjustment based on detected abuse patterns.  
* DDoS Protection: Cloud-based DDoS mitigation for all public-facing APIs.

Input Validation & Output Encoding:

* Comprehensive Validation: All API inputs validated against defined schemas with strict type checking.  
* Injection Prevention: Parameterized queries and context-aware output encoding to prevent injection attacks.  
* Content Security: API responses include appropriate security headers, including but not limited to HSTS and X-Content-Type-Options.

API Lifecycle Management:

* Versioning Strategy: Semantic versioning with backward compatibility commitments.  
* Deprecation Notices: Minimum 6-month notice for breaking changes with migration guides.  
* API Documentation: Comprehensive, up-to-date API documentation with security considerations highlighted.  
* Change Management: All API changes undergo security review before deployment.

---

## **6. AI Governance & Data Policy**

### **6.1 AI Training Data Practices**

Synthetic Data Methodology:

* We utilize synthetic datasets exclusively for AI model training activities, ensuring that customer personal data is not incorporated into model development processes.  
* Our models are trained and distilled from established foundation models using privacy-preserving techniques designed to maintain model performance while eliminating privacy risks.  
* This methodology eliminates privacy concerns traditionally associated with training data while maintaining model accuracy and effectiveness for intended use cases.

Data Lineage & Governance Framework:

* We maintain comprehensive data lineage tracking for abuse detection and cost verification purposes, implemented in accordance with our operational requirements.  
* Model performance monitoring includes drift detection and performance degradation alerting systems designed to maintain service quality.  
* Opt-In Telemetry: Performance monitoring of customer usage patterns requires explicit user consent and may be disabled through available controls at any time.

### **6.2 Model Transparency & Bias Prevention**

Model Development Practices:

* Risk-Based Approach to Bias Monitoring: Given that our models are distilled from established foundation models rather than trained on proprietary datasets, traditional bias monitoring protocols are not applicable to our development methodology.  
* Performance Monitoring: We continuously monitor model outputs for quality, accuracy, and potential performance issues using established metrics and procedures.  
* Version Control: All model versions are tracked with detailed change logs and performance metrics maintained for audit and quality assurance purposes.

Transparency & Communication:

* Clear documentation of model capabilities and limitations is provided to enterprise customers through available channels.  
* Model performance metrics and benchmarks are available upon reasonable request and subject to confidentiality restrictions.  
* Model updates are communicated through official channels with impact assessments provided where material changes occur.

---

## **7. Data Residency & Infrastructure**

### **7.1 Data Location & Sovereignty**

Primary Data Center Operations:

* Customer data is primarily stored in Google Cloud's Ohio, USA region (us-east5), subject to operational requirements and customer specifications.  
* Regional Options: Customers may specify preferred geographic regions for data storage to meet regulatory compliance requirements, subject to technical feasibility and service availability.

Data Residency Assurances:

* Written confirmation of data location may be provided in customer agreements, subject to ongoing operational requirements and service limitations.  
* Migration assistance may be available for customers with evolving residency requirements, subject to technical feasibility and applicable service terms.  
* Cross-border data transfers are conducted only with appropriate safeguards and, where required, explicit customer consent or contractual authorization.

### **7.2 Cloud Infrastructure & Self-Hosting Options**

Google Cloud Platform Foundation:

* Our infrastructure is built upon Google Cloud Platform, thereby benefiting from enterprise-grade security, compliance, and availability features, subject to GCP's terms and service limitations.  
* Multi-region redundancy with automated failover capabilities is implemented where technically feasible and commercially reasonable.  
* Customer data storage remains within customer-specified geographic boundaries, subject to service requirements and technical limitations.

Self-Hosting Solutions:

* Enterprise Container Deployment: We provide containerized deployment options for customers requiring on-premises or private cloud hosting, subject to technical requirements and support limitations.  
* Google Cloud Private Deployment: Self-hosting options may be available on customer-controlled Google Cloud infrastructure using our provided containers and documentation, subject to support terms and technical feasibility.  
* Data Sovereignty: Complete customer control over data location and access in self-hosted deployments, subject to customer's technical implementation and ongoing management responsibilities.

### **7.3 Multi-Tenant Architecture & Isolation**

Tenant Isolation Framework:

* Logical Separation: Row-level security implemented with tenant identifier validation on all data access operations.  
* Data Segregation: Customer data logically separated at the application layer with strict access controls preventing cross-tenant data access.  
* Query Isolation: All database queries include tenant-specific filtering to ensure data isolation at the query level.

Security Controls:

* Unique Encryption Keys: Where technically feasible, tenant-specific encryption keys are utilized for enhanced data protection.  
* Access Control: Role-based access control (RBAC) scoped to individual tenants, preventing any cross-tenant permission inheritance.  
* Session Management: Tenant-specific session handling with validation at each request to prevent session hijacking across tenants.

Resource Management:

* Resource Quotas: Per-tenant resource limits implemented to prevent resource exhaustion by individual tenants and ensure fair resource allocation.  
* Performance Isolation: Query optimization and caching strategies designed to prevent one tenant's usage from impacting others.  
* Storage Allocation: Tenant-specific storage quotas with monitoring and alerting for capacity management.

Audit & Compliance:

* Tenant-Specific Logging: Audit logs maintained separately per tenant with no possibility of cross-contamination.  
* Data Residency: Tenant data location preferences honored within our multi-tenant architecture where technically supported.  
* Compliance Isolation: Tenant-specific compliance requirements (such as data retention) can be configured independently.

---

## **8. Vendor & Supply Chain Security**

### **8.1 Third-Party Dependencies**

Simplified Supply Chain Architecture:

* We maintain a minimal vendor dependency model, relying exclusively on:  
  * Google Cloud Platform for infrastructure and core services  
  * GitHub for code repository and development workflow security  
  * Sentry.io for Crashlytics, Descope.com for Authentication, Paddle.com for Payments, Satismeter for NPS and Product Feedback, Mixpanel.io, and Segment.com, HubSpot.com for Support and Customer.io for Email Communications

Vendor Security Assessment:

* Google Cloud and GitHub maintain SOC 2 Type II, ISO 27001, and other enterprise security certifications, which we monitor for currency and validity.  
* We conduct periodic monitoring of vendor security posture and compliance status through available information and assessments.  
* Vendor security incidents are evaluated for potential customer impact with appropriate notifications provided where required.

### **8.2 Software Bill of Materials (SBOM)**

Component Transparency & Management:

* We maintain a comprehensive Software Bill of Materials detailing software components, libraries, and dependencies utilized in our platform, updated in accordance with our development processes.  
* Open Source Components: All open source dependencies are tracked with version information and known vulnerability status monitoring.  
* Vulnerability Management: Automated scanning and remediation of dependencies with security updates applied in accordance with our change management procedures.  
* Customer Access: SBOM information is available to enterprise customers upon reasonable request for their security assessment purposes, subject to confidentiality restrictions.

Supply Chain Security Measures:

* Dependency Scanning: Continuous monitoring of software dependencies for security vulnerabilities using automated tools and processes.  
* Automated Updates: Security patches are applied automatically where possible, with testing protocols implemented for critical updates.  
* Minimal Attack Surface: Our simplified architecture design reduces potential supply chain vulnerabilities through dependency minimization.

---

## **9. Compliance & Audit Support**

### **9.1 Audit Capabilities**

Customer Audit Support Services:

* Documentation Access: Security documentation, policies, and procedures are available for customer review, subject to confidentiality restrictions and reasonable request procedures.  
* Audit Logs: Detailed access and activity logs are available for customer security investigations, subject to technical capabilities and legal limitations.  
* Third-Party Assessments: SOC 2 reports and other compliance documentation may be shared with customers under appropriate confidentiality agreements.  
* Assessment Support: We provide reasonable support for customer security assessments and due diligence processes, subject to resource availability and commercial terms.

### **9.2 Regulatory Compliance**

Privacy Regulation Compliance:

* GDPR Compliance: We maintain compliance with EU General Data Protection Regulation requirements applicable to our processing activities.  
* CCPA/CPRA: California Consumer Privacy Act compliance is maintained for applicable customer data processing activities.  
* Regional Privacy Laws: We endeavor to comply with applicable privacy laws in jurisdictions where we provide services, subject to legal analysis and operational feasibility.

Security Standards Alignment:

* SOC 2 Type II: Annual certification maintained with commitment to continuous compliance, subject to certification body requirements.  
* ISO 27001: Our practices are designed to align with international security management standards, adapted to our operational environment.  
* Industry Standards: Compliance with sector-specific requirements as applicable to customer use cases and contractual obligations.

### **9.3 Compliance Roadmap**

Current or In-Renewal Certifications & Attestations:

* SOC 2 Type II: Currently certified with annual renewal in progress (expected completion: Sep 1, 2025)  
* GDPR Compliance: Primarily, implemented with Head of Cloud Infrastructure and Data Protection Head, designated and accompanied by documented procedures  
* CCPA/CPRA: Compliant with documented data subject request procedures and privacy notices

12-Month Targets:

* ISO 27001 Certification: Implementation of Information Security Management System (ISMS) with target certification by December 1, 2025 + 6 months  
* Enhanced Penetration Testing: Transition to annual third-party penetration testing schedule  
* Zero Trust Architecture: Complete implementation of zero trust principles across all systems

24-Month Targets:

* HIPAA Compliance: Business Associate Agreement (BAA) capability and technical safeguards (available upon customer demand)  
* ISO 27017 (Cloud Security): Extension of ISO framework to cloud-specific controls

Available Upon Request:

* Custom Compliance: Support for customer-specific compliance requirements through contractual commitments  
* Industry Frameworks: Alignment with NIST, CIS Controls, or other frameworks based on customer needs  
* Attestation Letters: Formal attestations for specific security controls or compliance requirements

Continuous Improvement:

* Quarterly review of compliance landscape and customer requirements  
* Annual third-party compliance assessment to identify gaps and opportunities  
* Regular updates to this roadmap based on customer feedback and regulatory changes

---

## **10. Financial Assurance & Risk Transfer**

### **10.1 Support Response Commitments**

Tiered Support Model:

| Priority Level | Initial Response Time | Target Resolution | Availability |
| :---- | :---- | :---- | :---- |
| Critical (P1) | 4 hour | 12 hours | Continuous availability |
| High (P2) | 8 hours | 36 hours | Business hours |
| Medium (P3) | 12 hours | 72 hours | Business hours |
| Low (P4) | 24 hours | Best effort | Business hours |

Enterprise Support Features:

* Dedicated Success Manager: Named technical account manager for enterprise accounts  
* Quarterly Business Reviews: Regular reviews of usage, performance, and roadmap alignment  
* Priority Escalation: Direct access to engineering team for critical issues  
* Custom SLAs: Negotiable service level agreements for enterprise customers

Support Channels & Resources:

* Continuously Available Emergency Hotline: For critical production issues (enterprise customers)  
* Support Portal: Ticket submission and tracking with real-time status updates  
* Knowledge Base: Comprehensive self-service documentation and troubleshooting guides  
* Community Forums: Peer support and best practices sharing

Continuous Improvement:

* CSAT Monitoring: Customer satisfaction scores tracked and reported quarterly  
* Root Cause Analysis: Systematic root cause analysis for all Priority 1 and Priority 2 incidents with preventive measures  
* Support Metrics: Monthly reporting on response times, resolution rates, and customer feedback

---

## **11. Appendices**

### **Appendix A: Definitions**

* RTO (Recovery Time Objective): The maximum tolerable downtime for a system or service during a disruption.  
* RPO (Recovery Point Objective): The maximum tolerable data loss measured in time duration during a disaster event.  
* PII: Personally Identifiable Information, meaning data that can reasonably identify a specific individual.  
* DPA (Data Processing Addendum): A contract that governs the handling of personal data between parties in accordance with applicable privacy laws.  
* SBOM (Software Bill of Materials): A comprehensive inventory of all software components, libraries, dependencies, and their versions used in a software product.  
* Zero Trust Architecture: A security model that requires verification of every user and device before granting access, regardless of their network location.  
* Synthetic Data: Artificially generated data that mimics real data patterns without containing actual personal information.  
* Data Lineage: The tracking of data's origin, movement, and transformation throughout its lifecycle within systems.  
* SOC 2 Type II: A security audit that evaluates the operational effectiveness of security controls over a specified period of time.  
* MFA (Multi-Factor Authentication): A security method requiring two or more verification factors to access systems or data.  
* Data Residency: The physical or geographic location where data is stored and processed, subject to applicable legal requirements.  
* SAST (Static Application Security Testing): Automated security testing that analyzes source code for vulnerabilities without executing the program.  
* DAST (Dynamic Application Security Testing): Security testing that analyzes running applications for vulnerabilities by simulating attacks.  
* RBAC (Role-Based Access Control): An access control method that restricts system access based on a user's role within an organization.  
* SSDLC (Secure Software Development Lifecycle): A framework that integrates security practices throughout all phases of software development.  
* API (Application Programming Interface): A set of protocols and tools for building software applications and enabling system interactions.  
* OAuth 2.0: An industry-standard protocol for authorization that enables applications to obtain limited access to user accounts.  
* STRIDE: A threat modeling methodology that categorizes threats as Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, and Elevation of privilege.  
* Priority Levels (P1/P2/P3/P4): Designation system for support ticket urgency, with Priority 1 (P1) representing the most critical issues and Priority 4 (P4) representing the lowest priority matters.  
* BAA (Business Associate Agreement): A HIPAA-required contract between a covered entity and a business associate that handles protected health information.  
* FedRAMP (Federal Risk and Authorization Management Program): A U.S. government program that provides a standardized approach to security assessment for cloud products and services.

### **Appendix B: Request Channels**

General Inquiries:

* Privacy / Data Subject Requests: privacy@pieces.app  
* Security & Incident Reports: security@pieces.app  
* General Support: support@pieces.app

Emergency Contacts:

* Continuously Available Security Hotline: (513) 572-3339 (Critical security incidents only)  
* Executive Escalation: tsavo@pieces.app

Documentation & Resources:

* Product Documentation: https://docs.pieces.app
* Product Support: https://github.com/pieces-app/support/issues

---

Legal Disclaimer: In the event of any conflict between this document and an executed Master Service Agreement (MSA), Data Processing Addendum (DPA), or other contractual agreement, the terms of the executed contract shall prevail. We reserve the right to update these policies from time to time in response to legal, technical, or business developments, with appropriate notice provided as required by applicable law or contract.
