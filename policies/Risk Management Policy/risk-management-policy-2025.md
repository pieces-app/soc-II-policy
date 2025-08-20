---
id: POL-0006
title: Risk Management Policy
owner:
  - Mack Myers (Co-Founder & Corporate Secretary, Mesh Intelligent Technologies, Inc.)
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards:
    - ISO/IEC 27005 (Information Security Risk Management)
    - NIST SP 800-30 (Guide for Conducting Risk Assessments)
    - NIST SP 800-37 (Risk Management Framework)
  procedures: []
  controls:
    - SOC 2 CC3.1, CC3.2, CC3.3, CC4.x, CC5.2
repo: https://github.com/pieces-app/soc-II-policy
---

# **Risk Management Policy**

**Policy Owner:** Mack Myers (Co-Founder & Corporate Secretary), Security/GRC (function)

**Effective Date:** August 19, 2025 

**Policy Type:** Risk Management Policy  
**Policy Number:** 6

| Company Name: | Mesh Intelligent Technologies, Inc. |  |
| :---- | :---- | :---- |
| Policy Owners: | Mack Myers (Co-Founder & Corporate Secretary), Security/GRC (function) | Phone: (513) 572-3339 |
| Effective Date: | August 19, 2025 | Date Revised: August 19, 2025 |
| Last Review: | August 19, 2025 | Next Review: August 19, 2026 |

## Purpose

To define actions to address Mesh Intelligent Technologies, Inc. information security risks and opportunities, and to define a plan for the achievement of information security and privacy objectives in alignment with SOC 2 and industry frameworks.

## Scope

- All Mesh Intelligent Technologies, Inc. IT systems that process, store or transmit confidential, private, or business-critical data.  
- Risks that could affect the medium to long-term goals of Mesh Intelligent Technologies, Inc. as well as risks in day-to-day service delivery.  
- Risk management systems and processes are targeted to achieve maximum benefit without imposing undue burden that would affect core service delivery.  
- Materiality is considered in developing systems and processes to manage risk.  
- This Policy applies to all employees and to external parties (consultants, contractors, business partners, vendors, suppliers, outsourced service providers, and other third parties) with access to Mesh Intelligent Technologies, Inc. networks and system resources.  
- Platform Context: We build native software across macOS, Linux, and Windows with optional cloud components powered via Google Cloud Platform (GCP) and selected AI providers (e.g., Anthropic, OpenAI). This hybrid footprint is in scope for risk identification, assessment, and treatment.

## Risk Management Statement

Inadequate risk management exposes Mesh Intelligent Technologies, Inc. to risks including compromise of company or customer systems, services and information, cyber-attacks, contractual or legal issues. Risk management plays an integral role in governance and management at strategic and operational levels to ensure business objectives are achieved.

## Risk Management Strategy

Mesh Intelligent Technologies, Inc. maintains processes to identify risks that hinder strategic and operational objectives and ensures the means to identify, analyze, control and monitor risks using this policy based on best practices (ISO 27005, NIST SP 800-30, NIST SP 800-37). The strategy and policy are reviewed at least annually. Internal functions ensure:  
- The policy is applied across applicable areas  
- The policy and its application are regularly reviewed  
- Non-compliance is reported to appropriate officers and authorities

## Practical Application of Risk Management

Mesh Intelligent Technologies, Inc. uses a standard format to identify, classify, evaluate, and treat risks, based on ISO 27005, NIST SP 800-30, and NIST SP 800-37.  
- Risks are assessed and ranked by impact and likelihood.  
- A formal enterprise Risk Assessment is performed at least annually and upon material change (e.g., major feature launches, architecture changes, new vendors with access to production or customer data).  
- Network penetration tests are performed at least annually, and results feed the Risk Register and Treatment Plan.  
- Vulnerability management, bug bounty inputs, and security monitoring inform risk identification and treatment.

System of Record: The Risk Register and Treatment Plan are maintained in Vanta.  
Link: https://app.vanta.com/risk-management/risk-register

