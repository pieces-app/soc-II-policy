---
title: Secure Development Policy
owner:
  - Mark Widman (Chief Technology Officer)
stakeholders:
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
  - Sam Jones (Chief AI Officer)
  - Security/GRC (function)
approver: Tsavo Knott (CEO)
version: 1.2.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC7.2, CC7.3, CC8.1, CC6.1–CC6.3
    - ISO/IEC 27001 Annex A: A.14 (System Acquisition, Development and Maintenance)
    - OWASP Top 10
  procedures:
    - Release Checklist
    - Threat Modeling Procedure
    - Vulnerability Management Procedure
  controls:
    - GitHub Enterprise Security (branch protections, required reviews, GHAS)
    - Google Cloud (workload identity federation for CI, Artifact Registry attestations)
repo: https://github.com/pieces-app/soc-II-policy
---

# **Secure Development Policy**

**Policy Owner:** Mark Widman (Chief Technology Officer)

**Effective Date:** August 19, 2025

# **Purpose** 

To ensure that information security is designed and implemented within the software development lifecycle (SDLC) for applications and information systems.

# **Scope**

All Mesh Intelligent Technologies, Inc. applications and information systems that are business critical and/or process, store, or transmit Confidential data. This policy applies to all internal and external engineers and developers of Mesh Intelligent Technologies, Inc. software and infrastructure.

# **Policy**

This policy describes the rules for the acquisition and development of software and systems that shall be applied to development within the Mesh Intelligent Technologies, Inc. organization.

## **System Change Control Procedures**

Changes to systems within the SDLC shall be controlled by the use of formal change control procedures. Change control procedures and requirements are described in the Operations Security Policy.

- Significant code changes must be reviewed and approved by an engineering manager before being merged into any production branch, in accordance with Trunk‑Based Development practices and our CODEOWNERS/required reviewers configuration.
- Change control procedures ensure that development, testing, and deployment of changes are not performed by a single individual without approval and oversight.

## **Software Version Control**

All Mesh Intelligent Technologies, Inc. software is version controlled and synced between contributors. Access to the central repository is restricted based on role. All code is written, tested, and committed prior to merge, and changes are submitted via pull requests to the origin repository.

## **Technical Review of Applications after Operating Platform Changes**

When operating platforms are changed, business‑critical applications shall be reviewed and tested to ensure that there is no adverse impact on organizational operations or security.

## **Restrictions on Changes to Software Packages**

Modifications to third‑party business application packages shall be discouraged, limited to necessary changes, and strictly controlled.

## **Secure System Engineering Principles**

Principles for engineering secure systems shall be established, documented, maintained, and applied to any information system implementation efforts. At a minimum, the following secure‑by‑design and privacy‑by‑design principles shall be applied in an effort to guard against common vulnerability classes, including those listed in the OWASP Top 10.

Secure‑by‑design principles:
1. Minimize attack surface area  
2. Establish secure defaults  
3. The principle of least privilege  
4. The principle of defense in depth  
5. Fail securely  
6. Do not implicitly trust services  
7. Separation of duties  
8. Avoid security by obscurity  
9. Keep security simple  
10. Fix security issues correctly  

Privacy‑by‑design principles:
1. Proactive not Reactive; Preventative not Remedial  
2. Privacy as the Default Setting  
3. Privacy Embedded into Design  
4. Full Functionality – Positive‑Sum, not Zero‑Sum  
5. End‑to‑End Security – Full Lifecycle Protection  
6. Visibility and Transparency – Keep it Open  
7. Respect for User Privacy – Keep it User‑Centric  

Software developers are expected to adhere to Mesh Intelligent Technologies, Inc. coding standards throughout the development cycle, including standards for quality, documentation, and security.

## **Secure Development Environment**

Mesh Intelligent Technologies, Inc. shall establish and appropriately protect environments for system development and integration efforts that cover the entire system development life cycle. The following environments shall be logically or physically segregated:

- Production  
- Test / Staging  
- Development

