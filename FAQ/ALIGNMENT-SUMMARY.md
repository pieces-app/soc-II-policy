# Document Alignment Summary
**Date:** January 2025  
**Last Updated:** January 2025 (v2 - Removed deprecated services, added new subprocessors)
**Purpose:** Ensure consistency between FAQ documents and legal agreements

## Key Alignments Made

### 1. Pricing Structure ✅
All documents now reflect consistent pricing:
- **Standard Enterprise Rate:** $22.99 USD/user/month (IMC pilot uses standard rate)
- **Early Adopter Rate:** $16.99 USD/user/month (available for select pilots)
- **Team Pricing:** $15-20/user/month (10-50 users)
- **Annual Discount:** 10% for annual prepayment
- **Billing:** Quarterly in advance via Paddle (Merchant of Record)
- **Payment Terms:** Net 30 days

### 2. Support SLAs ✅
Aligned across all documents with three tiers:

| Priority | Standard | Premium | Enterprise |
|----------|----------|---------|------------|
| P1 - Critical | 4 hours | 1 hour | 30 minutes |
| P2 - High | 8 hours | 4 hours | 2 hours |
| P3 - Medium | 24 hours | 12 hours | 8 hours |
| P4 - Low | 48 hours | 24 hours | 24 hours |

**Note:** IMC pilot includes Premium support

### 3. Subprocessor List ✅
Consistent list across FAQ and DPA:

**Infrastructure:**
- Google Cloud Platform (USA) - Primary infrastructure
- GitHub Enterprise (USA) - Code repository and CI/CD