## Risk Categories

Mesh Intelligent Technologies, Inc. considers and assesses risks across:  
- Reputational  
- Contractual  
- Regulatory/Compliance  
- Economic/Financial  
- Fraud  
- Privacy  
- Environmental & Sustainability  
- Impact on People  
- Use of Cloud Services  
- Operational Capacity  
- Third-Party / Vendor and Supply Chain  
- AI/ML and LLM-Specific Risks (see below)

### AI/ML and LLM-Specific Risk Considerations
- Prompt Injection and Model Manipulation: Risks of malicious instructions in prompts or content that alter model behavior (consider input filtering, allow/deny lists, tool-use restrictions, output guards).  
- Data Leakage and Sensitive Information Exposure: Risks of exposing customer or proprietary data via prompts, context windows, logs, or outputs (apply data minimization, redaction, masking, and strict logging policies).  
- Model Theft and Abuse: Risks of model or embedding misuse, API key compromise, excessive usage (apply rate limits, tenant scoping, key rotation).  
- Dataset Provenance and IP: Risks related to training/fine-tuning sources, licensing, and IP.  
- Bias, Safety, and Misuse: Risks of harmful or biased outputs; apply evaluation, content filters, and human-in-the-loop controls for sensitive use cases.  
- Third-Party LLM Providers: Risks in subprocessor regions, data retention, training usage, incident SLAs; require appropriate DPAs, residency assurances, and deletion timelines.  
- Privacy: Ensure personal data handling aligns with privacy laws and commitments.

## Risk Criteria

Overall risk is determined by combined likelihood and impact on the confidentiality, integrity, availability, or privacy of organizational and customer information or business systems.  
Management may adjust risk rankings based on system criticality, exploitability, and other relevant factors.

## Risk Response, Treatment, and Tracking

Risks are prioritized and maintained in a Risk Register, with one or more of the following responses:  
- Mitigate: Implement controls to reduce likelihood or impact.  
- Accept: Monitor the risk with documented rationale.  
- Transfer: Shift risk via contracts or insurance.  
- Avoid: Cease or change the activity to end the risk.  

For responses other than Accept or Avoid, a Risk Treatment Plan is documented with owner, target dates, and measurement.

## Risk Management Procedures

1. Maintain a Risk Register and Treatment Plan (Vanta).  
2. Rank risks by likelihood and impact (critical, high, medium, low, negligible).  
3. Determine overall risk from likelihood and impact.  
4. Where feasible, estimate potential monetary loss.  
5. Prioritize remediation considering risk, cost, effort, resources, and business impact; parallelize remediations when appropriate.  
6. Provide regular risk reports to senior leadership; escalate critical items.  
7. Perform formal enterprise risk assessment at least annually and upon material change (including new high-risk vendors, major product changes, or significant incidents).  
8. Integrate third-party risk inputs (SOC 2/ISO reports, pen test summaries, privacy terms) and AI/LLM risks into the Risk Register.  
9. Vendor reassessment cadence by tier: High annually; Medium every 2 years; Low on renewal; due dates tracked in the Risk Register.  
10. Risk Register Data Requirements (audit-ready): risk ID, title, description, owner, category, source (incident/scan/assessment/vendor/change/AI eval), likelihood, impact, inherent score, treatment option and rationale, planned controls, residual score, due date, evidence links (Drive/Vanta/GitHub/Workspace), next review date, and approval/acceptance record.

### Inherent vs Residual Risk
- Record inherent risk prior to treatment and residual risk after controls; show the delta and note any remaining exposure. Re-evaluate residual risk after implementing mitigations and at each review.

### Intake SLA
- New risks from incidents, pen tests, bug bounty, vulnerability scans, audit findings, material changes, vendor reviews, or AI/LLM evaluations must be triaged into the Risk Register within 10 business days.

### Time-Bounded Acceptance
- Accepted risks must include compensating controls, an explicit expiry date (≤ 6 months unless renewed), assigned owner, and next review date.