Production data must not be used in non‑production environments. Where realistic data is necessary, use synthetic or de‑identified data consistent with Legal & Security Policies (Customer‑Facing) and the Data Management Policy.

## **Outsourced Development**

Mesh Intelligent Technologies, Inc. shall supervise and monitor the activity of outsourced system development. Outsourced development shall adhere to all Mesh Intelligent Technologies, Inc. standards and policies. Access for contractors follows least privilege and is time‑bound.

## **System Security Testing**

Testing of security functionality shall be performed at defined periods during the development life cycle. No code shall be deployed to production systems without documented, successful test results and evidence of security remediation activities.

## **Application Vulnerability Management**

- Application code is scanned prior to deployment using SAST/SCA (e.g., GitHub Advanced Security), enforced org‑wide on production repositories.  
- Critical/high vulnerabilities are triaged promptly; patches that materially impact security should be deployed within 90 days of discovery (expedited for critical issues).  
- Dependencies are monitored continuously; SBOMs are generated for releases where applicable.

## **System Acceptance Testing**

Acceptance testing programs and related criteria shall be established for new information systems, upgrades, and new versions.

Prior to deploying code, a Release Checklist MUST be completed which includes a checklist of all Test Plans showing completion of all associated tests and remediation of identified issues.

## **Protection of Test Data**

Test data shall be selected carefully, protected, and controlled. Confidential customer data shall be protected in accordance with all contracts and commitments. Customer data shall not be used for testing purposes without the explicit permission of the data owner and the CTO (or delegate). Where feasible, de‑identify or synthesize test data.

## **Acquisition of Third‑Party Systems and Software**

The acquisition of third‑party systems and software shall be done in accordance with the requirements of the Third‑Party Management Policy.

## **Developer Training**

Software developers shall be provided with secure development training appropriate to their role at least annually. Training content addresses prevention of common attacks and vulnerabilities, including:

- Authorization bypass  
- Insecure session identifiers  
- Injection attacks  
- Cross‑site scripting (XSS)  
- Cross‑site request forgery (CSRF)  
- Vulnerable/outdated libraries and dependencies  

# **Platform and Pipeline Security (Implementation Details)**

## **Source Control and Reviews (GitHub Enterprise)**

- Protected branches require pull request reviews and passing status checks; dismiss stale approvals on new commits; use CODEOWNERS for critical repositories.  
- Require at least one non‑author reviewer (two for critical paths) for production repositories.  
- Enforce secret scanning and push protection organization‑wide; bypass only via documented exceptions.  
- Pin GitHub Actions by commit SHA; restrict repository/org secrets and prefer environment secrets with least privilege.  
- Use protected environments and deployment approvals for production.

## **CI/CD and Workload Identity**

- Prefer workload identity federation (OIDC) from GitHub to Google Cloud; avoid long‑lived service account keys.  
- If secrets are required, store in approved secret managers (GitHub Secrets with scoped access or Google Secret Manager); rotate promptly and audit usage.  
- Build provenance and artifact attestations are generated where supported; releases are signed per the Cryptography Policy.

## **Artifact Registry and Attestations (GCP/GAR)**

- Google Artifact Registry is the authoritative registry for container/images; attestations must be published with builds and verified prior to promotion.  
- Deployment gates verify Google Cloud Artifact Registry attestations before releasing to protected environments.  
- GCS buckets storing build artifacts and model/data assets must retain object checksums and enable integrity verification during pipeline steps.

## **Code Signing and Provenance (Supply Chain Security)**

- Release Binaries (macOS, Linux, Windows): Must be signed using non‑exportable keys in a hardware‑secured key vault/HSM. Apply RFC 3161‑compliant timestamping. Verification of signatures is required in distribution pipelines.  
- Windows: Code signing uses DigiCert Authenticode certificates; timestamping and signature verification are enforced in the release workflow.  
- Container/Artifact Signing: Container images and critical artifacts must be signed; provenance (builder, sources, dependencies, timestamps) must be generated (e.g., SLSA provenance) and verified prior to promotion/deployment.  
- Policy Enforcement: Deployment pipelines must verify signatures and attestations prior to release to protected environments. Unsigned or unverifiable artifacts are blocked.  
- Keys & Rotation: Follow the Cryptography Policy for key management and rotation; prefer keyless/OIDC‑backed signing where feasible, with auditable identity binding.  
- Evidence: Store signing logs and provenance/attestation records alongside releases; retain per retention policy.