**Operational Services:**
- Paddle (UK/US) - Payment processing (Merchant of Record)
- Descope (USA) - Authentication services
- Sentry (USA) - Crash analytics/Crashlytics (PII scrubbed)
- SendGrid (USA) - Email delivery
- Customer.io (USA) - Email communications
- HubSpot (USA) - CRM and support
- Segment (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- Mixpanel (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- Satismeter (USA) - In-app surveys (rare, optional)
- Hugging Face (USA) - On-device SLM/LLM model registry & download source
- Google Workspace (USA) - Email & productivity suite

**Communication Channels:**
- Slack (USA) - Customer/provider communication
- Discord (USA) - Customer/provider communication
- Google Chat (USA) - Customer/provider communication (via Google Workspace)
- Gmail (USA) - Customer support & communication (via Google Workspace)

### 4. Uptime SLAs ✅
- **Standard:** 99.5% monthly
- **Premium:** 99.9% monthly  
- **Enterprise:** 99.95% monthly
- **Service Credits:** 5% per 0.1% below target (max 50%)

### 5. Data Handling ✅
Consistent statements across all documents:
- **Primary Region:** Google Cloud Platform (us-east5 - Ohio, USA)
- **Regional Options:** Including Sydney/Australia for IMC
- **Backup Retention:** 35 days (rolling)
- **Data Export:** Available during term + 60 days post-termination
- **Deletion Timeline:** 30 days production, 35 days backups

### 6. Certifications ✅
- **SOC 2 Type II:** Current, renewal by September 2025
- **GDPR:** Fully compliant with DPO designated
- **CCPA/CPRA:** Compliant with Service Provider requirements
- **ISO 27001:** Target Q2 2026
- **HIPAA BAA:** Available on demand

### 7. Platform Support ✅
**Desktop Applications:**
- Windows 10 (1903+), Windows 11
- macOS 12.0+ (Monterey and later)
- Linux: Ubuntu 20.04+, Fedora 35+, Debian 11+

**IDE Integrations:**
- VS Code, JetBrains suite, Visual Studio, Sublime, Vim/Neovim

**Browser Extensions:**
- Chrome 90+, Edge 90+, Firefox 88+, Safari 14+

### 8. IMC-Specific Terms ✅
- 6-month pilot with flexible termination
- Sydney region data residency available
- Premium support included
- SSO/SCIM integration
- No minimum seats during pilot
- Price protection for 12 months post-pilot

## Documents Updated

1. ✅ `FAQ/common.md` - General vendor assessment FAQ
2. ✅ `FAQ/imc-procurement-response.md` - IMC-specific responses
3. ✅ `Agreements/Data-Processing-Agreement.md` - Subprocessor list (Appendix 3)

## Documents Verified for Consistency

1. ✅ `Agreements/Master-Service-Agreement.md`
2. ✅ `Agreements/SOW-IMC-Pilot.md`
3. ✅ `Contracts/Trial Letter.md`

## Key Points to Remember

1. **Paddle as Merchant of Record** - Handles all billing, tax calculation, and compliance
2. **No Training on Customer Data** - Only synthetic datasets used
3. **Local-First Architecture** - Data stays on device by default
4. **Flexible Deployment** - Cloud, on-premises, or hybrid options
5. **Enterprise Features** - SSO, SCIM, dedicated support, custom terms
6. **Analytics & Telemetry** - Segment/Mixpanel used for abuse detection and usage metrics (anonymized, opt-in - like cookie consent)
7. **Crash Analytics** - Sentry is specifically for crash analytics/Crashlytics, not general monitoring
8. **Communication** - Customer support via Slack/Discord/Google Chat/Gmail, not traditional ticketing systems

## Next Steps

- [ ] Review with legal team for final approval
- [ ] Share aligned documents with IMC
- [ ] Update public-facing documentation if needed
- [ ] Maintain version control for future updates

---

## Change Log

### Version 2 (January 2025)
- **Removed:** Datadog (monitoring), Auth0/Okta (identity), Zendesk (ticketing) - no longer used
- **Added:** Satismeter (in-app surveys), Hugging Face (model registry), Google Workspace
- **Clarified:** Segment/Mixpanel purpose (abuse detection telemetry, opt-in)
- **Clarified:** Sentry purpose (crash analytics/Crashlytics, not general monitoring)
- **Updated:** Communication channels to reflect actual usage (Slack/Discord/Google Chat/Gmail)
- **Updated:** DPA breach notification to 24 hours (from 72 hours)

### Version 3.1 (January 2025 - Critical Architecture Clarification)
- **Clarified:** >99% of data persists on-device, <1% cloud metadata only
- **Emphasized:** Cloud processing is pure I/O with zero storage
- **Confirmed:** Air-Gapped mode operates completely offline
- **Removed:** Confusing percentages about "cloud storage" vs "cloud processing"
- **Added:** Customer audit logging as only exception to zero-storage principle

### Version 3 (January 2025 - Post-Bitly Feedback)
- **Updated:** Data architecture to reflect 85/15 on-device/cloud split
- **Added:** LLM configuration options (blended, SSO-locked, BYOK, air-gapped)
- **Clarified:** Ephemeral cloud processing vs persistent storage
- **Added:** Hardware requirements for different modes
- **Updated:** All documents to avoid absolute statements about data location

### Version 1 (January 2025)
- Initial alignment of pricing, SLAs, subprocessors, and technical specifications

---

## Data Processing Architecture Alignment (v3)

### Data Architecture Reality
- **>99% data persists on-device:** ALL actual user data stays local
- **<1% cloud metadata:** Auth tokens, crash analytics, abstract metrics only
- **~15% ephemeral processing:** Pure I/O for LLM inference (zero storage)
- **Air-Gapped mode:** Can operate completely offline without internet

### Configuration Options
All documents now reflect these options:
1. **Blended Mode (Default):** Cloud LLM enhancement with ephemeral processing
2. **SSO-Locked:** Restrict to enterprise-approved cloud models
3. **BYOK:** Use customer's existing LLM licenses
4. **Air-Gapped:** 100% on-device with local SLMs

### Hardware Requirements (Aligned)
- **Blended Mode:** 8GB RAM min, 16GB recommended (M3 MacBook Pro sufficient)
- **Air-Gapped:** 16GB RAM min, 32GB recommended for 14B+ parameter models

### Key Principles (Consistent Across All Docs)
- **ALL data persists on-device** - cloud has minimal metadata only
- **Cloud processing is pure I/O** - input → compute → output → delete
- **Zero storage of processed data** - unless customer explicitly requests auditing
- **Air-Gapped mode** - product works completely offline
- **No training on customer data** - ever
- **Configuration flexibility** - org-wide or per-user settings

---

## Deeper Policy Alignment Checks (v2)

### 1. Breach Notification Timelines ✅
- **Customer Notification:** Aligned to **24 hours** in `LEGAL_POLICY` and all FAQs.
- **GDPR Notification:** Maintained at **72 hours** as required by law.

### 2. Data & Log Retention ✅
- **Backup Deletion:** Aligned to **35 days** in `DPA` and `ALIGNMENT-SUMMARY` (was incorrectly 90).
- **Log Retention:** Clarified in `Data Management Policy` that **365-day** retention is for internal/compliance audit logs, while customer-facing security logs are retained for **90 days** per `LEGAL_POLICY`.

### 3. Subprocessors & Services ✅
- **LEGAL_POLICY:** Updated with the full, correct list of subprocessors, removing deprecated services and adding new ones.

### 4. Support SLAs ✅
- **LEGAL_POLICY:** Updated P1/P2 response times to **1 hour/4 hours** respectively, matching the Premium/Enterprise tiers offered to customers like IMC.

*This summary ensures all customer-facing and legal documents tell the same consistent story about Pieces' capabilities, pricing, and commitments.*
