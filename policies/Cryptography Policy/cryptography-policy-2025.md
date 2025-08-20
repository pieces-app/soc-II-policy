---
title: Cryptography Policy
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)
stakeholders:
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Mark Widman (Chief Technology Officer)
  - Sam Jones (Chief AI Officer)
  - Security/GRC (function)
  - Nathan Courtney (Head of CI/CD & DevOps)
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - SOC 2 CC6.1, CC6.6, CC7.1
    - ISO/IEC 27001 Annex A: A.8, A.10 (Cryptography)
    - NIST SP 800-57 (Key Management)
    - NIST SP 800-52 Rev. 2 (TLS)
    - NIST SP 800-131A Rev. 2 (Transitioning Cryptographic Algorithms)
    - FIPS 140-3 (Validated Modules)
  procedures:
    - Key Management Procedure
    - Certificate Management Procedure
    - Secrets Management Procedure
repo: https://github.com/pieces-app/soc-II-policy
---

# Cryptography Policy

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO), Mesh Intelligent Technologies, Inc.)

**Effective Date:** August 19, 2025

# Purpose

To ensure proper and effective use of cryptography to protect the confidentiality, authenticity, and integrity of information. This policy establishes requirements for cryptographic methods, key protection, and lifecycle management across all environments and systems.

# Scope

All information systems developed and/or controlled by Mesh Intelligent Technologies, Inc. that store or transmit Confidential or Restricted data, including services running in Google Cloud Platform (GCP), GitHub, Google Workspace, sanctioned SaaS, endpoints, and backups/snapshots.

# Policy

- Mesh Intelligent Technologies, Inc. evaluates risks in processing and storing data and implements cryptographic controls to mitigate those risks where appropriate.
- Strong cryptography is used with documented key management processes and procedures.
- All encryption aligns with industry standards and guidance including NIST SP 800-57, SP 800-52r2, SP 800-131A, and uses FIPS 140-3 validated modules where available for production cryptographic operations; where not available, provider best-practice configurations are used with documented risk acceptance.
- Customer or Confidential company data must utilize strong ciphers and secure configurations in accordance with vendor recommendations and industry best practices when stored or transferred over public or untrusted networks.
- No custom/homegrown cryptographic algorithms or protocols may be used.

## Baseline Requirements

- Data in Transit: TLS 1.3 required by default. TLS 1.2 is permitted only where required by a platform and with provider-approved strong cipher suites; configurations are reviewed at least annually.
- Data at Rest: AES-256 (GCM/XTS as applicable) via GCP default encryption or application-level encryption.
- Keys and Secrets: Managed via cloud KMS/HSM and Secret Manager; access restricted by least privilege; usage is logged and monitored.
- Internal Services: mTLS for service-to-service communications where technically feasible.
- Certificates: Public certificates issued by trusted CAs; validity periods meet CA/B Forum limits; automated renewal where feasible.
- Hashing: SHA-256 or stronger; MD5 and SHA-1 are prohibited.
- SSH: ed25519 or RSA 3072+ for new keys; legacy RSA 2048 allowed only until rotation.

TLS 1.2 fallback: Allowed only where a platform requires it. We inherit strong cipher suite baselines from Google Cloud and GitHub and verify periodically; weak/deprecated ciphers are disabled.

## Key Management