## **SBOM Generation and Dependency Hygiene (Recommended)**

- SBOMs: Where feasible, generate a Software Bill of Materials (SBOM) for production releases (application and container) in CycloneDX format, using Syft (or equivalent) in CI. For native apps, generate from build output directories or installer artifacts (e.g., .dmg/.pkg/.msi). Store SBOMs with the release artifacts and make available to enterprise customers upon request under NDA.  
- SCA / Dependency Updates: Enable automated dependency update workflows (e.g., Dependabot security updates). Critical/high vulnerabilities are triaged and remediated within defined SLAs; exceptions require documented risk acceptance.  
- Third‑Party Licenses: Track license compliance via SBOM/SCA; remediation is required for non‑compliant licenses before release.

## **Threat Modeling and Design Reviews**

- Perform threat modeling (e.g., STRIDE) for new features, significant architectural changes, or new data flows involving Confidential data.  
- Document mitigations and track risks in the Risk Register as appropriate.

## **ML/AI Development Considerations**

- Data Usage: Customer personal data is not used for model training; use synthetic or approved non‑customer datasets consistent with Legal & Data policies.  
- Artifact Control: Track dataset lineage and model artifact integrity (checksums/signing where feasible); restrict access by least privilege.  
- Hugging Face Models/Datasets: Pin by exact revision (commit/hash) when referencing external models or datasets; mirror critical artifacts to GCS with checksum validation before use.  
- Evaluation Data: Where evaluation involves Confidential data, apply de‑identification and access controls; retain only as long as necessary per Data Management Policy.

# **Assurance & Evidence (Audit Readiness)**

We maintain the following evidence:

- Pull request review records with required reviewers and status checks.  
- Branch protection, CODEOWNERS, and GHAS configuration exports.  
- SAST/SCA findings and remediation tracking; release SBOMs where applicable.  
- Release Checklists with security test results and approvals.  
- CI/CD configuration (OIDC to GCP), secret scopes, and rotation evidence.  
- Code signing logs, signature verification results, and artifact provenance/attestations.  
- GAR attestation verification logs and deployment gate evidence; GCS checksum validation logs.  
- Environment protection rules and deployment approvals for production.  
- Training completion records for developers (onboarding and annual).  

# **Exceptions**

Requests for an exception to this policy must be submitted to the CTO for approval. Exceptions are time‑bound and must include scope, compensating controls, owner, and expiration.

# **Violations & Enforcement**

Any known violations of this policy should be reported to the CTO or Security/GRC. Violations may result in immediate withdrawal or suspension of system and network privileges and/or disciplinary action in accordance with company procedures up to and including termination of employment.

## **TSC Mapping (SOC 2)**

- CC7.2: Changes are developed, reviewed, tested, and approved prior to release.  
- CC7.3: Vulnerability identification and remediation (SAST/SCA, patch timelines).  
- CC8.1: Change management and deployment controls (reviews, approvals, environment protection).  
- CC6.1–CC6.3: Logical access to development and deployment systems.

## **References**

- Legal & Security Policies (Customer‑Facing): Privacy, Retention/Deletion, BCP/DR  
- Cryptography Policy: Code signing/provenance, TLS, secrets  
- Access Control Policy: Branch protections, SSO/MFA, least privilege  
- Data Management Policy: Classification, non‑production data handling  
- Third‑Party Management Policy: Vendor assessments and DPAs  
- Risk Management Policy: Risk Register links for significant changes

## **Change Log**

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 08-Mar-2023 | First Version | Mark Widman | Tsavo Knott (CEO) |
| 1.1.0 | 15-Aug-2023 | Updates to Secure System Engineering Principles | Georgia Donmoyer | Mack Myers |
| 1.2.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |


