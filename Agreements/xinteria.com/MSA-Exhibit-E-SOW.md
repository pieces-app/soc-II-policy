<!-- 
MSA EXHIBIT E SOW - XINTERIA TEAM DEPLOYMENT
This comprehensive SOW is executed under the Master Service Agreement
Specific to Xinteria's team deployment requirements

Note: This MSA Exhibit E, SOW is ready for Xinteria but requires filling in:
- Specific dates
- Contact information
- SSO provider details (if applicable)
- Initial seat count (approximately 24)
-->

# MSA EXHIBIT E STATEMENT OF WORK #001
## XINTERIA TEAM DEPLOYMENT

**SOW Number:** 001-XINTERIA-2025  
**SOW Effective Date:** _____________________  
**Project Name:** Xinteria Team Deployment  
**Program Type:** 12-Month Annual Plan with Early Adopter Discount

This Statement of Work ("**SOW**") is entered into as of the date last signed below and is governed by the Master Service Agreement dated _____________________ between **Mesh Intelligent Technologies, Inc. (d/b/a pieces.app)** ("**Provider**") and **_______________________________________ (Xinteria)** ("**Customer**" or "**Xinteria**").

**Early Adopter Program:** This SOW includes a special 25% early adopter discount for the initial 12-month term, with flexible termination rights and full pro-rated refunds if Customer terminates early.

---

## 1. SCOPE OF SERVICES

### 1.1 Enterprise Deployment Overview
Provider will deliver a comprehensive enterprise deployment of the Pieces for Developers platform as **artificial memory for Xinteria's team**, tailored to enhance context retention, knowledge transfer, and productivity across all Xinteria personnel including developers, engineers, product managers, and other knowledge workers within Xinteria's operational environment and workflows.

### 1.2 Services Included
- **Platform Access:** Full access to the complete Pieces ecosystem including native desktop applications, all available plugins/extensions, and cloud services
- **SSO Integration (Optional):** SAML 2.0/OIDC integration with Xinteria's identity provider
- **User Access Management:** SSO-based access control (if enabled) - users authenticate via SSO and access is managed through Provider's admin console
- **LLM Configuration Options:**
  - Blended Mode: ~85% on-device processing with cloud LLM enhancement (default)
  - SSO-Locked Cloud LLMs: Restrict to specific provider models (if SSO enabled)
  - BYOK Option: Use Customer's existing GCP Gemini, OpenAI, or Claude Enterprise licenses (via our cloud proxy services)
  - Air-Gapped Mode: 100% on-device with local SLMs (reduced capabilities)
  - User or org-wide configuration available
- **Custom Configuration:** Tailored setup for Xinteria's development environment
- **Dedicated Support:** Support tier per selected level (Standard/Premium/Enterprise)
- **Success Management:** Assigned Customer Success Manager
- **Onboarding:** Quick-start session and ongoing support

### 1.3 Deployment Specifications
- **Platforms:** Windows 10/11, macOS 12+, Linux (Ubuntu 20.04+)
- **Integration Points:** 
  - All available IDE plugins/extensions across the ecosystem
  - All available browser plugins/extensions
  - Native desktop applications (PiecesOS ecosystem)
  - Model Context Protocol (MCP) integrations
  - API access for custom integrations and new plugin development across departments
- **Security Requirements:** 
  - Enterprise-grade encryption and security controls
  - Zero-knowledge architecture options available
  - Secure cloud proxy services for LLM operations

---

## 2. DELIVERABLES AND MILESTONES

### Phase 1: Setup and Integration (Week 1)
- [ ] SSO integration with Xinteria's identity provider (if applicable)
- [ ] User access list configuration and SSO testing (if applicable)
- [ ] Security review and approval (if applicable)
- [ ] Environment configuration

### Phase 2: Initial Rollout & Onboarding (Weeks 2-3)
- [ ] Initial kickoff meeting (1 hour, drop-in format for installation help)
- [ ] Week 2: First walkthrough and check-in session
- [ ] Weeks 2-3: 3-4 optional office hours (45 min each) for onboarding support
- [ ] Quick-start guide: "Pieces as your artificial memory"
- [ ] MCP (Model Context Protocol) integration overview (if applicable)
- [ ] Dedicated Slack/Discord/Teams/Google Chat channel setup

### Phase 3: Ongoing Deployment (Month 2+)
- [ ] Ongoing support per selected tier
- [ ] Regular check-ins and feedback sessions
- [ ] Quarterly business reviews
- [ ] Usage analytics and ongoing optimization
- [ ] Success criteria assessment
- [ ] Platform updates and feature releases

---

## 3. COMMERCIAL TERMS

### 3.1 Pricing
- **Standard Per-User Rate:** $22.99 USD per user per month
- **Early Adopter Discount:** 25% off for 12-month annual commitment
- **Discounted Rate:** $17.24 USD per user per month ($206.88 per user per year)
- **Initial Seats:** _____ users (approximately 24 based on team size)
- **Billing Frequency:** Annual in advance
- **Setup Fees:** Waived
- **Professional Services:** Basic onboarding included at no additional charge

### 3.2 Payment Schedule
- **First Invoice:** Annual subscription from Start Date
- **Renewal Invoices:** Annually on anniversary of Start Date
- **Payment Terms:** Net 30 days from invoice date
- **Payment Method:** Via Paddle (Merchant of Record)
- **Alternate Invoicing:** At Customer's option, Provider will invoice Customer directly (outside Paddle) on **Net 30** terms against a Customer PO, payable by ACH/wire in USD. Taxes will be calculated and remitted by Provider or passed-through as applicable.

### 3.3 Seat Adjustments
- **Increases:** Pro-rated for remainder of current annual term
- **Decreases:** Effective at next annual renewal

### 3.4 Discounts and Incentives
- **Early Adopter Discount:** 25% off standard rate for this initial 12-month term
- **Price Protection:** Standard rate ($22.99/user/month) locked for duration of initial term
- **Volume Discounts:** Available for 50+ seats (applied on top of early adopter discount)
- **Multi-Year Commitments:** Additional discounts available upon request for subsequent renewals

---

## 4. SERVICE LEVEL AGREEMENT

### 4.1 Support Tier
**Support Tier:** _____ (Standard/Premium/Enterprise - select based on Customer needs)

**Standard Support:**
- **Hours:** 9 AM - 5 PM ET, Monday-Friday
- **Channels:** Email and support chat
- **Response Times:**
  - P1 (Critical): 4 hours
  - P2 (High): 8 hours
  - P3 (Medium): 24 hours
  - P4 (Low): 48 hours

**Premium Support** (if selected):
- **Hours:** 7 AM - 9 PM ET, Monday-Friday
- **Channels:** Dedicated Slack/Discord/Teams/Google Chat, email
- **Response Times:**
  - P1 (Critical): 1 hour
  - P2 (High): 4 hours
  - P3 (Medium): 12 hours
  - P4 (Low): 24 hours

**Enterprise Support** (if selected):
- **Hours:** 24/7/365
- **Channels:** Dedicated Slack/Discord/Teams/Google Chat, email, cell phone for emergencies
- **Response Times:**
  - P1 (Critical): 30 minutes
  - P2 (High): 2 hours
  - P3 (Medium): 8 hours
  - P4 (Low): 24 hours

### 4.2 Availability
- **Target Uptime:** Per MSA Exhibit B based on selected tier
  - Standard: 99.5% monthly
  - Premium: 99.7% monthly
  - Enterprise: 99.9% monthly
- **Maintenance Windows:** Scheduled with 72-hour notice, capped at 4 hours per month
- **Service Credits:** Per MSA Exhibit B (up to 100% monthly)

### 4.3 Escalation Path
1. Support Team: support@pieces.app
2. Customer Success: tsavo@pieces.app or mack@pieces.app
3. Technical Escalation: mark@pieces.app or brian.powell@pieces.app

---

## 5. CUSTOMER RESPONSIBILITIES

### 5.1 Technical Requirements
- Provide access to identity provider for SSO configuration (if SSO requested)
- Assign technical contact for integration activities (if applicable)
- Ensure user devices meet minimum system requirements
- Provide necessary network access and firewall configurations

### 5.2 User Management
- Designate account administrator
- Manage user provisioning and seat assignments
- Coordinate initial team onboarding
- Communicate platform updates and best practices to team

### 5.3 Success Framework
*Success metrics and goals to be tracked during deployment*

**Suggested Evaluation Framework:**
- **Artificial Memory Impact:**
  - Enhanced context retention and recall across all users
  - Improved knowledge transfer between team members and departments
  - Reduced time spent on repetitive research/searches
- **User Experience (All Personnel):**
  - Faster onboarding for new team members (developers, analysts, researchers)
  - More detailed and contextual daily standups and team communications
  - Improved work quality through better context awareness and information retention
- **Team Dynamics:**
  - Enhanced collaboration through shared knowledge base
  - Better visibility into individual and team productivity patterns
  - Improved documentation and knowledge preservation
- **Technical Integration & Augmentation:**
  - Deep integration with internal tooling and agent pipelines
  - Enhanced reporting capabilities and data insights
  - API-driven workflow automation and process enhancement
  - Custom integrations with Xinteria's existing technical infrastructure
