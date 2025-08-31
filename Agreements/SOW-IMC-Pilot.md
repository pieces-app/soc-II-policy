<!-- 
STATEMENT OF WORK - IMC PILOT
This SOW is executed under the Master Service Agreement
Specific to IMC's pilot program requirements

Note: This template is ready for IMC but requires filling in:
- Specific dates
- Contact information
- SSO provider details
- Initial seat count
-->

# STATEMENT OF WORK #001
## IMC PILOT PROGRAM

**SOW Number:** 001-IMC-2025  
**SOW Effective Date:** _____________________  
**Project Name:** IMC Enterprise Pilot Program

This Statement of Work ("**SOW**") is entered into as of the date last signed below and is governed by the Master Service Agreement dated _____________________ between **Mesh Intelligent Technologies, Inc. (d/b/a pieces.app)** ("**Provider**") and **IMC Trading** ("**Customer**" or "**IMC**").

---

## 1. SCOPE OF SERVICES

### 1.1 Pilot Program Overview
Provider will deliver a comprehensive pilot program of the Pieces for Developers platform as **artificial memory for IMC's teams**, tailored to enhance context retention, knowledge transfer, and productivity across all IMC personnel including developers, analysts, researchers, and other knowledge workers within IMC's operational environment and workflows.

### 1.2 Services Included
- **Platform Access:** Full access to the complete Pieces ecosystem including native desktop applications, all available plugins/extensions, and cloud services
- **SSO Integration:** SAML 2.0/OIDC integration with IMC's identity provider
- **User Access Management:** SSO-based access control - users authenticate via SSO and access is managed through Provider's admin console
- **LLM Configuration Options:**
  - Blended Mode: ~85% on-device processing with cloud LLM enhancement (default)
  - SSO-Locked Cloud LLMs: Restrict to specific provider models
  - BYOK Option: Use IMC's existing GCP Gemini, OpenAI, or Claude Enterprise licenses (via our cloud proxy services)
  - Air-Gapped Mode: 100% on-device with local SLMs (reduced capabilities)
  - User or org-wide configuration available
- **Custom Configuration:** Tailored setup for IMC's development environment
- **Dedicated Support:** Premium-tier support with dedicated chat channels and emergency contact
- **Success Management:** Assigned Customer Success Manager
- **Onboarding:** Quick-start session and ongoing office hours support

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
- [ ] SSO integration with IMC's identity provider
- [ ] User access list configuration and SSO testing
- [ ] Security review and approval
- [ ] Environment configuration

### Phase 2: Initial Rollout & Onboarding (Weeks 2-3)
- [ ] Initial kickoff meeting (1 hour, drop-in format for installation help)
- [ ] Week 2: First walkthrough and check-in session
- [ ] Weeks 2-3: 3-4 optional office hours (45 min each) for onboarding support
- [ ] Quick-start guide: "Pieces as your artificial memory"
- [ ] MCP (Model Context Protocol) integration overview (if applicable)
- [ ] Dedicated Slack/Discord/Teams/Google Chat channel setup

### Phase 3: Full Pilot Deployment (Weeks 4-20)
- [ ] Weekly office hours (45 min, optional drop-in for quick questions)
- [ ] Bi-weekly feedback sessions (45 min, Weeks 4-8) - Provider benefit
- [ ] Monthly feedback sessions (45 min, Weeks 9-20) - Provider benefit
- [ ] Mid-pilot review (Week 12)
- [ ] Usage analytics and ongoing optimization
- [ ] Success criteria assessment

### Phase 4: Evaluation and Transition (Weeks 21-24)
- [ ] Pilot success evaluation
- [ ] ROI analysis and metrics review
- [ ] Production deployment planning (if proceeding)
- [ ] Knowledge transfer and documentation

---

## 3. COMMERCIAL TERMS

### 3.1 Pilot Pricing
- **Per-User Rate:** $22.99 USD per user per month (standard enterprise rate)
- **Initial Seats:** 30 users
- **Billing Frequency:** Quarterly in advance
- **Setup Fees:** Waived for pilot program
- **Professional Services:** Included at no additional charge

### 3.2 Payment Schedule
- **First Invoice:** Pro-rated from Start Date through end of calendar quarter
- **Subsequent Invoices:** Beginning of each calendar quarter
- **Payment Terms:** Net 30 days from invoice date
- **Payment Method:** Via Paddle (Merchant of Record)
- **Alternate Invoicing:** At Customer's option, Provider will invoice Customer directly (outside Paddle) on **Net 30** terms against a Customer PO, payable by ACH/wire in USD. Taxes will be calculated and remitted by Provider or passed-through as applicable.