### Vendor–Risk Linkage
- High-risk vendors that access production systems or customer data must have corresponding risk entries linked to their vendor assessments; mitigations and reassessment dates must align to vendor tier cadence.

### Meeting Attestation
- Quarterly governance minutes include attendees and an attestation that the listed risks and treatments were reviewed and approved or routed for escalation.

## Risk Acceptance Criteria and Levels (Legacy Roles – Preserved)

- CEO: Ultimately responsible for the acceptance and/or treatment of any risks to the organization.
- Chief Information Officer: Can approve the avoidance, remediation, transference, or acceptance of any risk cited in the Risk Register.
- IT Manager / Systems Engineer: Responsible for the identification and treatment plan development of all Information Security related risks; communicates risks to top management and adopts risk treatments in accordance with executive direction.

Note: In the current structure, CIO responsibilities are fulfilled by the CTO, and IT Manager/Systems Engineer responsibilities are fulfilled by the Head of Cloud Infrastructure & Security. This section is retained to ensure continuity with the 2023 policy and audit evidence.

## Risk Appetite & Thresholds

- Risk Appetite: Mesh Intelligent Technologies, Inc. maintains a low appetite for risks affecting production systems, customer data, legal/regulatory obligations, or safety.  
- Acceptance Thresholds:  
  - Critical risks: Mitigate or avoid; temporary acceptance requires CEO approval and compensating controls; target remediation ≤ 30 days.  
  - High risks: Mitigate; documented acceptance requires executive approval and review; target remediation ≤ 90 days.  
  - Medium/Low risks: Acceptable with documented rationale, owner, and review cadence.  
- Category-Level Appetite (examples):  
  - Privacy/Customer Data: Very low appetite  
  - Model Safety/Bias: Low appetite  
  - Availability/Uptime: Low appetite  
  - Financial/Contractual: Low to medium appetite depending on exposure and mitigation options  
- Numeric acceptance guidance (matrix mapping): Medium risks with composite score ≤ 9 may be accepted with compensating controls and semiannual review; document cost/benefit rationale in the Risk Register.

## Governance & KRIs

- Governance Cadence: Quarterly Risk Review with CEO (Tsavo Knott), Corporate Secretary & CPO (Mack Myers), Security/GRC, Head of Cloud Infrastructure & Security (Hiro Tamada), and CTO (Mark Widman); ad-hoc reviews upon material changes or incidents.  
- Evidence: Meeting minutes, Vanta Risk Register export, current Treatment Plan; stored in Google Drive data room.  
- Key Risk Indicators (tracked quarterly):  
  - % risks reviewed on schedule  
  - # open Critical/High beyond SLA  
  - % vendor reassessments on-time per tier  
  - # AI/LLM risks with active compensating controls  
  - # material incidents and resulting risk updates  
- Executive/Board Reporting: Provide an annual risk posture summary (Q4) to the CEO and board; store in Google Drive.

## Risk Exceptions (Process)

- Exceptions must document owner, scope, rationale, compensating controls, and expiry date.  
- Approvals: CEO (material), Corporate Secretary and Security/GRC (non-material).  
- Duration: Time-bound; reviewed on or before expiry with decision to extend, mitigate, or retire.

## Incident and Change Triggers

- Post-Incident Risk Updates: For Sev‑1/major incidents, update or create associated Risk Register entries and reassess within 10 business days of postmortem. Evidence: incident postmortem (Google Workspace), related GitHub issues/links, and control updates.  
- Roles in Cloud-Related Incidents: Head of Cloud Infrastructure & Security (Hiro Tamada) and CTO (Mark Widman) are primary technical leads; CEO (Tsavo Knott) and Corporate Secretary & CPO (Mack Myers) are executive stakeholders; Head of CI/CD & DevOps (Nathan Courtney) participates for deployment/release risks and remediation.  
- Material Change Risk Review (pre‑go‑live): Triggered by new data flows, PII scope changes, LLM provider/region changes, production schema changes, or major architectural modifications. Require a documented risk review and approvals before go‑live; link evidence (design docs, tickets) in the Risk Register.

