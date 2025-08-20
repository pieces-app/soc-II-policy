---
title: Operations Security Policy
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
stakeholders:
  - Mark Widman (Chief Technology Officer)
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Legal Counsel
approver: Tsavo Knott (CEO)
version: 1.3.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards: []
  procedures: []
  controls: []
repo: https://github.com/pieces-app/soc-II-policy
---

# **Operations Security Policy** 

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))

**Effective Date:** August 19, 2025 

# **Purpose** 

To ensure the correct and secure operation of information processing systems and facilities.

# **Scope** 

All Mesh Intelligent Technologies, Inc. information systems that are business critical and/or process, store, or transmit company data. This Policy applies to all employees of Mesh Intelligent Technologies, Inc. and other third-party entities with access to Mesh Intelligent Technologies, Inc. networks and system resources.

# **Operations Security**

## **Documented Operating Procedures**

Both technical and administrative operating procedures shall be documented as needed and made available to all users who need them. Configuration-as-code and runbooks are maintained in version control (GitHub) and/or internal documentation.

## **Change Management**

Changes to the organization, business processes, information processing facilities, production software and infrastructure, and systems that affect information security in the production environment and financial systems shall be tested, reviewed, and approved prior to production deployment. All significant changes to in-scope systems and networks must be documented.

Change management processes shall include:

- Planning and testing: Plan and test changes in segregated environments (staging) with rollback plans; document potential impact considering dependencies.  
- Approvals: Documented managerial/owner approval before proceeding with changes that may have significant impact on information security, operations, or production platforms. Pull requests require required reviewers per CODEOWNERS.  
- Communication: Advance communication/warning of changes, including schedules and anticipated effects, provided to all relevant internal stakeholders; customer communications coordinated via Corporate Secretary/Legal if required.  
- Emergency changes: Emergency changes may be expedited but must undergo retrospective review and authorization within two business days.  
- Remediation: Unsuccessful changes are promptly remediated or rolled back; evidence is attached to the change record.  
- Records: Change records are retained in tickets and/or GitHub PRs with links to tests, approvals, and deploy logs.

Infrastructure-as-Code and Drift: Production infrastructure changes are made via infrastructure-as-code (IaC) and reviewed through GitHub pull requests. Enable drift detection/alerts for critical stacks where feasible and reconcile drift via code. 

No Console-Only Changes: Infrastructure changes must be performed via IaC (no console-only changes in production). Emergency console actions must be captured in tickets and reconciled back to IaC promptly.

Change Windows: Customer-impacting maintenance follows defined windows and requires ≥ 24 hours advance notification coordinated by the Corporate Secretary/Legal per the Legal & Security Policies.

## **Capacity Management**

The use of processing resources and system storage shall be monitored and adjusted to ensure that system availability and performance meets Mesh Intelligent Technologies, Inc. requirements. Human resource skills, availability, and capacity shall be reviewed and considered as a component of capacity planning and as part of the annual risk assessment process.

Scaling resources for additional processing or storage capacity, without changes to the system, can be performed using cloud-native scaling (e.g., GCP autoscaling) and does not require full code change procedures.

## **DDoS and Edge Protections**

Public-facing endpoints are protected using cloud-native WAF/DDoS controls (e.g., Google Cloud Armor) and rate limiting where applicable. TLS is enforced for all external endpoints; cipher configurations follow the Cryptography Policy.

## **GitHub Organization Security Baseline**

We enforce an organization-wide security baseline for GitHub (see `policies/Operations Security Policy/github-org-security-baseline.md`), including: branch protection with required reviewers and status checks, CODEOWNERS, GHAS secret scanning with push protection, Dependabot security updates, protected environments with deployment approvals for production, Actions pinned by commit SHA, self-hosted runner scoping, and OIDC-based workload identity to GCP.

## **Google Workspace Admin Baseline**

We enforce SSO/MFA for Workspace, enable anti-phishing/attachment protections, and maintain audit logging. Admin roles are assigned by least privilege and reviewed periodically (see `policies/Operations Security Policy/google-workspace-admin-baseline.md`).

## **Data Leakage Prevention**