### 3.3 Seat Adjustments
- **Increases:** Pro-rated for remainder of current quarter
- **Decreases:** Effective beginning of next quarter, minimum 15 seats
- **Minimum Requirement:** Pilot must maintain at least 15 seats to ensure meaningful evaluation

### 3.4 Post-Pilot Pricing
Upon successful pilot completion and transition to production:
- **Standard Enterprise Rate:** $22.99 USD per user per month
- **Volume Discounts:** Available based on seat count
- **Annual Commitment Discounts:** 10% for annual prepayment

---

## 4. SERVICE LEVEL AGREEMENT

### 4.1 Support Tier
**Premium Support** included during pilot:
- **Hours:** 7 AM - 9 PM ET, Monday-Friday
- **Channels:** Dedicated Slack/Discord/Teams/Google Chat, email, cell phone for emergencies
- **Response Times:**
  - P1 (Critical): 1 hour
  - P2 (High): 4 hours
  - P3 (Medium): 12 hours
  - P4 (Low): 24 hours

### 4.2 Availability
- **Target Uptime:** 99.7% monthly availability (Premium tier standard)
- **Maintenance Windows:** Scheduled with 72-hour notice
- **Service Credits:** Not applicable during pilot period (focus on collaborative issue resolution)

### 4.3 Escalation Path
1. Support Team: enterprise.pilots@pieces.app
2. Customer Success: tsavo@pieces.app or mack@pieces.app
3. Technical Escalation: hiro@pieces.app, mark@pieces.app, or brian.powell@pieces.app

### 4.4 Pilot SLA Alignment
Notwithstanding anything in the MSA or its Exhibits: (a) Target Availability during the Pilot is **99.7% monthly**; (b) **service credits do not apply** during the Pilot; (c) the **Measurement Period** for SLA purposes equals the Pilot Term; (d) **Support Hours and response times** are as stated in §4.1 of this SOW and control over any conflicting definitions; and (e) **SLA-based termination rights do not apply during the Pilot** - all other termination rights (convenience, cause unrelated to SLA) remain per MSA/SOW terms. The Parties expressly agree to these modifications under MSA §12.10.

### 4.5 Pilot Remedies for Service Issues
For any material availability or response-time deviation during the Pilot, Provider will: (i) deliver a **root cause analysis** and remediation plan; (ii) provide **additional support resources** as needed; and (iii) **extend the Pilot timeline** if necessary to meet Pilot objectives, in lieu of service credits.

---

## 5. IMC RESPONSIBILITIES

### 5.1 Technical Requirements
- Provide access to identity provider for SSO configuration
- Assign technical contact for integration activities
- Ensure user devices meet minimum system requirements
- Provide test accounts and environments as needed

### 5.2 Program Management
- Designate pilot program owner
- Coordinate user onboarding and training attendance
- Provide regular feedback and participate in check-ins
- Communicate issues and requirements timely

### 5.3 Success Criteria
*Success criteria to be collaboratively defined during pilot kickoff*

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
  - Custom integrations with IMC's existing technical infrastructure
- **Operational Excellence:**
  - Platform adoption and user satisfaction (broad vs. deep adoption models)
  - Security and compliance requirements met
  - Integration success with IMC's existing workflows
- **Power User Identification:**
  - Identification of users who find Pieces indispensable for their specific roles
  - Documentation of high-value use cases and workflow transformations
  - Assessment of "mission-critical" adoption patterns for key personnel

**Custom Success Criteria** *(to be defined with IMC):*
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
- Monthly progress reports
- Quarterly business reviews
- Best practices guidance
- Adoption and usage analytics

---

## 7. DATA PROCESSING

### 7.1 Data Handling
- Processing governed by the separate Data Processing Agreement
- IMC data remains within agreed geographic boundaries
- No processing of regulated data (PCI, PHI, etc.) unless explicitly authorized in writing
- Regular security attestations provided

### 7.2 Data Residency
- **Primary Processing:** United States (GCP us-east5 - Ohio)
- **Backup Locations:** GCP us-central1 (Iowa) - same country redundancy, no cross-region transfers outside the United States without prior written notice
- **Data Export:** Available throughout pilot and 60 days after in standard formats (Markdown/JSON as applicable)

