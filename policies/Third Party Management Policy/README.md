# Third-Party Management Policy – Folder Guide

This folder contains the policy and supporting operational artifacts for Third-Party/Vendor Risk Management.

- third-party-management-policy-v1.1.md: The authoritative policy. Defines roles (Corporate Secretary, Security/GRC, airCFO, Head of Cloud Infra/Security, CTO), vendor tiering, due diligence, onboarding/offboarding, monitoring, AI/ML vendor requirements, exceptions, and references.
- vendor-intake-checklist.md: One-page intake form used at vendor request time. Captures business context, proposed risk tier, required diligence artifacts (SOC2/ISO, pen test, DPA, etc.), access scope, AI/LLM specifics, and approvals. Submit this with links to evidence.
- vendor-inventory.csv: Live register of all vendors and review status. Used for audits and internal tracking. Keep this up to date as the source of truth.

## vendor-inventory.csv – Columns

- Vendor Name: Legal or common vendor name.
- Owner: Internal business/system owner (e.g., Mack Myers).
- Service Description: Short description of the service provided.
- Data Categories: Types of data involved (e.g., PII, customer data, logs, code).
- Prod Access (Y/N): Whether the vendor can access production systems/data.
- Risk Tier: High / Medium / Low (see policy criteria).
- Last Assessment: Date of last risk/due-diligence review.
- Next Review Due: Target date based on tier cadence or material change.
- Assurance (SOC2/ISO): Latest external assurance (e.g., SOC 2 Type II, ISO 27001).
- DPA (Y/N): Whether a Data Processing Agreement is executed.
- Subprocessors Link: URL to vendor’s subprocessor list or document location.
- Regions: Data residency/processing regions used by the vendor.
- SSO/MFA (Y/N): Whether the vendor supports and has SSO/MFA enabled for us.
- Encryption (At Rest/In Transit): Summary (e.g., AES-256 / TLS 1.2+).
- Notes: Any pertinent notes (e.g., compensating controls, exceptions).

## Maintenance & Ownership

- Corporate Secretary (Mack Myers) and Security/GRC maintain the register and evidence links; airCFO co-approves HR/finance vendors.
- Head of Cloud Infra/Security (Hiro Tamada) maintains AI/LLM evaluation evidence with oversight by the CTO (Mark Widman).
- Update inventory upon onboarding, material scope/change, and offboarding. Align review cadence with the policy’s tiering.

## TODO: Populate vendor-inventory.csv

Add or update rows for the following services. For each, fill Owner, Data Categories, Prod Access (Y/N), Risk Tier, Assurance (SOC2/ISO), DPA (Y/N), Subprocessors Link, Regions, SSO/MFA, Encryption, and Notes.

- GitHub (source control; GitHub Enterprise Security)
- Sentry (error monitoring)
- Mixpanel (product analytics)
- Google Cloud (GCP; infrastructure)
- Google Workspace / Google Drive (productivity, storage)
- OpenAI (LLM APIs)
- Anthropic (LLM APIs)
- Cloudsmith (artifact repository)
- Segment (customer/event pipelines)
- Status monitoring (Statusmeter/Statuspage – confirm exact provider)
- Vanta (compliance automation)
- Carta (equity/data room reference in HR policy)
- Shortwave (email client – if in use)
- Descope / IdP (if applicable; confirm actual provider)
- Hugging Face
- DigiCert
- Azure and Microsoft 365
- Others

Developer tools & media (add if used)
- Cursor (AI code editor)
- JetBrains IDEs (IntelliJ IDEA, WebStorm, PyCharm, etc.)
- VS Code (extensions, marketplace)
- ScreenStudio (screen recording)
- Loom (async video)
- Slack / Discord (team comms)


Discovery tips
- Review Vanta Integrations for connected services and add any missing vendors.
- Check finance/HR (airCFO) purchase records and IT asset lists for additional SaaS.
- Confirm with Cloud/Infra (Hiro Tamada) and CTO (Mark Widman) for AI/ML tools and infra dependencies.
