# IMC Procurement Review - Pieces Response Document

**Prepared for:** IMC Pacific Pty Ltd  
**Date:** January 2025  
**POC Scope:** Sydney office, 30 users  
**Pieces Contacts:** 
- Tsavo Knott (CEO) - tsavo@pieces.app
- Mack Myers (CPO) - mack@pieces.app  
- Smit (Team) - smit@pieces.app

---

## Executive Summary

Pieces is an AI-powered developer productivity platform that operates with a local-first architecture, ensuring data sovereignty and privacy by default. We maintain SOC 2 Type II certification and have designed our platform specifically to address enterprise security and compliance requirements.

---

## Detailed Responses to IMC Questions

### 1. Underlying Code / Training Data

#### Q: Are any sources of code/data used to train or fine-tune AI models (open-source, proprietary, third-party licensed)?

**Answer:** 
- **No customer or open-source code is used for training**. We exclusively use synthetic datasets for AI model training.
- Our models are distilled from established foundation models using privacy-preserving techniques
- We do not scrape, collect, or train on:
  - Open-source repositories (GitHub, GitLab, etc.)
  - Customer proprietary code
  - Third-party licensed code
- This approach eliminates IP contamination risks and ensures clean model provenance

---

### 2. Ownership

#### Q: Who owns the inputs we provide (e.g., proprietary code, client data)?

**Answer:**
- **IMC retains 100% ownership** of all inputs including:
  - Proprietary code
  - Client data
  - Documentation
  - Any other materials provided to Pieces
- This is explicitly stated in our Master Service Agreement (MSA) and Data Processing Addendum (DPA)
- No license grant to Pieces beyond what's necessary to provide the service

#### Q: Does Pieces claim any rights to outputs (AI-suggested code, refactoring recommendations), or are they fully customer-owned?

**Answer:**
- **All outputs are fully IMC-owned**, including:
  - AI-generated code suggestions
  - Refactoring recommendations  
  - Analysis results
  - Any derivative works
- Pieces claims no rights, license, or ownership to any outputs
- Outputs can be used without restriction or attribution

#### Q: Can customer data be used for model improvement?

**Answer:**
- **No, not without explicit opt-in consent**
- Default setting: Customer data is never used for model improvement
- For IMC's enterprise deployment:
  - We can contractually guarantee no data usage for model training
  - Complete exclusion from any improvement programs
  - Audit trail of this exclusion maintained

---

### 3. Leakage / Data Privacy

#### Q: Is Pieces local-first/offline, or does data flow to cloud servers?

**Answer:**
- **Pieces operates with configurable hybrid architecture**

**Default Blended Mode (~85% on-device, ~15% cloud processing):**
- ALL data persistence on developer machines
- Cloud provides ephemeral LLM inference only
- Zero retention of cloud-processed data
- Results immediately stored locally

**Configuration Options for IMC:**
- **Blended Mode:** Cloud LLM for enhanced AI (ephemeral I/O only)
- **SSO-Locked:** Restrict to IMC-approved cloud models
- **BYOK:** Use IMC's existing GCP/OpenAI/Claude licenses (**Important:** BYOK still requires our cloud proxy services for secure protocol translation and policy enforcement)
- **Air-Gapped:** 100% offline operation (no internet required)
- Can be configured org-wide or per-user/team

**Minimal Cloud Metadata (<1% - operational only):**
- Authentication state (SSO tokens)
- Crash analytics metadata (PII scrubbed)
- Abstract usage metrics (opt-in, anonymized)
- License validation
- Abuse detection signals

**Ephemeral Cloud Processing (Zero Storage):**
- Pure I/O operation for LLM inference
- Input → Compute → Output → Delete
- No persistence of prompts or responses
- Unless IMC explicitly requests audit logging

#### Q: Policies on data transmission, encryption, and storage?

**Answer:**

**Encryption:**
- Transit: TLS 1.3 (all communications)
- At Rest: AES-256 encryption
- Key Management: Google Cloud KMS with automated rotation
- Option for Customer-Managed Encryption Keys (CMEK)

**Data Transmission:**
- All transmissions over encrypted channels
- No data leaves device in local-only mode
- Cloud sync only with explicit user action

**Storage:**
- Local: Device-encrypted storage
- Cloud: Google Cloud Platform (us-east5 - Ohio)
- Regional options available (including Sydney/Australia)
- 35-day backup retention with encryption

#### Q: Are subprocessors used? If so, where are they located?

**Answer:**

**Infrastructure (Core):**
- Google Cloud Platform (USA, with Sydney region available)
- GitHub Enterprise (USA) - code/development only, no customer data