## BIA and Impact Alignment

- Impact scoring aligns to Business Impact Analysis (BIA) and the Legal Policy’s BCP/DR objectives (RTO/RPO).  
- High/Very High impacts reflect material disruption to critical services or breach of regulatory commitments.  
- Project and change reviews must consider BIA classification for scope and prioritization.

## AI/LLM Risk Mapping to NIST AI RMF

- Govern: Define roles, accountability, and policies for AI usage and vendor selection.  
- Map: Identify AI system context, data flows, and risks (prompt injection, data leakage, model abuse).  
- Measure: Evaluate model behaviors and controls (filters, redaction, RBAC, rate limits); track KRIs.  
- Manage: Implement mitigations, compensating controls, and continuous monitoring; update Risk Register entries and treatment tasks.  
- Evaluation Cadence: Conduct AI/LLM red‑team or evaluations quarterly or prior to major releases for prompt injection, data leakage, model safety/bias; record results, issues, and mitigations in the Risk Register.  
- Data Handling and Logs: Retain AI prompts/responses/logs only as necessary for operations and security with a default 90‑day cap; apply masking/redaction of sensitive data and restrict access based on least privilege.  
- Model Improvement Using Customer Content: Customer content is not used for model training or improvement by default; any exceptions must be explicitly authorized in writing on a per‑engagement basis and documented with appropriate safeguards in the Risk Register and contracts.

## Templates & Evidence

- Templates: Risk Assessment template, Risk Acceptance form, Treatment Plan template (stored in Google Drive data room).  
- System of Record: Vanta Risk module is the authoritative risk register; evidence artifacts stored in Drive with links from register entries.  
- Incident Tracking: Working groups and incident groups track issues in Google Workspace and GitHub; link incident IDs and reports to Risk Register entries.

## Information Security in Project Management

All technical projects or projects with potential risk to the company must consider information security risk from planning through completion, including:  
- Initial information security risk assessments  
- Early identification of security and privacy requirements  
- Ongoing assessment and management of risks, especially for internal and external communications and third-party integrations

## Roles and Responsibilities

| Role | Responsibility |
| ----- | ----- |
| CEO (Tsavo Knott) | Ultimately responsible for acceptance/treatment of risks to the organization. |
| Corporate Secretary & CPO (Mack Myers) | Owns policy oversight, risk governance cadence, and maintains executive reporting. |
| Security/GRC (function) | Operates the risk program; maintains Risk Register; drives assessments and treatment plans; integrates third-party and AI/LLM risks; contact: security@pieces.app. |
| Head of Cloud Infrastructure & Security (Hiro Tamada) | Leads technical risk identification, cloud responsibility-matrix, and control validation. |
| CTO (Mark Widman) | Oversees strategic risk decisions for architecture and AI/ML; adjudicates compensating controls. |
| Chief Information Officer (fulfilled by CTO) | Approves avoidance, remediation, transference, or acceptance of risks cited in the Risk Register. |
| IT Manager / Systems Engineer (fulfilled by Head of Cloud Infrastructure & Security) | Identifies risks and develops treatment plans; communicates risks to top management and adopts risk treatments per executive direction. |
| Chief AI Officer (Sam Jones) | Governs AI/ML risk posture, model/data usage policy, safety and bias evaluations, and recommends AI vendor risk acceptance. |
| Head of CI/CD & DevOps (Nathan Courtney) | Owns pipeline security (build signing, artifact integrity), CI secrets management, and software supply chain risk inputs (SBOM, dependency scanning). |
| System Owners / Engineering Leaders | Identify and report risks, document use cases and data types, implement mitigations and controls. |

## Other Resources

- ISMS Risk Assessment and Treatment Policy (internal)  
- 04-ISMS Risk Assessment and Treatment Policy  
- Risk Register (Vanta): https://app.vanta.com/risk-management/risk-register  
- Risk Assessment Spreadsheet (internal)

## ISO 27001 / 27701 Coverage

- ISO 27001 6.1; 6.2

## TSC Mapping (SOC 2)

- CC3.1, CC3.2 (Risk Assessment and Identification)  
- CC3.3 (Risk Mitigation)  
- CC4.x (Monitoring, in conjunction with continuous risk review)  
- CC5.2 (Access-related risk controls where applicable)

## Change Log

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 01-Jan-2023 | Initial Policy | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |

**Assurance (No Regression):** The 2025 v1.1.0 policy retains 100% of the 2023 sections and wording intent and expands with additional detail (matrix, roles, acceptance criteria, procedures, appendices). ISO 27005/NIST 800‑30/800‑37 references remain; risk categories, procedures, and matrices are preserved and expanded.

---

# APPENDIX A – Risk Assessment Process

Based on NIST SP 800-30; used to:  
- Prepare and conduct effective risk assessments  
- Communicate/share results and risk information  
- Maintain risks on an ongoing basis

### Step 1: Prepare for the Assessment
- Identify purpose of the assessment and decisions supported  
- Define scope (functions/processes, timeframe, architectural/technical considerations)  
- Document assumptions/constraints (priorities, objectives, resources, team expertise)  
- Identify information sources (architecture/configs, legal/regulatory, threat sources/events, vulnerabilities, impacts, existing controls)

### Step 2: Conduct the Assessment
- Identify Threat Sources (human—intentional/unintentional; environmental; natural; system/equipment) and consider capability, motive/intent, targeted assets  
- Identify Threat Events relevant to Mesh Intelligent Technologies, Inc.  
- Identify Vulnerabilities and influencing conditions (people, process, technology)  
- Determine Likelihood (consider threat capability/intent/opportunity; vulnerabilities; existing or planned safeguards)  
- Determine Impact (business/operational, financial, reputation, legal/regulatory; consider existing/planned safeguards)  
- Determine Risk by combining likelihood and impact

### Step 3: Communicate and Share the Results
- Communicate results to decision makers and executive leadership to drive risk-based decisions and support risk response  
- Share the assessment and risk information with appropriate personnel

### Step 4: Maintain the Assessment
- Monitor risk factors that drive changes in risk  
- Update assessments at least annually and after material changes or incidents

# APPENDIX B – Risk Assessment Matrix and Description Key

| RISK = LIKELIHOOD * IMPACT | LIKELIHOOD |  |  |  |  |
| :---- | :---: | :---: | :---: | :---: | :---: |
| **IMPACT** | **Very unlikely: 1** | **Unlikely: 2** | **Somewhat likely: 3** | **Likely: 4** | **Very likely: 5** |
| **Very high impact: 5** | **5** | **10** | **15** | **20** | **25** |
| **High impact: 4** | **4** | **8** | **12** | **16** | **20** |
| **Medium impact: 3** | **3** | **6** | **9** | **12** | **15** |
| **Low impact: 2** | **2** | **4** | **6** | **8** | **10** |
| **Very low impact: 1** | **1** | **2** | **3** | **4** | **5** |

| RISK LEVEL | RANGE | RISK DESCRIPTION |
| ----- | ----- | ----- |
| **Negligible** | 1–3 | A threat event could be expected to have a very limited adverse effect on organizational operations, mission capabilities, assets, individuals, customers or other organizations. |
| **Low** | 4–8 | A threat event could be expected to have a limited adverse effect on organizational operations, mission capabilities, assets, individuals, customers, or other organizations. |
| **Moderate** | 9–15 | A threat event could be expected to have a serious adverse effect on organizational operations, mission capabilities, assets, individuals, customers, or other organizations. |
| **High** | 16–20 | A threat event could be expected to have a severe adverse effect on organizational operations, mission capabilities, assets, individuals, customers, or other organizations. |
| **Critical** | 21–25 | A threat event could be expected to have a catastrophic adverse effect on organizational operations, mission capabilities, assets, individuals, customers, or other organizations. |

| LIKELIHOOD LEVEL | LIKELIHOOD DESCRIPTION | RATING (NUMERICAL) |
| ----- | ----- | :---: |
| **Very Low** | A threat event is so unlikely that it can be assumed its occurrence may not be experienced. A threat source is not motivated or has no capability, or controls prevent or significantly impede exploitation. | 1 |
| **Low** | A threat event is unlikely, but there is a slight possibility it may be experienced. A threat source lacks sufficient motivation or capability, or controls impede exploitation. | 2 |
| **Moderate** | A threat event is possible. A threat source is motivated or has capability, but controls may significantly reduce or impede successful exploitation. | 3 |
| **High** | A threat event is likely and its occurrence can be assumed. A threat source is highly motivated or has sufficient capability/resources, but some controls may reduce or impede successful exploitation. | 4 |
| **Very High** | A threat event is highly likely. A threat source is highly motivated or has sufficient capability/resources, and no controls are in place or those in place are ineffective. | 5 |

Probability guidelines (legacy scale, preserved for continuity):  
- Very Low (1): ≈ 5% in a 5–10 year period  
- Low (2): ≈ 6%–20% in a 2–5 year period  
- Moderate (3): ≈ 21%–50% in a 1–2 year period  
- High (4): ≈ 51%–80% in a 1 year period  
- Very High (5): > 80% in a ≤ 1 year period

| IMPACT LEVEL | IMPACT DESCRIPTION | RATING (NUMERICAL) |
| ----- | ----- | :---: |
| **Negligible** | A threat event could be expected to have almost no adverse effect on organizational operations, mission capabilities, assets, individuals, customers or other organizations. | 1 |
| **Low** | A threat event could be expected to have a limited adverse effect; degradation of mission capability yet primary functions can still be performed; minor damage; minor financial loss; range of effects limited to some cyber resources but no critical resources. | 2 |
| **Moderate** | A threat event could be expected to have a serious adverse effect; significant degradation of mission capability yet primary functions can still be performed at a reduced capacity; minor damage; minor financial loss; range of effects significant to some cyber resources and some critical resources. | 3 |
| **High** | A threat event could be expected to have a severe or catastrophic adverse effect; severe degradation or loss of mission capability and one or more primary functions cannot be performed; major damage; major financial loss; range of effects extensive to most cyber resources and most critical resources. | 4 |
| **Critical** | A threat event could be expected to have multiple severe or catastrophic adverse effects on organizational operations, assets, individuals, other organizations, or the Nation. Range of effects sweeping, involving almost all cyber resources. | 5 |

---

## References (external)
- SOC 2 Risk Assessment CC3.1/CC3.2 explained: https://www.isms.online/soc-2/controls/risk-assessment-cc3-1-explained/; https://www.isms.online/soc-2/controls/risk-assessment-cc3-2-explained/  
- How to write SOC 2 risk management policy: https://www.isms.online/soc-2/policies/how-to-write-soc-2-risk-management-policy/  
- SOC 2 risk assessment guide: https://concertium.com/soc-2-risk-assessment-guide/  
- SOC 2 for SaaS companies: https://sprinto.com/blog/why-soc-2-for-saas-companies/  
- AI/LLM risks (prompt injection, data leakage): https://witness.ai/prompt-injection/; https://konghq.com/blog/enterprise/llm-security-playbook-for-injection-attacks-data-leaks-model-theft  
- SOC 2 in AI-driven businesses: https://www.auditpeak.com/soc-2-compliance-in-ai-driven-businesses/; https://www.lbmc.com/blog/generative-ai-soc-2/  
- NIST AI Risk Management Framework: https://www.diligent.com/resources/blog/nist-ai-risk-management-framework/; https://www.scrut.io/post/nist-ai-risk-management-framework  
- Third-party risk & SOC 2: https://blog.rsisecurity.com/third-party-risk-management-soc-2-and-vendor-security/  
- Risk management automation (Vanta): https://www.vanta.com/collection/grc/risk-management-automation/; https://www.vanta.com/collection/tprm/thrid-party-risk-requirements-soc-2/