We classify information per the Data Management Policy and provide awareness training on appropriate handling. Where feasible, we enable label-aware DLP in Google Workspace (sharing restrictions, warnings/blocks) and repository secret scanning (GitHub Advanced Security). Transfers of Confidential data outside approved systems require management approval.

## **Web Filtering**

We enforce safe, secure internet use through endpoint protection and browser controls. Access to known malicious sites is blocked via provider protections; users must follow the Code of Conduct and Acceptable Use Policy. Additional restrictions may be applied based on risk and role.

## **Separation of Development, Staging and Production Environments**

Development and staging environments shall be strictly segregated from production environments to reduce the risks of unauthorized access or changes to the operational environment. Confidential production customer data must not be used in development or test environments without the express approval of the CPO/Corporate Secretary or CTO and implementation of de-identification where feasible.

Refer to the Data Management Policy for a description of Confidential data. If production customer data is approved for use in the course of development or testing, it shall be scrubbed of any such sensitive information whenever feasible.

# **Systems and Network Configuration, Hardening, and Review**

Systems and networks shall be provisioned and maintained in accordance with configuration and hardening standards described in Appendix A to this policy. Firewalls and/or appropriate network access controls and configurations shall be used to control network traffic to and from the production environment in accordance with this policy. Production network access configuration rules shall be reviewed at least annually. Tickets shall be created to obtain approvals for any needed changes.

# **Protection from Malware**

In order to protect the company's infrastructure against the introduction of malicious software, detection, prevention, and recovery controls to protect against malware shall be implemented, combined with appropriate user awareness.

Anti-malware protections shall be utilized on all company-issued endpoints except for those running operating systems not normally prone to malicious software. Threat detection and response software shall be utilized for company email. The anti-malware protections utilized shall be capable of detecting common forms of malicious threats and performing the appropriate mitigation activity (such as removing, blocking or quarantining).

All files should be scanned upon introduction to systems, and scanning should occur upon access, modification, or download where supported. Anti-malware definition and engine updates should be configured to be downloaded and installed automatically whenever new updates are available. Known or suspected malware incidents must be reported as a security incident. It is a violation of company policy to disable or alter the configuration of anti-malware protections without authorization.

## **Endpoint and Email Security**

Endpoint Detection & Response (EDR) and Mobile Device Management (MDM) baselines are enforced per the Asset Management Policy (full-disk encryption, screen lock, auto-updates, remote wipe, posture checks). Google Workspace anti-phishing and attachment scanning are enabled for corporate email.

# **Information Backup**

The need for backups of systems, databases, information and data shall be considered and appropriate backup processes shall be designed, planned and implemented. Backup procedures must include procedures for maintaining and recovering customer data in accordance with documented SLAs. Security measures to protect backups shall be designed and applied in accordance with the confidentiality or sensitivity of the data. Backup copies of information, software and system images shall be taken regularly to protect against loss of data. Backups and restore capabilities shall be periodically tested, not less than annually; production data restore tests are performed at least quarterly per the BC/DR plan.

Backups must be stored separately from the production data location (e.g., different region/bucket where feasible). Mesh Intelligent Technologies, Inc. does not regularly backup user devices like laptops. Users are expected to store critical files and information in company-sanctioned file storage repositories. Backup schedules are maintained within backup or platform software.

Backup Specifics (summary; see BC/DR Plan for detail):
- Cloud SQL/managed data stores: automated daily backups, point-in-time recovery where supported; quarterly restores to staging for validation.  
- Google Cloud Storage: server-side encryption, checksums, and versioning for critical buckets where feasible; quarterly restore tests.  
- Artifact Registry (GAR): releases and attestations retained with artifacts; verify availability during DR exercises.  
- Evidence: restore test artifacts stored under `evidence/bcdr/` in this repository.

# **Service Accounts and Workload Identity**

- Prefer Workload Identity Federation (OIDC) for CI/CD and service-to-service access; avoid long-lived service account keys.  
- Service account keys (if unavoidable) must be minimally scoped, stored only in approved secret managers, and rotated on a periodic cadence appropriate to risk (≤ 180 days) and immediately after incidents.  
- Prohibit embedding keys in repositories or container images; enforce secret scanning and attestations in release pipelines.

# **Logging & Monitoring**

