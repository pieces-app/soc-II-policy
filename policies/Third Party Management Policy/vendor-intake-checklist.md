# Vendor Intake Checklist (Third-Party Management)

Complete for every new vendor or material scope change. Attach evidence/links where applicable.

1. Business Context
   - Requestor, system owner, stakeholders
   - Intended use case and criticality
   - Data categories involved (PII, customer data, credentials, secrets, code, logs)
   - Production access? (Yes/No). If yes, describe scope

2. Risk Tiering (proposed)
   - Inherent risk factors: data sensitivity, system criticality, prod access, transaction volume
   - Proposed tier: High / Medium / Low

3. Due Diligence Artifacts (attach/links)
   - SOC 2 Type II / ISO 27001 / SOC 3 (as applicable)
   - Pen test summary (<=12 months) and remediation approach
   - Security whitepaper or controls overview
   - Encryption (at rest/in transit) description; SSO/MFA support
   - IR/BCDR summaries; uptime/availability commitments
   - DPA and subprocessor list; data residency/regions
   - Breach notification commitments (<=72 hours)

4. Contract & Security Terms
   - Right-to-audit / right-to-review security reports
   - Data deletion/certification upon termination (<=30 days)
   - Termination assistance and export format

5. Access & Provisioning
   - Required permissions and roles; least-privilege justification
   - SSO/MFA required; API key scoping and rotation plan
   - Logging/monitoring integration requirements

6. AI/ML & LLM (if applicable)
   - Model/data usage: training on our data? default opt-out enforced?
   - Dataset provenance and licensing statements
   - Safety/privacy/bias evaluation evidence; jailbreak/content moderation controls
   - Subprocessor (GPU/accelerator) and regions disclosed

7. Compensating Controls (if gaps)
   - Scope limitation, tokenization, additional monitoring, network isolation, etc.

Approvals:
- Security/GRC: ____________________  Date: ______
- Corporate Secretary: _____________  Date: ______
- Head of Cloud Infra/Security: _____  Date: ______
- CTO (if strategic/high risk): ______  Date: ______