- **Operational Excellence:**
  - Platform adoption and user satisfaction (broad vs. deep adoption models)
  - Security and compliance requirements met
  - Integration success with Xinteria's existing workflows
- **Platform Adoption:**
  - User engagement and satisfaction
  - Feature utilization across the team
  - Integration with daily workflows

**Xinteria-Specific Goals** *(to be defined):*
- _________________________________
- _________________________________
- _________________________________

---

## 6. PROVIDER RESPONSIBILITIES

### 6.1 Delivery Commitments
- Ensure platform availability per SLA
- Provide agreed support levels
- Deliver training and documentation
- Regular platform updates and improvements
- Security and compliance maintenance

### 6.2 Success Management
- Assigned Customer Success Manager
- Regular progress reports
- Quarterly business reviews (for Premium/Enterprise tiers)
- Best practices guidance
- Adoption and usage analytics

---

## 7. DATA PROCESSING

### 7.1 Data Handling
- Processing governed by the separate Data Processing Agreement
- Xinteria data remains within agreed geographic boundaries
- No processing of regulated data (PCI, PHI, etc.) unless explicitly authorized in writing
- Regular security attestations provided

### 7.2 Data Residency
- **Primary Processing:** United States (GCP us-east5 - Ohio)
- **Backup Locations:** GCP us-central1 (Iowa) - same country redundancy, no cross-region transfers outside the United States without prior written notice
- **Data Export:** Available throughout term and 60 days after termination in standard formats (Markdown/JSON as applicable), at no additional charge

### 7.3 Architecture Clarification
This section provides clarity on data processing architecture:

**On-Device Data (>99% of persistent data):**
- ALL snippets, files, links, code, OS-level/application-level context, etc.
- ALL AI conversation history and context
- ALL workflow data and personal productivity information
- Provider has **no remote access** to on-device data by design

**Cloud Processing Options:**
- **Blended Mode (Default):** ~85% on-device processing, ~15% ephemeral cloud LLM processing
- **BYOK:** Customer's existing LLM licenses **require Provider's cloud proxy** for protocol translation - **not air-gapped**
- **Air-Gapped Mode:** 100% on-device with local SLMs **only** - no cloud connectivity, no BYOK

**Cloud Metadata (<1% operational only):**
- Authentication state, license validation, crash analytics (PII scrubbed), opt-in telemetry

**Data Retention:**
- **Ephemeral cloud processing:** Zero retention by default unless Customer explicitly requests audit logging
- **Cloud metadata:** Per Legal Policy retention schedules
- **On-device data:** Customer-controlled, Provider cannot access remotely

---

## 8. TERM AND TERMINATION

### 8.1 Service Term
- **Initial Term:** 12 months from Start Date
- **Renewal:** Automatically renews for successive 12-month periods unless terminated per MSA terms
- **Extensions:** By mutual written agreement

### 8.2 Termination Rights
- **For Convenience:** Customer may terminate this SOW on 90 days' written notice for any reason
- **For Cause:** Per MSA Section 11.3 (30 days cure period)
- **For SLA Breach:** Per MSA Section 1.4 (after 3 consecutive months of critical SLA failures)
- **Pro-Rated Refunds:** Customer will receive a full pro-rated refund of any prepaid fees for the unused portion of the term if Customer terminates for convenience, cause, or SLA breach. Refunds will be calculated based on the number of days remaining in the annual term.

### 8.3 Data Transition
- **Data Export:** Available throughout term and 60 days post-termination
- **Data Deletion:** Per MSA Section 5.7 (30-60 days for production, 35 days for backups)
- **Orderly Wind-Down:** Provider will assist with smooth transition

---

## 9. SUCCESS METRICS

### 9.1 Key Performance Indicators
*To be jointly defined during deployment based on Xinteria's specific objectives*

**Suggested Baseline Metrics:**
- **Adoption Models:** 
  - Broad adoption: ___% active users by month 3, OR
  - Deep adoption: ___ power users who find Pieces indispensable for their roles
- **User Satisfaction:** NPS score > 40 (or equivalent satisfaction metric)
- **Artificial Memory Value:**
  - ___% improvement in context recall and knowledge transfer
  - ___% reduction in time spent searching for information/documentation
  - ___% increase in knowledge artifact reuse (code, research, insights)
- **Team Collaboration:**
  - Increased detail & context in daily standups: ___% improvement
  - Faster knowledge/context transfer to teammates: ___x faster
  - Enhanced onboarding speed for new team members: ___% faster
- **Productivity Insights:**
  - Deeper insights into time spent and efficiency across all individual contributors
  - ___% improvement in identifying productivity patterns across roles
  - Enhanced visibility into knowledge gaps and learning opportunities for all users