Access to keys and secrets is controlled in accordance with the Access Control Policy (https://app.vanta.com/c/pieces.app/policies/access-control-policy-bsi) and least privilege. Minimum requirements:

| Domain | Key Type | Algorithm | Key Length | Max Expiration |
| :---- | :---- | :---- | :---- | :---- |
| Web Certificate | RSA or ECC with SHA2+ signature | RSA or ECC with SHA2+ signature | RSA 2048+ or ECC P-256/384 | Up to 1 year |
| Web Cipher (TLS) | Asymmetric Encryption | Ciphers achieving grade A or better on SSL Labs | Varies | N/A |
| Confidential Data at Rest | Symmetric Encryption | AES (GCM/XTS) | 256 bit | 1 year (DEK rotation target) |
| Passwords | One-way Hash (provider-managed) | Provider-managed (e.g., 1Password, Descope) | Industry-standard; no custom hashing | N/A |
| Endpoint Storage (SSD/HDD) | Symmetric Encryption | AES | 128 or 256 bit | N/A |

Additional lifecycle requirements:
- Key Generation: Use approved libraries and FIPS 140-3 validated modules where feasible.
- Storage: Keys stored in KMS/HSM; secrets stored in Secret Manager. Keys and secrets are never hardcoded in source code.
- Rotation: DEKs rotated at least annually or upon compromise; KEKs/CMKs rotated at least annually; TLS certs auto-renewed; immediate rotation upon suspected exposure.
- Backup Keys: Encrypted and access-restricted; recovery procedures tested at least annually.
- Destruction: Cryptographic erasure performed when keys are retired; destruction is logged.
- Separation of Duties: Key administration and application operations responsibilities are segregated where feasible.

## Certificate Management

- Inventory: The authoritative inventory for production-facing certificates is the cloud provider’s certificate management (e.g., Google Cloud managed certificates and load balancers). For any non-managed/third-party certificates, an entry is maintained in GitHub (Security Register) within the `pieces-app` and `open-runtime` organizations with issuer, owner, and expiration.
- Renewal: Certificates are issued and renewed automatically via ACME/cloud-managed mechanisms where feasible. Any manual renewals are tracked via GitHub issues with owners and due dates within the `pieces-app` and `open-runtime` organizations.
- Revocation: Immediate revocation and reissuance upon key compromise or mis-issuance; incident response procedures invoked.

## Secrets Management

- Storage: Secrets are stored in Google Cloud Secret Manager or GitHub Secrets Manager; access is granted to service identities with least privilege.
- Transmission: Secrets are only transmitted over encrypted channels.
- Scanning: Automated secret scanning is enabled in repositories; exposures trigger incident response and immediate rotation.
- Password Manager: Password management and secure sharing of API keys and other sensitive information is performed via 1Password Business with SSO/MFA; we rely on provider encryption and hashing and do not manage password hashing directly.
- Service Accounts: Service accounts are administered using the Google Cloud CLI (gcloud). Workload Identity/OIDC is preferred over long-lived keys. If key material must be generated, it is stored in Secret Manager or 1Password, tightly access-controlled, and rotated promptly; long-lived keys are avoided.

## Identity & Token Management (Descope)

- Authentication: End-user authentication is handled by Descope with MFA enabled for sensitive operations; OAuth 2.0/OIDC flows use standards-based libraries.
- Token Security: JWTs are signed using RS256 or ES256; token lifetimes are minimized; refresh tokens are stored securely and can be revoked.
- Key Rotation: Descope signing keys are rotated per provider guidance or upon compromise indicators; JWKS endpoints are cached with reasonable TTL and verified on use.
- Session Management: Session identifiers are random, unguessable, and transmitted only over TLS; secure flags set for cookies where applicable.
 - Token Lifetimes: Default access token TTL ≤ 60 minutes; refresh token TTL ≤ 30 days. Administrative console sessions use shorter TTLs where feasible. Immediate revocation is enforced upon role change, separation, or suspected compromise.

## Platform & Vendor Controls

- Google Cloud Platform (GCP):
  - Encryption at rest is enabled by default; for sensitive workloads we use Customer-Managed Encryption Keys (CMEK) via Cloud KMS when technically feasible.
  - Service-to-service communications are restricted via VPC and Identity-Aware controls; mTLS is used where feasible.
  - Logs (Cloud Audit, Access Transparency where applicable) are retained ≥ 365 days in accordance with policy.
  - CMEK coverage targets: Cloud SQL, Cloud Storage (GCS), BigQuery, Pub/Sub, and other services supporting CMEK; documented where not technically supported with compensating controls.
- GitHub Enterprise Security:
  - GitHub Advanced Security (secret scanning, Dependabot, code scanning) is enabled for production repositories.
  - Branch protection rules enforce code review and status checks; repository secrets use OIDC/workload identity rather than long-lived credentials where feasible.
  - Public visibility is prohibited for repositories containing Confidential data or secrets.
- Sentry:
  - Application telemetry is transmitted over TLS; PII scrubbing and secure tunnel features are enabled where available.
  - Access to Sentry is restricted via SSO/MFA; retention aligns with Legal & Security Policies.
- Segment & Mixpanel:
  - Event data is transmitted via TLS and scoped to minimal fields; secrets are never embedded in event payloads.
  - Abuse detection and anomaly monitoring leverage these platforms; retention aligns with Legal & Security Policies.
- OpenVPN:
  - Configured via Google Cloud; access to sensitive systems requires VPN with SSO/MFA; encryption and configuration follow Google and provider best practices.

## Strong Authentication (MFA/2FA) for Internal SaaS

- Enforcement: All internal SaaS used for development and operations (e.g., Google Workspace/GCP, GitHub Enterprise, Sentry, Descope consoles, Segment, Mixpanel, Paddle, HubSpot) must enforce SSO with multi-factor authentication (MFA).
- Factors: Security keys (WebAuthn/FIDO2) are preferred; TOTP (RFC 6238) allowed as fallback; SMS is disallowed except as a break-glass method with time-bound approval.
- Scope: MFA is mandatory for privileged roles (e.g., cloud admins, repo admins, CI/CD maintainers) and recommended for all personnel.
- Review: Semiannual reviews verify MFA enforcement policies across providers and removal of non-compliant accounts; evidence is retained.
 - Network Access: Access to sensitive systems requires VPN (OpenVPN configured through Google Cloud) with SSO/MFA enforcement, following Google best practices.

## Software Supply Chain Security & Code Signing

- Target Level: We target SLSA Level 3 for release artifacts where reasonably feasible.
- Attestations: Build systems generate artifact attestations (e.g., GitHub artifact attestations, Sigstore/cosign) including provenance (builder identity, sources, dependencies, timestamps) and are verified prior to release.
- Code Signing: Release binaries for macOS, Linux, and Windows are signed using HSM-backed, non-exportable keys in a hardware-secured key vault. RFC 3161-compliant timestamping is applied.
- SBOM: Software Bill of Materials is generated for releases, stored with artifacts, and used for dependency transparency and vulnerability management.

## Algorithm and Configuration Standards

- We inherit cryptographic configuration baselines from our providers (e.g., Google Cloud, GitHub) and do not use custom algorithms or protocols.
- Deprecated or weak algorithms and ciphers are prohibited (e.g., MD5, SHA-1, RC4, 3DES, export ciphers, anonymous key exchange). TLS 1.3 is preferred; TLS 1.2 may be used only with provider-approved strong suites.
- SSH keys must use modern, strong algorithms (e.g., ed25519 preferred; RSA 3072+ acceptable); obsolete key exchange and MAC algorithms are disabled.

## Logging and Monitoring

- Key usage, certificate issuance/renewal, and secret access are logged; logs are retained ≥ 365 days.
- Configuration baselines and deviations are monitored via cloud security tooling; alerts are triaged by Security/Cloud Infrastructure.
- GitHub Advanced Security, Sentry, and cloud logs provide additional evidence for cryptographic control operation and alerting.
- Google Vault is used to retain and discover Google Workspace records to support investigations of access matters and policy violations, in accordance with legal and retention requirements.
 - Where feasible, log buckets/buckets use retention lock (WORM) to prevent tampering within retention windows.

## Roles & Responsibilities

- Corporate Secretary & CPO (Mack Myers): Owns this policy; ensures annual review; approves exceptions.
- Head of Cloud Infrastructure (Hiro Tamada): Implements TLS/KMS/Secret Manager controls; manages certs and logging.
- Chief Technology Officer (Mark Widman): Oversees engineering adherence to cryptographic standards and SSDLC.
- Head of CI/CD & DevOps (Nathan Courtney): Operates code-signing and build provenance controls; enforces non-exportability of signing keys and CI/CD secret hygiene; ensures signed commits and artifact attestation where supported.
- Security/GRC (function): Coordinates audits, evidence collection, and policy rollouts; maintains exception registers and links to GitHub issues.
- Chief AI Officer (Sam Jones): Ensures model pipelines and AI systems use approved cryptographic controls and do not train on customer personal data.
- Legal Counsel: Advises on regulatory requirements; manages legal holds where applicable.

## Exceptions

Requests for exceptions must be submitted and approved by the CEO (Tsavo Knott). All exceptions are documented and tracked in GitHub (Security Exception issues) within the `pieces-app` and `open-runtime` organizations and must include scope, rationale, compensating controls, owner, and expiration.

Portable or removable media: At present, the use of portable or removable media for customer or company Confidential/Restricted data is disallowed. Any exception to move, copy, or store such data on portable/removable media requires prior written approval from the CEO and must use approved full-disk encryption (e.g., AES-256 via device-native encryption such as FileVault or BitLocker). The exception must be recorded in GitHub within the `pieces-app` or `open-runtime` organization with time-bound approval and a revocation plan.

## Violations & Enforcement

Report suspected violations to security@pieces.app, the Corporate Secretary, or the CPO. Violations may result in suspension of privileges and/or disciplinary action up to and including termination.

## Assurance & Evidence (Audit Readiness)

We maintain the following evidence:
- TLS configuration scans (e.g., SSL Labs) and remediation records.
- Certificate inventory with ownership and expiration; renewal logs.
- KMS/Secret Manager key policies, rotation logs, and access audit logs (≥ 365 days).
- Secret scanning reports and rotation evidence for any exposures.
- Annual crypto configuration baseline review and approvals.
- Incident response records for any crypto-related events (revocations, rotations).
- Descope configuration exports (algorithms, key rotation), and token lifetime settings.
- GitHub Advanced Security reports (secret scanning, Dependabot) and remediation tracking.
- Sentry configuration (PII scrubbing) and access logs.
- Semiannual KMS key access reviews and attestation records; semiannual repository secret audits.
- MFA enforcement screenshots/config exports across SaaS providers; SSO policy records and semiannual review attestations.
- Code signing evidence: HSM configuration, signing logs (macOS/Linux/Windows), and provenance/attestation records in CI/CD.

## TSC Mapping

- CC6.1: Logical access and protection of cryptographic materials (KMS/Secret Manager, least privilege).
- CC6.6: Data protection via encryption at rest and in transit; rotation and decommissioning.
- CC7.1: Change/configuration management for cryptographic settings; monitoring and alerting.

## References

- NIST SP 800-57 (Key Management)
- NIST SP 800-52 Rev. 2 (TLS)
- NIST SP 800-131A Rev. 2 (Algorithm transitions)
- FIPS 140-3 (Validated modules)
- Access Control Policy: https://app.vanta.com/c/pieces.app/policies/access-control-policy-bsi
- Data Management Policy (2025)

## Change Log

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 08-Mar-2023 | First Version | Mark Widman | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |

---