Production infrastructure shall be configured to produce detailed logs appropriate to the function served by the system or device. Event logs recording user activities, exceptions, faults and information security events shall be produced, kept and reviewed through automated alerting and manual triage by engineering/security. Appropriate alerts shall be configured for events that represent a significant threat to the confidentiality, availability or integrity of production systems or Confidential data.

Logging should meet the following criteria for production applications and supporting infrastructure:

- Log user log-in and log-out.  
- Log CRUD (create, read, update, delete) operations on application and system users and objects.  
- Log security settings changes (including disabling or modifying of logging).  
- Log application owner or administrator access to customer data (Access Transparency where supported).  
- Logs must include user ID, IP address, valid timestamp, type of action performed, and object of this action.  
- Logs must be retained for at least 365 days for production infrastructure; logs should not contain sensitive data or payloads.  

Daily Log Review: Engineering/Security performs daily review of alerts and key logs, in addition to automated monitoring, to identify anomalies (e.g., unusual traffic, brute force attempts, anomalous external connections, DDoS-like spikes, malware alerts, unauthorized access/changes, suspicious file modifications). Suspected events are escalated per the Incident Response Plan.

Identified anomalies or suspicious activities should be escalated to the incident response team for further investigation and action, in line with the Incident Response Plan.

Log Immutability: Where feasible, enable write-once-read-many (WORM)/retention lock for security logs to prevent tampering within retention windows.

Monitoring Stack & Alerting: Cloud Logging/Monitoring, Sentry, and GitHub Advanced Security provide operational and security signals. Alerts page the on-call engineer via the on-call policy; severe events (e.g., Sev-1) trigger immediate page and executive escalation. 

On-call & Escalation: Follow the BC/DR runbook for activation (see `policies/Business Continuity and Disaster Recovery Plan/bcdr-activation-runbook.md`) and record timelines in the event log template (`policies/Business Continuity and Disaster Recovery Plan/bcdr-event-log-template.md`).

Paging Timelines: Sev-1 pages immediately (target ≤ 5 minutes to acknowledge); escalate to L2/owner within ≤ 15 minutes if unresolved.

## **Protection of Log Information**

Logging facilities and log information shall be protected against tampering and unauthorized access through role-based access controls and the principle of least privilege.

## **Administrator & Operator Logs**

System administrator and system operator activities shall be logged and reviewed and/or alerted in accordance with the system classification and criticality.

## **Data Restore Logs**

Restores of production data containing PII from backups, either for the purposes of providing services or for testing purposes, shall be logged or tracked in auditable tickets.

## **Clock Synchronization**

The clocks of all relevant information processing systems shall be synchronized to network time servers using reputable time sources.

## **File Integrity Monitoring, Alerting and Intrusion Detection**

Production systems shall be configured to monitor, log, and alert on suspicious changes to critical system files where feasible. Alerts shall be configured for suspicious conditions and engineers shall review logs in line with the Logging & Monitoring policy. Suspicious conditions include, but are not limited to:
- Unusual or unauthorized network traffic patterns  
- Port scanning, brute force attacks, or other suspicious network activities  
- Anomalous connections from external or unexpected IP addresses  
- Unusual traffic spikes that may indicate DDoS  
- Alerts triggered by anti-malware/email security  
- Unauthorized access or changes to critical files and databases  
- Suspicious file renaming, deletion, or modification activities  

Unauthorized intrusions and access attempts or changes to systems shall be investigated and remediated in accordance with the Incident Response Plan.

# **Secrets Management (Operational Guardrails)**

- No secrets in source code or images; secret scanning/push protection enabled via GitHub Advanced Security.  
- Secrets are stored in approved secret managers; access is logged and reviewed.  
- Rotation: secrets and certificates are rotated after security incidents and on a periodic cadence appropriate to risk; rotation evidence is retained.  
- Break-glass: use of break-glass credentials requires prior approval (or immediate CEO/CTO notification if urgent), is time-bound, and is logged with post-use review.

# **Control of Operational Software**

The installation of software on production systems shall follow the change management requirements defined in this policy.

# **Technical Vulnerability Management**

Information about technical vulnerabilities of information systems being used shall be obtained in a timely fashion, exposure shall be evaluated, and appropriate measures taken to address the associated risk. Methods include vulnerability scanning, penetration tests, vendor alerts, and bug bounty inputs.

Vulnerability scans shall be performed on public-facing systems in the production environment at least quarterly. Penetration tests of the applications and production network shall be performed at least annually, and additional scanning and testing shall be performed following major changes to production systems and software.

Engineering evaluates severity; if a critical or high-risk vulnerability is identified, a service ticket is created and assigned to the system/application/platform owner for investigation and remediation.

Vulnerabilities shall be patched or remediated in the following timeframes:

| Determined Severity | Remediation Time |
| ----- | ----- |
| Critical (CVSS 9.0–10.0) | 0 Days (immediate) |
| High (CVSS 7.0–8.9) | 30 Days |
| Medium (CVSS 4.0–6.9) | 60 Days |
| Low (CVSS 0.1–3.9) | 90 Days |
| Informational (CVSS 0) | As needed |

Tickets for any vulnerability which cannot be remediated within the standard timeline must show a risk treatment plan and planned remediation timeline.

# **Restrictions on Software Installation**

Rules governing the installation of software by users shall be established and implemented in accordance with the Information Security Policy.

# **Patch Management**

Having strong patch management processes in place is paramount to maintaining and operating a secure computing environment. Our policy covers all in-scope components of the information technology infrastructure deployed and managed by our company. This includes, but is not limited to:

- Servers (virtual and physical)
- Databases
- Storage systems
- Load Balancers
- Web Application Servers
- Firewalls, routers, and other network devices
- Container images and orchestration platforms
- All other software and hardware components

All components are required to run OS/software that is supported by the vendor. All systems running unsupported OS/software must be updated or decommissioned within a timely manner.

Identification of vulnerabilities within the code base, including within third-party libraries, is done according to the procedures detailed above in the Technical Vulnerability Management section.

To minimize downtime, patching takes place during off-peak usage. In cases where a patch is necessary to remediate a high or critical vulnerability, patching will take place ad hoc. All patches are issued within the minimal window defined for each risk ranking:

| Determined Severity | Remediation Time |
| ----- | ----- |
| Critical (CVSS 9.0–10.0) | 0 Days (immediate) |
| High (CVSS 7.0–8.9) | 30 Days |
| Medium (CVSS 4.0–6.9) | 60 Days |
| Low (CVSS 0.1–3.9) | 90 Days |
| Informational (CVSS 0) | As needed |

Patch management evidence (tickets, deployment logs, scan results) is stored under `evidence/ops/patches/`.

# **Information Systems Audit Considerations**

Audit requirements and activities involving verification of operational systems shall be carefully planned and agreed to minimize disruptions to business processes.

# **Systems Security Assessment & Requirements** 

Risks shall be considered prior to the acquisition of, or significant changes to, systems, technologies, or facilities. Where requirements are formally identified, any relevant security requirements shall be included. The acquisition of new suppliers and services shall be made in accordance with the Third-Party Management Policy.

An annual network security assessment includes a review of major changes to the environment such as new system components and network topology.

# **Threat Intelligence**

Threat intelligence shall be collected, analyzed, and disseminated to relevant teams to proactively identify and mitigate emerging threats.

- Collection: Vendor advisories (Google, GitHub, DigiCert), CISA alerts, bug bounty reports, security community feeds, industry threat reports
- Analysis: Evaluate applicability to our stack (GCP, GitHub, Google Workspace), prioritize by impact/likelihood
- Dissemination: Share actionable intelligence with engineering, ops, and executive teams via security bulletins
- Feedback: Track effectiveness of threat-based mitigations in the Risk Register
- Evidence: Store threat intelligence reports and actions taken under `evidence/ops/threat-intel/`

# **Data Masking**

Sensitive data shall be masked or tokenized in non-production environments and logs:

- Production data in dev/staging: De-identify PII/secrets; use synthetic data where feasible per Data Management Policy
- Log scrubbing: Remove/mask sensitive fields (passwords, tokens, PII) before ingestion; configure Sentry PII scrubbing
- Database masking: Apply column-level masking for sensitive fields when replicating to non-prod
- Testing data: Generate synthetic test data matching production schemas without real customer data
- Evidence: Masking configurations and validation tests stored under `evidence/ops/data-masking/`

# **Zero Trust Architecture Principles**

We implement Zero Trust principles across our infrastructure:

- Never trust, always verify: All access requires authentication and authorization regardless of network location
- Least privilege access: Users and services receive minimal permissions required for their function
- Assume breach: Design systems assuming attackers have network presence; segment and isolate critical resources
- Verify explicitly: Use multiple signals (identity, device, location, behavior) for access decisions
- Inspect and log all traffic: Full visibility into all communications, encrypted or not
- Implementation: Identity-Aware Proxy for GCP resources, service mesh for inter-service auth, continuous verification

# **AI/ML Operational Security**

Specific controls for AI/ML workloads:

- Model versioning: All models tracked in Hugging Face with immutable version pins for rollback capability
- Training data governance: Data provenance tracked, access logged, retention per Data Management Policy
- Model access control: API keys scoped per environment; rate limiting enforced; usage monitored
- Adversarial protection: Input validation, output filtering, prompt injection detection where applicable
- Compute isolation: ML workloads run in dedicated GCP projects with restricted IAM and network policies
- Model registry security: Hugging Face repositories private by default; access via SSO/MFA; audit logging enabled
- Evidence: Model deployment logs and access records under `evidence/ops/ml-operations/`

# **API Security**

APIs shall be secured with defense-in-depth controls:

- Authentication & Authorization: OAuth 2.0/OIDC with JWT validation; API keys for service accounts with rotation
- Rate Limiting: Per-client and global limits enforced via Cloud Armor; DDoS protection on all public endpoints
- Input Validation: Schema validation, size limits, type checking; reject malformed requests early
- Output Filtering: Sensitive data scrubbing; consistent error responses without stack traces
- Versioning & Deprecation: Semantic versioning with sunset notices; maintain compatibility during transitions
- Monitoring: Log all API calls with request/response metadata (excluding sensitive data); alert on anomalies
- Documentation: OpenAPI specs maintained; security requirements documented per endpoint

# **Supply Chain Security**

Software supply chain shall be secured through:

- Dependency Scanning: Dependabot enabled org-wide; daily scans for vulnerabilities; auto-PRs for patches
- SBOM Generation: CycloneDX format via Syft for releases where feasible; stored with artifacts
- Artifact Signing: Code signing for Windows (DigiCert Authenticode); container signing via GAR attestations
- Build Provenance: SLSA Level 3 attestations where supported; build logs retained with artifacts
- Third-Party Assessment: Vendors assessed per Third-Party Management Policy; security questionnaires required
- Open Source Policy: License compliance scanning; approved list for critical dependencies
- Evidence: SBOMs, attestations, and scan results under `evidence/ops/supply-chain/`

# **Container & Kubernetes Security**

Container workloads shall follow security best practices:

- Image Security: Base images from trusted registries; vulnerability scanning before deployment; distroless where feasible
- Runtime Security: Read-only filesystems; no privileged containers; security contexts enforced
- Network Policies: Default deny; explicit allow rules; service mesh for mTLS between pods
- Secrets Management: External secrets operator; no hardcoded secrets; rotation automated
- Resource Limits: CPU/memory limits enforced; horizontal pod autoscaling configured
- Admission Control: Policy enforcement via OPA/Gatekeeper; pod security standards applied
- Monitoring: Container runtime monitoring; anomaly detection; audit logging to Cloud Logging

# **Infrastructure as Code Security**

IaC shall be secured throughout lifecycle:

- Policy as Code: Security policies defined in code; automated validation before deployment
- Static Analysis: IaC scanning for misconfigurations (e.g., public buckets, weak encryption)
- Drift Detection: Daily scans for configuration drift; alerts on unauthorized changes (where tooling available)
- Version Control: All IaC in GitHub with branch protection; required reviews for production changes
- Secrets Management: No secrets in IaC; use secret references and runtime injection
- Testing: IaC changes tested in staging; automated rollback on failure
- Documentation: Infrastructure documented as code; architecture diagrams updated with changes

# **Security Metrics & KPIs**

Operational security effectiveness measured through:

