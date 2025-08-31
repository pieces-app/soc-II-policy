# Pieces Vendor Assessment FAQ
**Version:** 1.0.0  
**Last Updated:** January 2025  
**Purpose:** Central reference for vendor assessments, procurement reviews, and security due diligence  
**Audience:** Procurement teams, security assessors, legal teams, and prospective enterprise customers

---

## Table of Contents

1. [Underlying Code & Training Data](#1-underlying-code--training-data)
2. [Data Ownership](#2-data-ownership)
3. [Data Privacy & Security](#3-data-privacy--security)
4. [Learning Capabilities](#4-learning-capabilities)
5. [Terms & Conditions](#5-terms--conditions)
6. [Vendor Maturity & Certifications](#6-vendor-maturity--certifications)
7. [Licensing & Pricing](#7-licensing--pricing)
8. [Technical Architecture](#8-technical-architecture)
9. [Compliance & Regulatory](#9-compliance--regulatory)
10. [Support & SLAs](#10-support--slas)

---

## 1. Underlying Code & Training Data

### Q: What sources of code/data are used to train or fine-tune AI models?

**A: We use exclusively synthetic datasets for AI model training.**

- **No Customer Data in Training**: Customer personal data is never incorporated into model development processes
- **Synthetic Data Methodology**: Our models are trained and distilled from established foundation models using privacy-preserving techniques
- **Foundation Model Distillation**: We leverage pre-trained foundation models and create specialized models through distillation, not direct training on proprietary datasets
- **Privacy by Design**: This approach eliminates traditional privacy concerns associated with training data while maintaining model accuracy and effectiveness
- **No Open Source Code Training**: We do not scrape or train on open-source repositories or proprietary codebases

### Q: How do you ensure model quality without using real customer data?

**A:** 
- Synthetic data generation techniques that mimic real-world patterns without containing actual personal information
- Model performance monitoring with drift detection and degradation alerting systems
- Continuous evaluation against benchmarks and quality metrics
- Version control with detailed change logs and performance metrics for all model iterations

---

## 2. Data Ownership

### Q: Who owns the inputs we provide (e.g., proprietary code, client data)?

**A: You retain full ownership of all your inputs.**

- **Customer Ownership**: 100% customer ownership of all provided data, code, and inputs
- **No Rights Claimed**: Pieces claims no ownership rights to customer inputs
- **Contractual Guarantee**: Ownership explicitly preserved in our Master Service Agreement (MSA) and Data Processing Addendum (DPA)
- **Data Portability**: Full export capabilities available at any time through cloud/local APIs in industry-standard formats (JSON, CSV)

### Q: Does Pieces claim any rights to outputs (AI-suggested code, refactoring recommendations)?

**A: Outputs are fully customer-owned.**

- **No Rights to Outputs**: All AI-generated suggestions, code completions, and recommendations belong entirely to the customer
- **Work Product**: Treated as customer work product with no licensing back to Pieces
- **No Vendor Lock-in**: Outputs can be freely used, modified, and integrated without restrictions
- **IP Protection**: Customer intellectual property rights fully preserved

### Q: Can customer data be used for model improvement?

**A: Only with explicit opt-in consent.**

- **Default Setting**: Model improvement using customer data is disabled by default
- **Opt-In Control**: Individual users can enable telemetry through in-application settings
- **Enterprise Control**: Enterprise customers can contractually exclude all data from any model improvement
- **De-identification**: If opted-in, only de-identified or aggregated data is used
- **Transparency**: Clear documentation of what data might be used and how

---

## 3. Data Privacy & Security

### Q: Is Pieces local-first/offline, or does data flow to cloud servers?

**A: Pieces operates with a configurable hybrid architecture.**
**Default Blended Mode (~85% on-device, ~15% cloud processing):**
- ALL data storage and persistence happens on user devices
- Cloud provides ephemeral LLM inference (input/output operation only)
- Zero retention of processed data in cloud
- Results immediately stored locally on-device

**Configuration Options:**
- **Blended Mode:** Default with cloud LLM for enhanced AI (ephemeral I/O only)
- **SSO-Locked:** Restrict cloud LLMs to specific enterprise models
- **BYOK:** Use customer's existing GCP Gemini, OpenAI, or Claude Enterprise licenses (**Important:** ALL BYOK configurations still require our cloud proxy services for protocol translation, authentication, and policy enforcement - true air-gapped BYOK is not technically possible)
- **Air-Gapped:** 100% offline operation with local SLMs (no internet required)
- Configuration can be set org-wide or per-user

**Minimal Cloud Metadata (<1% - operational only):**
- Authentication tokens (session state)
- Crash analytics (PII scrubbed signatures)
- Abstract usage metrics (opt-in, anonymized)
- License validation keys
- Abuse detection signals

**Ephemeral Cloud Processing (Zero Storage):**
- Pure input/output computation for LLM inference
- No persistence of inputs or outputs
- Immediate deletion after processing
- Results sent to device for local storage

### Q: What are your policies on data transmission, encryption, and storage?

**A: Enterprise-grade encryption and security throughout.**

**Encryption Standards:**
- **In Transit**: TLS 1.3 (preferred) or TLS 1.2 with strong cipher suites
- **At Rest**: AES-256 encryption via Google Cloud Platform's default encryption
- **Key Management**: Google Cloud KMS with automated rotation
- **Enhanced Options**: Customer-Managed Encryption Keys (CMEK) available for enterprise

**Data Storage:**
- Primary region: Google Cloud Platform (us-east5 - Ohio, USA)
- Regional options available for regulatory compliance (including Sydney/Australia)
- Multi-zone redundancy with automatic failover
- 35-day encrypted backup retention (rolling)
- Data export available during term and 60 days post-termination

### Q: Are subprocessors used? If so, where are they located?

**A: Minimal subprocessor usage with strict controls.**

**Critical Infrastructure:**
- **Google Cloud Platform** (USA) - Infrastructure and core services
- **GitHub** (USA) - Code repository and development security

**Operational Services:**
- **Paddle.com** (UK/US) - Payment processing (Merchant of Record)
- **Descope.com** (USA) - Authentication services (SSO)
- **Sentry.io** (USA) - Crash analytics/Crashlytics (PII scrubbed)
- **SendGrid** (USA) - Email delivery
- **Customer.io** (USA) - Email communications
- **HubSpot** (USA) - CRM and support
- **Segment.com** (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- **Mixpanel.io** (USA) - Abuse detection telemetry & usage metrics (anonymized, opt-in)
- **Satismeter** (USA) - In-app surveys (rare, optional)
- **Hugging Face** (USA) - On-device SLM/LLM model registry & download source
- **Google Workspace** (USA) - Email & productivity suite

**Communication Channels:**
- **Slack** (USA) - Customer/provider communication
- **Discord** (USA) - Customer/provider communication
- **Google Chat** (USA) - Customer/provider communication (via Google Workspace)
- **Gmail** (USA) - Customer support & communication (via Google Workspace)

All subprocessors:
- Maintain SOC 2 Type II or equivalent certifications
- Bound by comprehensive Data Processing Addenda (DPAs)
- Subject to annual security assessments
- Listed in our DPA with update notifications

**Important Notes:**
- Analytics (Segment/Mixpanel) are opt-in, similar to cookie consent - users control whether to share telemetry
- Sentry is specifically for crash analytics (Crashlytics), not general application monitoring
- No customer code or data is processed by operational service providers

### Q: How does Pieces ensure GDPR compliance?

**A: Comprehensive GDPR compliance program.**

- **Legal Basis**: Processing under contract performance, legitimate interests, or consent
- **Data Subject Rights**: Full support for access, correction, deletion, portability requests
- **Response Times**: 30-45 day response time for data subject requests
- **DPO Designation**: privacy@pieces.app
- **Standard Contractual Clauses**: SCCs in place for international transfers
- **Privacy by Design**: Built into product architecture and development processes
- **Breach Notification**: **24-hour** notification to customers for confirmed incidents affecting their data; **72-hour** notification to supervisory authorities (GDPR) when required
- **Data Minimization**: Only collect and retain necessary data

---

## 4. Learning Capabilities

### Q: Does Pieces learn from customer data?

**A: Learning is disabled by default with opt-in controls.**

**Default Behavior:**
- No learning from customer data without explicit consent
- Synthetic data used for base model development
- Customer data remains isolated from training pipelines

**Opt-In Learning:**
- Users can explicitly enable contribution to model improvement
- Enterprise agreements can permanently disable all learning
- De-identification applied before any opted-in usage
- Clear audit trail of consent and usage

### Q: Can customers opt out of contributing to training?

**A: Yes, with multiple control levels.**

- **Individual Control**: User-level settings in application
- **Enterprise Control**: Contractual exclusion in enterprise agreements
- **Granular Options**: Selective opt-in/out for different data types
- **Immediate Effect**: Opt-out takes effect immediately
- **No Penalty**: Full functionality maintained with opt-out

### Q: How is federated learning or similar techniques handled?

**A: Privacy-preserving techniques when applicable.**

- On-device processing where possible
- Differential privacy techniques for aggregated insights
- No raw data leaves customer environment in federated scenarios
- Edge computing capabilities for sensitive workloads

---

## 5. Terms & Conditions

### Q: What agreements are available for review?

**A: Comprehensive legal framework available.**

**Standard Agreements:**
- Master Service Agreement (MSA)
- Data Processing Addendum (DPA) with SCCs
- Service Level Agreement (SLA)
- Acceptable Use Policy (AUP)
- Privacy Policy (publicly available)
- Terms of Service

**Enterprise Options:**
- Custom Enterprise License Agreement (ELA)
- Business Associate Agreement (BAA) - available on demand
- Security Addendum with enhanced commitments
- Custom DPA terms for specific requirements

### Q: How are agreements negotiated and updated?

**A:**
- Red-line friendly for enterprise customers
- Legal-to-legal negotiation supported
- Material changes communicated with appropriate notice
- Annual review cycles with customer input
- Amendments tracked and version controlled

---

## 6. Vendor Maturity & Certifications

### Q: What is your current funding status?

**A: Financially stable and growing.**

- **Company**: Mesh Intelligent Technologies, Inc. (DBA Pieces)
- **Founded**: 2020 (Delaware incorporation)
- **Funding Stage**: VC-backed with strategic investors
- **Revenue Model**: Subscription-based SaaS
- **Financial Health**: Positive unit economics with growing customer base
- **Headquarters**: Cincinnati, Ohio, USA

### Q: What certifications do you maintain?

**A: Industry-standard security certifications.**

**Current Certifications:**
- **SOC 2 Type II**: Currently certified, annual renewal in progress (completion: September 2025)
- **GDPR Compliance**: Fully implemented with documented procedures and DPO designated
- **CCPA/CPRA**: Compliant with privacy rights procedures and Service Provider requirements

**Roadmap (12-24 months):**
- **ISO 27001**: Target certification by Q2 2026
- **ISO 27017**: Cloud security extension (24-month target)
- **HIPAA**: BAA capability (available upon customer demand)
- **Zero Trust Architecture**: Implementation in progress

### Q: Do you have cyber insurance?

**A: Comprehensive coverage maintained.**

- **Coverage**: Enterprise cyber liability insurance
- **Limits**: Appropriate for company size and risk profile
- **Renewal**: Annual review and renewal (2025-2026 policy active)
- **Scope**: Data breach, business interruption, liability coverage
- **Evidence**: Certificate of Insurance available upon request

---

## 7. Licensing & Pricing

### Q: Do you offer enterprise licensing or per-seat?

**A: Flexible licensing options available.**

**Licensing Models:**
- **Per-Seat**: Standard model for teams up to 100 users
- **Enterprise Site License**: Available for larger deployments
- **Concurrent User**: Option for shift-based teams
- **Unlimited/Company-wide**: Custom pricing for organization-wide deployment

### Q: What is your cost model?

**A: Transparent, scalable pricing.**

**Pricing Structure:**
- **Free Tier**: Limited features for individual developers
- **Professional**: $10-15/user/month (billed annually)
- **Team (10-50 users)**: $15-20/user/month with volume discounts
- **Enterprise (50+ users)**: 
  - Standard Rate: $22.99/user/month
  - Early Adopter/Pilot: $16.99/user/month
  - Volume discounts available
  - Annual commitment discount: 15% for annual prepayment
  - Custom pricing based on specific requirements

**Trial/POC Options:**
- 30-day free trial for teams
- 6-month pilot programs for enterprise (with early adopter pricing)
- Success criteria-based evaluations
- Flexible termination rights during pilot

**Payment Processing:**
- **Merchant of Record**: Paddle.com handles billing, tax calculation, and compliance
- **Billing Cycles**: Quarterly in advance (standard), custom terms available
- **Payment Terms**: Net 30 days
- **Currency**: USD with local currency conversion via Paddle

---

## 8. Technical Architecture

### Q: What deployment options are available?

**A: Multiple deployment models with configurable processing modes.**

**Processing Modes (All Deployments):**
- **Blended (Default):** ~85% on-device, ~15% cloud LLM processing
- **SSO-Locked:** Cloud LLMs restricted to enterprise-approved models
- **BYOK:** Bring Your Own Key for existing LLM licenses
- **Air-Gapped:** 100% on-device with local SLMs

**Deployment Options:**

**Standard SaaS:**
- Multi-tenant on Google Cloud Platform
- Geographic data residency options (US, EU, Sydney/Australia)
- Ephemeral cloud processing, persistent local storage
- Native desktop applications:
  - Windows 10 (1903+), Windows 11
  - macOS 12.0+ (Monterey and later)
  - Linux: Ubuntu 20.04+, Fedora 35+, Debian 11+
- IDE integrations: VS Code, JetBrains suite, Visual Studio, Sublime, Vim/Neovim
- Browser extensions: Chrome 90+, Edge 90+, Firefox 88+, Safari 14+

**Self-Hosted/On-Premises:**
- Complete air-gapped operation available
- Private cloud deployment options
- 100% data sovereignty
- Local SLM models only (no cloud processing)
- Separate licensing terms apply

**Hardware Requirements:**
- **Blended Mode:** 8GB RAM on macOS minimum (16GB recommended), 16GB on Windows/Linux, (32GB recommended)
- **Air-Gapped:** 32GB RAM minimum (64GB recommended for larger models)
- **Storage:** 2GB for blended, 20GB+ for air-gapped with models

### Q: How is multi-tenancy isolation ensured?

**A: Comprehensive isolation controls.**

- **Logical Separation**: Row-level security with tenant validation
- **Encryption**: Tenant-specific encryption keys where feasible
- **Access Control**: RBAC scoped to individual tenants
- **Resource Quotas**: Per-tenant limits prevent noisy neighbor issues
- **Audit Isolation**: Separate audit logs per tenant
- **Network Segmentation**: VPC isolation for enterprise customers

---

## 9. Compliance & Regulatory

### Q: What compliance frameworks do you support?

**A: Broad compliance coverage.**

**Implemented:**
- GDPR (EU data protection)
- CCPA/CPRA (California privacy)
- SOC 2 Type II (security controls)
- NIST Cybersecurity Framework alignment

**Available on Request:**
- HIPAA (healthcare) - BAA available
- Industry-specific frameworks
- Regional privacy laws
- Custom compliance attestations

### Q: How do you support customer audits?

**A: Comprehensive audit support.**

- **Documentation**: Security policies and procedures available
- **Audit Rights**: Annual audit rights in enterprise agreements
- **Evidence**: SOC 2 reports shared under NDA
- **Questionnaires**: Support for security assessments
- **On-site Audits**: Available for enterprise customers
- **Continuous Monitoring**: Real-time security posture via Vanta

---

## 10. Support & SLAs

### Q: What support levels are available?

**A: Tiered support model.**

**Support Tiers:**

| Priority | Standard | Premium | Enterprise | Description |
|----------|----------|---------|------------|-------------|
| P1 - Critical | 4 hours | 1 hour | 30 minutes | Production down, no workaround |
| P2 - High | 8 hours | 4 hours | 2 hours | Major functionality impaired |
| P3 - Medium | 24 hours | 12 hours | 8 hours | Moderate impact with workaround |
| P4 - Low | 48 hours | 24 hours | 24 hours | Minor issues or questions |

**Support Hours:**
- **Standard:** Business hours (9 AM - 5 PM ET, Mon-Fri)
- **Premium:** Extended hours (7 AM - 9 PM ET, Mon-Fri)
- **Enterprise:** 24/7/365

**Enterprise Features:**
- Dedicated Customer Success Manager
- Quarterly Business Reviews
- Direct engineering escalation
- Custom SLAs negotiable
- 24/7 emergency hotline

### Q: What are your uptime commitments?

**A: Enterprise-grade availability.**

- **Target Uptime**: 
  - Standard: 99.5% monthly
  - Premium: 99.9% monthly
  - Enterprise: 99.95% monthly
- **Scheduled Maintenance**: Up to 4 hours/month with 72-hour advance notice
- **Service Credits**: Available for SLA breaches (5% per 0.1% below target, max 50%)
- **Real-time Status**: status.pieces.app
- **RTO**: 4 hours for critical incidents
- **RPO**: 24 hours maximum data loss

---

## Additional Resources

### Contact Information
- **General Support**: support@pieces.app
- **Security Team**: security@pieces.app
- **Privacy/DPO**: privacy@pieces.app
- **Legal**: legal@pieces.app
- **Sales/Enterprise**: enterprise@pieces.app
- **Emergency Hotline**: +1 (513) 572-3339 (critical incidents only)

### Documentation
- **Product Documentation**: https://docs.pieces.app
- **Security Portal**: Available to enterprise customers
- **API Documentation**: https://docs.pieces.app/api
- **Status Page**: https://status.pieces.app

### Evidence & Attestations
Available upon request under NDA:
- SOC 2 Type II Report
- Penetration test executive summary
- Security architecture diagrams
- Vendor security assessments
- Insurance certificates
- Financial viability documentation

---

## Appendix: Quick Reference for Procurement Teams

### Key Differentiators
✅ **>99% data persists on-device** - True data sovereignty  
✅ **Cloud is pure I/O** - Zero storage of processed data  
✅ **Air-Gapped mode** - Operates completely offline  
✅ **No training on customer data** - Synthetic data only  
✅ **Flexible LLM options** - Blended, SSO-locked, BYOK, or air-gapped  
✅ **Self-hosting available** - Complete data sovereignty option  
✅ **SOC 2 Type II certified** - Annual third-party validation  
✅ **Minimal subprocessors** - Simplified supply chain  
✅ **GDPR/CCPA compliant** - Privacy by design  
✅ **Enterprise-grade encryption** - AES-256, TLS 1.3  
✅ **Flexible licensing** - Per-seat to site-wide options  

### Red Flags We DON'T Have
❌ No sale of customer data  
❌ No training on customer code without explicit consent  
❌ No vendor lock-in (full data portability)  
❌ No offshore development without security controls  
❌ No unencrypted data transmission or storage  
❌ No sharing with third parties for their purposes  

### Negotiable Terms for Enterprise
- Custom data residency requirements
- Enhanced security controls (CMEK, dedicated infrastructure)
- Custom retention and deletion schedules
- Specific compliance certifications
- Modified liability and indemnification terms
- Custom SLAs and support levels
- Multi-year pricing agreements
- Proof of Concept success criteria

---

*This FAQ is maintained by the Pieces Security and Legal teams. For the most current information or specific questions not addressed here, please contact our team directly.*

**Document Version:** 1.0.0  
**Last Review:** January 2025  
**Next Review:** April 2025  
**Classification:** External/Public with NDA for certain sections