- **Technical Integration Opportunities:**
  - Integration with internal agent pipelines and automation tools
  - Enhanced reporting and analytics capabilities via API
  - Custom workflow integrations specific to Xinteria's technical environment
  - ___% improvement in automated knowledge capture and retrieval

**Baseline Success Criteria** *(suggested targets):*
- **Adoption:** Either 60% broad adoption (15+ active users) OR 8+ power users who find Pieces indispensable
- **User Satisfaction:** NPS score > 40 or equivalent satisfaction metric
- **Productivity Impact:** Demonstrable improvement in context retention, knowledge transfer, or search efficiency
- **Technical Integration:** Successful platform integration and stability (SSO if applicable)
- **Security Compliance:** No security incidents or compliance violations

**Custom Xinteria Metrics** *(to be defined collaboratively):*
- _________________________________
- _________________________________
- _________________________________

### 9.2 Reporting
- Monthly usage reports
- Quarterly performance reviews
- Ad-hoc analytics as requested
- Periodic assessment reports as needed

---

## 10. CONTACTS

### Xinteria Contacts
- **Program Owner:** _____________________
- **Technical Lead:** _____________________
- **Security Contact:** _____________________
- **Billing Contact:** _____________________

### Provider Contacts
- **Customer Success Managers:** 
  - Tsavo Knott: tsavo@pieces.app
  - Mack Myers: mack@pieces.app
- **Technical Account Managers:** 
  - Mark Widman: mark@pieces.app
  - Brian Powell: brian.powell@pieces.app
- **Support:** support@pieces.app
- **Escalation:** security@pieces.app

---

## 11. SPECIAL TERMS

### 11.1 Deployment Provisions
- **Initial Term:** 12-month commitment with automatic annual renewal
- **Early Adopter Program:** 25% discount for initial term only
- **Easy Exit:** 90-day notice termination for convenience with full pro-rated refund
- **Price Protection:** Rate locked for initial 12-month term
- **Renewal Pricing:** Standard rates apply after initial term unless otherwise negotiated
- **Reference Rights:** Upon mutual agreement

### 11.2 Confidentiality
- Deployment participation may be kept confidential if requested
- No public references without written consent
- Case study development requires approval

---

## 12. ACCEPTANCE

This SOW is effective upon execution by authorized representatives of both parties.

**_______________________________________ (XINTERIA)**

By: _________________________________  
Name: _______________________________  
Title: ______________________________  
Date: _______________________________

**MESH INTELLIGENT TECHNOLOGIES, INC.**

By: _________________________________  
Name: _______________________________  
Title: ______________________________  
Date: _______________________________

---

## APPENDIX A: TECHNICAL SPECIFICATIONS

### Supported Platforms
- **Windows:** 10 (1903+), 11
- **macOS:** 12.0+ (Monterey and later)
- **Linux:** Ubuntu 20.04+

### Minimum Hardware Requirements
**Blended Mode (Default):**
- **RAM:** 8GB minimum, 16GB recommended
- **Processor:** Intel i5/AMD Ryzen 5 or Apple M1 or better
- **Storage:** 2GB available space
- **Note:** ~2GB RAM used for nano-models during processing

**Air-Gapped Mode (100% Local):**
- **RAM:** 16GB minimum, 32GB recommended
- **Processor:** Apple M3/Intel i7/AMD Ryzen 7 or better recommended
- **Storage:** 20GB+ for local models
- **Note:** 6-7GB RAM for 14B parameter models, scales with model size and context

---

## APPENDIX B: ONBOARDING & SUPPORT STRUCTURE

### Initial Kickoff (Week 1-2 - 1 hour, optional)
- Installation support
- "Pieces as your artificial memory" - the intuitive approach
- Quick setup walkthrough
- Core concept: Save once, recall anywhere
- Live demo of typical developer workflow

### Onboarding Support (Weeks 2-4)
- Optional office hours sessions (45 min each)
- Available at customer convenience
- Installation troubleshooting
- Quick tips for getting started
- MCP (Model Context Protocol) overview if relevant
- Ensure team has fundamentals covered

### Ongoing Support
- Regular support per selected tier (Standard/Premium/Enterprise)
- Dedicated communication channels based on tier
- Email: support@pieces.app
- Troubleshooting and feature guidance
- Feature requests welcome

### Check-ins and Reviews
- Monthly check-ins (for Premium/Enterprise tiers)
- Quarterly business reviews
- Usage analytics and optimization recommendations
- Success stories and feedback collection

### Self-Service Resources
- Quick-start guide: "Pieces in 5 minutes"
- Short video walkthroughs (< 3 minutes each)
- Dedicated support channel based on tier
- In-app tooltips and guidance
- Comprehensive documentation at docs.pieces.app