- Vulnerability Metrics: Mean time to detect (MTTD), mean time to remediate (MTTR) by severity
- Patch Compliance: % systems patched within SLA; age of oldest unpatched vulnerability
- Access Reviews: % completed on time; # of excess privileges removed; # of orphaned accounts
- Incident Metrics: # of incidents by type; MTTD/MTTR; % prevented by controls
- Audit Findings: # of findings by severity; time to remediation; repeat findings
- Training Compliance: % staff completed security training; phishing simulation click rates
- Monitoring Coverage: % of systems with logging; alert-to-incident ratio; false positive rate
- Evidence: Metrics dashboards and reports under `evidence/ops/metrics/`

# **Incident Response Integration**

Security incidents detected through operational monitoring shall be handled per the Incident Response Plan (`policies/Incident Response Plan/incident-response-plan-2023.md`):

- Detection: Alerts from monitoring tools (Cloud Security Command Center, Sentry, GitHub Advanced Security) trigger incident evaluation
- Classification: Events assessed for impact and classified as security events or incidents per IRP definitions
- Escalation: Security incidents immediately escalated to incident response team via established channels
- Insurance Notification: CFO notifies At-Bay Specialty Insurance Company within 24 hours for incidents with potential claims
- Containment: Operational controls (network isolation, access revocation, service suspension) available for rapid containment
- Evidence: Preserve logs, snapshots, and forensic data; chain of custody maintained
- Recovery: Restore operations per BC/DR procedures; verify integrity before returning to production
- Lessons Learned: Post-incident review to improve operational controls and detection capabilities

# **Continuous Compliance Monitoring**

Compliance posture continuously monitored through:

- Vanta Integration: Automated control monitoring and evidence collection for SOC 2/ISO 27001
- Cloud Security Posture: Security Command Center for GCP misconfigurations and compliance violations
- Policy Violations: Automated alerts for policy breaches (e.g., public buckets, excessive permissions)
- Audit Trail: Immutable audit logs for all administrative and security-relevant actions
- Remediation Tracking: Issues tracked in ticketing system with SLAs based on severity
- Executive Reporting: Monthly security posture reports to leadership; quarterly board updates
- Evidence: Compliance reports and remediation records under `evidence/ops/compliance/`

# **Operations Evidence**

Operational evidence (e.g., maintenance notices, change approvals, org policy exports, GHAS/Dependabot enforcement screenshots, vulnerability scans, penetration test reports) is stored in this repository under `evidence/ops/` with dated subfolders and brief README notes:

- `evidence/ops/vuln-scans/` - Quarterly vulnerability scan reports
- `evidence/ops/pen-tests/` - Annual penetration test reports and remediation tracking
- `evidence/ops/patches/` - Patch management tickets and deployment logs
- `evidence/ops/github/` - GitHub org security settings and GHAS reports
- `evidence/ops/workspace/` - Google Workspace admin configurations
- `evidence/ops/maintenance/` - Change notices and approvals
- `evidence/ops/threat-intel/` - Threat intelligence reports and actions
- `evidence/ops/ml-operations/` - ML model deployments and access logs
- `evidence/ops/data-masking/` - Data masking configurations and tests
- `evidence/ops/supply-chain/` - SBOMs, attestations, and dependency scans
- `evidence/ops/metrics/` - Security metrics dashboards and KPI reports
- `evidence/ops/compliance/` - Continuous compliance monitoring reports

# **Exceptions**

Requests for an exception to this policy must be submitted to the IT/Engineering leadership for approval. Exceptions are time-bound and must include scope, compensating controls, owner, and expiration.

# **Violations & Enforcement**

Any known violations of this policy should be reported to the Head of Cloud Infrastructure & Security. Violations of this policy can result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## **Version History**

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0 | 8-March-2023 | First Version | Mack Myers | Tsavo Knott |
| 1.1 | 13-July-2023 | Patch Management | Georgia Donmoyer | Mack Myers |
| 1.2 | 14-August-2023 | Expanded Logging & Alerting | Georgia Donmoyer | Mack Myers |
| 1.3 | 19-August-2025 | 2025 Refresh - Cloud-native focus, GitHub/GCP specifics | Mack Myers | Tsavo Knott (CEO) |

# **APPENDIX A - Configuration and Hardening Standards**

Configuration and hardening standards are maintained in internal documentation. Address baseline config management and deployment per control 3.4, 7.1.

**Servers and Virtual Machines**  
This is the standard for system-level server and virtual server (VM) configuration hardening. Some customization to these settings may be required to configure the system for its specific target environment.