### 7.3 Architecture Clarification (Authoritative for IMC Pilot)
This section harmonizes MSA, DPA, and SOW language regarding data processing architecture:

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

### 8.1 Pilot Term
- **Duration:** 6 months from Start Date
- **Extensions:** By mutual written agreement
- **Early Success:** May transition to production at any time

### 8.2 Termination Rights
- **For Convenience:** Either party with 45 days written notice (Notwithstanding MSA §11.2, the parties agree that this SOW §8.2 controls during the Pilot)
- **For Cause:** Per MSA terms
- **Refunds:** Pro-rated for unused pre-paid period

### 8.3 Post-Pilot Options
- **Production Transition:** Seamless move to full deployment
- **Extended Pilot:** Additional evaluation time if needed
- **Conclusion:** Orderly wind-down with data export

---

## 9. SUCCESS METRICS

### 9.1 Key Performance Indicators
*To be jointly defined during pilot kickoff based on IMC's specific objectives*

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
  - Custom workflow integrations specific to IMC's technical environment
  - ___% improvement in automated knowledge capture and retrieval

**Baseline Pilot Success Criteria** *(minimum for "successful pilot" determination):*
- **Adoption:** Either 60% broad adoption (18+ active users) OR 10+ power users who find Pieces indispensable
- **User Satisfaction:** NPS score > 40 or equivalent satisfaction metric
- **Productivity Impact:** Demonstrable improvement in context retention, knowledge transfer, or search efficiency
- **Technical Integration:** Successful SSO integration and platform stability
- **Security Compliance:** No security incidents or compliance violations during pilot

**Custom IMC Metrics** *(to be defined collaboratively):*
- _________________________________
- _________________________________
- _________________________________

### 9.2 Reporting
- Monthly usage reports
- Quarterly performance reviews
- Ad-hoc analytics as requested
- Final pilot assessment report

---

## 10. CONTACTS

### IMC Contacts
- **Program Owner:** _____________________
- **Technical Lead:** _____________________
- **Security Contact:** _____________________
- **Billing Contact:** _____________________

### Provider Contacts
- **Customer Success Managers:** 
  - Tsavo Knott: tsavo@pieces.app
  - Mack Myers: mack@pieces.app
- **Technical Account Managers:** 
  - Hiro Tamada: hiro@pieces.app
  - Mark Widman: mark@pieces.app
  - Brian Powell: brian.powell@pieces.app
- **Support:** enterprise.pilots@pieces.app
- **Escalation:** security@pieces.app

---

## 11. SPECIAL TERMS

### 11.1 Pilot-Specific Provisions
- No long-term commitment required
- Flexible termination rights
- Price protection for 12 months post-pilot
- Reference rights upon mutual agreement

### 11.2 Confidentiality
- Pilot participation may be kept confidential if requested
- No public references without written consent
- Case study development requires approval

---

## 12. ACCEPTANCE

This SOW is effective upon execution by authorized representatives of both parties.

**IMC TRADING**

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

### Initial Kickoff (Week 2 - 1 hour, drop-in)
- Installation support - join and leave when ready
- "Pieces as your artificial memory" - the intuitive approach
- 5-minute setup walkthrough
- Core concept: Save once, recall anywhere
- Live demo of typical developer workflow

### Onboarding Office Hours (Weeks 2-3)
- 3-4 sessions available (45 min each)
- Optional attendance - at customer convenience
- Installation troubleshooting
- Quick tips for getting started
- MCP (Model Context Protocol) overview if relevant
- Ensure everyone has fundamentals covered

### Weekly Office Hours (Weeks 4-20, 45 minutes)
- Optional drop-in format
- No agenda - bring your questions
- Share tips and discoveries
- Troubleshooting support
- Feature requests welcome

### Feedback Sessions (45 minutes - Provider Benefit)
- **Weeks 4-8:** Bi-weekly sessions
- **Weeks 9-20:** Monthly sessions
- Product feedback collection
- Usage patterns discussion
- Feature prioritization input
- Success stories and challenges

### Self-Service Resources
- Quick-start guide: "Pieces in 5 minutes"
- Short video walkthroughs (< 3 minutes each)
- Dedicated Slack/Discord/Teams/Google Chat channel
- In-app tooltips and guidance
- No formal training required - it's intuitive!