**Operational Services (No customer code/data processed):**
- **Paddle** (UK/USA) - Payment processing as Merchant of Record
- **Descope** (USA) - Authentication services only
- **Sentry** (USA) - Crash analytics/Crashlytics with PII scrubbing
- **SendGrid** (USA) - Email delivery
- **HubSpot** (USA) - CRM and support
- **Segment** (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- **Mixpanel** (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- **Satismeter** (USA) - In-app surveys (rare, optional)
- **Hugging Face** (USA) - On-device SLM/LLM model registry & download source
- **Google Workspace** (USA) - Email & productivity suite

**Communication Channels:**
- **Slack** (USA) - Customer/provider communication
- **Discord** (USA) - Customer/provider communication
- **Google Chat** (USA) - Customer/provider communication (via Google Workspace)
- **Gmail** (USA) - Customer support & communication (via Google Workspace)

**For IMC:** We can provide a complete subprocessor list in the DPA with:
- Notification of changes
- Right to object to new subprocessors
- All subprocessors maintain SOC 2 or equivalent

#### Q: How does Pieces ensure GDPR compliance?

**Answer:**
- **Full GDPR compliance implemented** including:
  - Documented legal bases for processing
  - Data Subject Rights procedures (access, deletion, portability)
  - 30-day response time for requests
  - Data Protection Officer designated (privacy@pieces.app)
  - Standard Contractual Clauses (SCCs) for transfers
  - Privacy by Design architecture
  - 24-hour breach notification commitment to customers
  - 72-hour breach notification commitment to supervisory authorities (GDPR)
  - Data minimization and purpose limitation
  - Annual privacy assessments

---

### 4. Learning Capabilities

#### Q: Does Pieces learn from customer data (fine-tuning, embeddings, federated learning)?

**Answer:**
- **No learning from IMC data without explicit consent**
- Our approach:
  - Base models use only synthetic data
  - No fine-tuning on customer data
  - Embeddings stay local to user/organization
  - No federated learning across customers
- IMC-specific configuration:
  - Complete isolation from other customers
  - No cross-pollination of data or models
  - Contractual guarantee of no learning

#### Q: If yes, can customers opt out of contributing to training?

**Answer:**
- **Yes, multiple opt-out mechanisms:**
  - System-wide opt-out via enterprise agreement
  - User-level controls in application settings
  - Contractual exclusion with audit rights
  - Immediate effect upon configuration
  - No functionality loss when opted out

---

### 5. Terms & Conditions

#### Q: Please share the latest MSA and DPA for review against IMC standards.

**Answer:**
- We will provide for IMC's legal review:
  - Master Service Agreement (MSA) - Enterprise version
  - Data Processing Addendum (DPA) with SCCs
  - Service Level Agreement (SLA)
  - Security Addendum (if required)
  - Business Associate Agreement (BAA) template (if needed)
  
- Our agreements are:
  - Red-line friendly
  - Negotiable for enterprise customers
  - Include audit rights
  - Include security and privacy commitments
  - Governed by agreed jurisdiction

---

### 6. Vendor Maturity

#### Q: Current funding status (VC-backed, revenue stage)?

**Answer:**
- **Company:** Mesh Intelligent Technologies, Inc. (DBA Pieces)
- **Founded:** 2020 (Delaware, USA)
- **Funding:** VC-backed with strategic investors
- **Stage:** Revenue-generating with positive unit economics
- **Customers:** Growing base including enterprises
- **Stability:** 
  - 5+ years in operation
  - Consistent product development
  - Long-term committed team

#### Q: Certifications (SOC 2, ISO 27001)?

**Answer:**

**Current Certifications:**
- ✅ **SOC 2 Type II** - Active (renewal in progress for 2025)
- ✅ **GDPR Compliant** - Fully implemented
- ✅ **CCPA/CPRA Compliant** - With documented procedures

**12-Month Roadmap:**
- 🎯 ISO 27001 - Target: Q2 2026
- 🎯 Penetration Testing - Annual third-party assessments
- 🎯 Zero Trust Architecture - Implementation ongoing

**Available for IMC:**
- SOC 2 Type II report (under NDA)
- Security assessment documentation
- Compliance attestation letters
- Penetration test executive summaries
- Premium Support included during pilot (1-hour P1 response)

---

### 7. Licensing

#### Q: Do you offer enterprise licensing, or is it per-seat?

**Answer:**

**Available Licensing Models:**
1. **Per-Seat** (Standard)
   - Ideal for POC/trial phase
   - Monthly or annual billing
   - Flexible scaling

2. **Enterprise Site License** (For IMC consideration)
   - Organization-wide access
   - Predictable costs
   - Volume discounts
   - Custom terms available

3. **Hybrid Options**
   - Concurrent user licensing
   - Department/team bundles
   - Consumption-based models

#### Q: Please provide cost model.

**Answer:**

**POC/Trial (30 users - Sydney):**
- 30-day free trial available
- Extended POC terms negotiable
- Success criteria-based evaluation

**Pilot/POC Pricing (IMC Sydney - 30 users):**
- **Standard Enterprise Rate:** $22.99 USD/user/month
- **Billing:** Quarterly in advance via Paddle (Merchant of Record)
- **Setup Fees:** Waived for pilot program
- **Professional Services:** Included at no charge
- **Pilot Duration:** 6 months with flexible termination

**Production Pricing (Post-Pilot):**
- **Standard Enterprise Rate:** $22.99 USD/user/month
- **Volume Discounts:** Available based on seat count
- **Annual Commitment Discount:** 10% for annual prepayment
- **Price Protection:** 12 months post-pilot continuation

**For IMC Specifically:**
- POC: Flexible 30-60 day evaluation available
- No minimum seat requirements during pilot
- Quarterly billing cycles
- Payment via Paddle with local currency support
- Net 30 payment terms

---

## Proposed Next Steps for IMC

### 1. Immediate Actions
- [ ] Share MSA/DPA for IMC legal review
- [ ] Provide SOC 2 report under NDA
- [ ] Schedule technical deep-dive session

### 2. POC Planning (Sydney Office - 30 Users)
- [ ] Define success criteria and KPIs
- [ ] Set 6-month pilot period with flexible exit
- [ ] Configure LLM mode (blended, SSO-locked, BYOK, or air-gapped)
- [ ] Configure data residency (Sydney region available)
- [ ] Set up SSO integration with IMC identity provider
- [ ] Establish dedicated Slack/Teams support channel
- [ ] Verify hardware requirements:
  - Blended Mode: M3 MacBook Pro with 16GB RAM sufficient
  - Air-Gapped: 16GB+ RAM recommended for local SLMs
- [ ] User mix recommendation:
  - Developers (primary)
  - Product managers
  - Support engineers
  - Other technical roles

### 3. Commercial Discussion
- [ ] Finalize POC terms (no cost)
- [ ] Discuss production pricing model
- [ ] Review enterprise licensing options
- [ ] Align on contract terms

### 4. Technical Configuration
- [ ] Local-only vs hybrid deployment
- [ ] Integration requirements
- [ ] Security controls implementation
- [ ] Compliance validation

---

## Key Differentiators for IMC

### Why Pieces is Right for IMC

1. **Data Sovereignty & Control**
   - >99% of data persists exclusively on IMC devices
   - Cloud processing is pure I/O computation (zero storage)
   - Air-Gapped mode operates completely offline
   - BYOK option for existing LLM licenses
   - No training on IMC's proprietary code

2. **Enterprise Security**
   - SOC 2 Type II certified
   - Enterprise-grade encryption
   - Minimal subprocessor footprint
   - SSO-locked cloud models available

3. **Flexible Deployment**
   - Start with Sydney POC
   - Per-user or org-wide LLM configuration
   - Scale to global deployment
   - Air-gapped option for sensitive teams

4. **Transparent Architecture**
   - Clear data processing boundaries
   - No hidden retention or training
   - Ephemeral vs persistent data clearly defined
   - Audit-friendly documentation

5. **Commercial & Technical Flexibility**
   - POC-friendly terms
   - Works with existing hardware (M3/16GB RAM)
   - Supports diverse user roles (devs, PMs, support)
   - Australian entity billing capable

---

## Contact Information

**For Technical Questions:**
- Tsavo Knott (CEO): tsavo@pieces.app
- Engineering Team: engineering@pieces.app

**For Security/Compliance:**
- Security Team: security@pieces.app
- Privacy/DPO: privacy@pieces.app

**For Commercial/Legal:**
- Mack Myers (CPO): mack@pieces.app
- Legal Team: legal@pieces.app

**Emergency/Critical Issues:**
- Hotline: +1 (513) 572-3339

---

## Appendix: Quick Facts for IMC Procurement

✅ **NO training on customer code**  
✅ **100% customer data ownership**  
✅ **>99% data persists on-device only**  
✅ **Cloud processing is pure I/O (zero storage)**  
✅ **Air-Gapped mode works completely offline**  
✅ **BYOK option for existing LLM licenses**  
✅ **SOC 2 Type II certified**  
✅ **GDPR/CCPA compliant**  
✅ **Sydney region available**  
✅ **30-day free POC**  
✅ **Works with M3 MacBook Pro / 16GB RAM**  
✅ **Enterprise licensing available**  
✅ **5+ years in business**  
✅ **Red-line friendly agreements**

---

*This document prepared specifically for IMC Pacific Pty Ltd procurement review. For updates or clarifications, please contact the Pieces team directly.*