All physical and virtual systems must adhere to the following technical requirements:
- Change all vendor defaults (including default passwords on OS/software, application/system accounts, SNMP strings) before network exposure.  
- Remove/disable unnecessary default accounts before system deployment.  
- Configure access control lists to allow only necessary protocols, ports, and services.
- Install critical security patches and updates within defined SLAs.
- Enable host-based firewalls and configure for least-privilege network access.
- Enable audit logging for security events, system access, and privilege escalation.
- Configure automatic security updates where feasible; manual updates with change control otherwise.
- Implement file integrity monitoring for critical system files.
- One primary function per VM where feasible.  
- Enable only necessary services, protocols, daemons; disable unnecessary functionality.
- Configure secure time synchronization (NTP).
- Enforce strong authentication per Access Control Policy.
- Encrypt data at rest and in transit per Cryptography Policy.
- Apply critical/high security patches within SLAs defined above.  

**Network Standards (GCP)**  
- Management of network rules/settings performed by authorized engineering personnel and changes follow change management.  
- Maintain current network diagrams; review at least annually.  
- Use VPC/subnet isolation and firewall rules to restrict inbound/outbound traffic; default deny except required services/ports.  
- Use NAT to prevent disclosure of internal IPs; any exceptions documented and reviewed.  
- Enforce anti-spoofing; limit inbound to authorized services; restrict port/IP ranges unless justified.  
- Enforce remote access timeouts; vendor access enabled only when needed and disabled after use.  
- Hybrid links (if any) scanned/tested at least annually for security requirements.  
- TLS Everywhere: All external and internal service communications use TLS as feasible; cryptographic baselines follow the Cryptography Policy.  

**GCP-Specific Hardening**  
- Organization Policies: Enforce constraints (e.g., restrict public IPs, require OS Login, disable service account key creation)
- VPC Service Controls: Implement perimeters for sensitive projects; restrict data exfiltration
- Cloud IAM: No direct user bindings where feasible; use groups; enable IAM Conditions for context-aware access
- Cloud KMS: Customer-managed encryption keys (CMEK) for sensitive data; HSM backing for critical keys
- Cloud Storage: Uniform bucket-level access; versioning and retention locks; signed URLs for temporary access
- Compute Engine: Shielded VMs; OS Login enforced; metadata concealment; sole-tenant nodes for sensitive workloads
- Cloud SQL: Private IP only; SSL enforced; automated backups with PITR; maintenance windows defined
- Logging: Cloud Audit Logs (Admin, Data Access, System Event) enabled; exported to Cloud Storage with retention lock
- Binary Authorization: Enforce container image signatures for GKE deployments
- Security Command Center: Enable for continuous posture monitoring and compliance scanning

**Container Hardening (GKE/Cloud Run)**  
- Cluster Security: Private GKE clusters; authorized networks; Workload Identity enabled
- Node Security: Container-Optimized OS (COS); auto-upgrade enabled; node auto-repair
- Pod Security: Pod Security Standards enforced; security contexts (non-root, read-only root filesystem)
- Network Policies: Calico/Cilium for micro-segmentation; Istio service mesh for mTLS
- Image Scanning: Vulnerability scanning in Artifact Registry; block critical vulnerabilities
- Runtime Protection: Falco or similar for runtime threat detection; seccomp/AppArmor profiles
- Secrets: Workload Identity for service account impersonation; Secret Manager integration
- Compliance: CIS Kubernetes Benchmark compliance; regular security assessments

**Endpoint Hardening**  
- OS Hardening: CIS benchmarks applied; unnecessary services disabled; host firewall enabled
- Patch Management: Automatic security updates where feasible; managed patching for servers
- Endpoint Protection: EDR/XDR solution deployed; real-time threat detection and response
- Device Management: MDM for corporate devices; compliance checks before resource access
- Encryption: Full-disk encryption enforced; BitLocker (Windows), FileVault (macOS), LUKS (Linux)
- Access Control: Local admin restricted; privileged access management (PAM) for elevation
- Monitoring: Security event logging; centralized log collection; behavioral analytics

Additional standards for cloud/container/endpoint hardening are maintained in internal runbooks and follow CIS/NIST baselines where applicable.


