---
title: Business Continuity and Disaster Recovery (BC/DR)
owner:
  - Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))
stakeholders:
  - Hiro Tamada (Head of Cloud Infrastructure)
  - Mark Widman (Chief Technology Officer)
  - Nathan Courtney (Head of CI/CD & DevOps)
  - Katie Storm (AirCFO, HR/Asset Manager)
  - Legal Counsel
approver: Tsavo Knott (CEO)
version: 1.1.0
effective_date: 2025-08-19
review_frequency: Annual
status: Approved
related:
  standards: []
  procedures: []
  controls: []
repo: https://github.com/pieces-app/soc-II-policy
---

# Business Continuity and Disaster Recovery (BC/DR)

**Policy Owner:** Mack Myers (Co-Founder, Corporate Secretary & Chief Product Officer (CPO))

**Effective Date:** August 19, 2025

# Purpose

The purpose of this business continuity plan is to prepare Mesh Intelligent Technologies, Inc. in the event of service outages caused by factors beyond our control (e.g., natural disasters, man‑made events), and to restore services to the widest extent possible in a minimum time frame.

# Scope

All Mesh Intelligent Technologies, Inc. IT systems that are business critical. This plan applies to all employees of Mesh Intelligent Technologies, Inc. and to all relevant external parties, including but not limited to consultants and contractors.

The following scenarios are excluded from the BC/DR plan scope:

- Loss of availability for a production hosting service provider (i.e., Google Cloud Platform)
- Loss of availability of Mesh Intelligent Technologies, Inc. satellite offices (these will be treated as incidents)

In the event of a loss of availability of a hosting service provider, the Head of Cloud Infrastructure will confer with the CTO, CPO/Corporate Secretary, and executive staff to determine an appropriate response strategy.

# Policy

- In the event of a major disruption to production services and a disaster affecting the availability and/or security of Mesh Intelligent Technologies, Inc. offices, senior managers and executive staff shall determine mitigation actions.
- A disaster recovery test, including a test of backup restoration processes, shall be performed at least annually.
- Backup restoration tests for production data are performed at least quarterly (per Legal & Security Policies commitments).
- Continuity of information security shall be considered along with operational continuity.
- In the case of an information security event or incident, refer to the Incident Response Plan.

# Testing & Maintenance

- Exercises: Conduct at least one annual tabletop BC/DR exercise and one technical disaster recovery exercise.  
- Backup Restores: Perform quarterly restore tests for critical data stores (e.g., databases, object storage, configurations) and document results.  
- Communications: Semiannual call-tree/notification drill and alternate‑channel communication test (Slack, phone, Google Meet).  
- Evidence: Store BC/DR test plans, results, screenshots, and approvals in this repository under `evidence/bcdr/` with dated folders (e.g., `evidence/bcdr/2025-09-30-q3-restore-test/`).

# Alternate Work Facilities

If a Mesh Intelligent Technologies, Inc. office becomes unavailable due to a disaster, all staff shall work remotely from their homes or any safe location.

# Communications and Escalation

- Executive staff and senior managers should be notified of any disaster affecting Mesh Intelligent Technologies, Inc. facilities or operations.
- Communications shall take place over any available regular channels including Slack, email (Google Workspace), phone, and Google Meet.
- Key contacts and on‑call schedules are maintained by the Corporate Secretary in the Google Drive data room and are available to executives and managers.

## Key Contacts & Resources

- Primary evidence and plans repository: https://github.com/pieces-app/soc-II-policy  
- Evidence folder (BC/DR): `evidence/bcdr/`  
- Key Contacts and On‑Call: Google Drive data room (Corporate Secretary)  
- Incident Response Plan: Security program index in this repository; link maintained by Corporate Secretary  

# Roles and Responsibilities

| Role | Responsibility |
| :---- | :---- |
| Head of Cloud Infrastructure (Hiro Tamada) | Leads BC/DR efforts for production platforms to mitigate losses and recover cloud services and data. Coordinates failover and restoration activities. |
| CTO (Mark Widman) | Leads continuity of customer‑facing services and technical decision‑making during disasters; approves recovery priorities with the CEO. |
| Corporate Secretary & CPO (Mack Myers) | Owns this plan; coordinates executive communication; maintains key contacts and external notifications with Legal. |
| Head of CI/CD & DevOps (Nathan Courtney) | Restores CI/CD systems and runners; validates build/release pipelines and artifact integrity. |
| HR (AirCFO, Katie Storm) | Manages internal communications to employees and any actions needed to maintain health and safety. Coordinates remote work readiness. |
| Legal Counsel | Oversees regulatory notifications and contractual communications as required. |
| Department Heads & Managers | Communicate with staff and ensure continuity of departmental functions; escalate issues to executive staff. |

## Command & Control Structure (During Activation)

- Incident Commander: CEO or delegate (CTO).  
- Operations Lead: Head of Cloud Infrastructure (production continuity).  
- Communications Lead: Corporate Secretary & Legal Counsel (customer/regulatory).  
- Logistics/People: HR (AirCFO) for workforce, access, and facilities.  
- Scribes: Assigned by Corporate Secretary; maintain event log and decision register.

# Notifications & Regulatory Alignment

- Customer Communication: Executive communications follow the Legal & Security Policies; inform customers of material service disruption, expected impact, and restoration progress.  
- Regulatory Notifications: Legal Counsel coordinates any required notifications under applicable laws/regulations and contractual commitments.  
- Status and Updates: Communications cadence determined by severity; maintain an internal log of updates and decisions during the event.

## Subprocessor/Provider Notifications

- We subscribe to status notifications for critical subprocessors (e.g., Google Cloud status for GCS/Cloud SQL, GitHub, Google Workspace, Sentry, Segment, Mixpanel, Paddle, HubSpot). Upon receiving a provider alert that materially impacts our services, we assess blast radius and, if customer impact is likely, notify customers per the Legal & Security Policies.  
- Provider outage updates are tracked in the event log and referenced in customer communications.

# Backup & Data Recovery Strategy (GCP and SaaS)

- Google Cloud Storage (GCS): Server‑side encryption enabled; object versioning for critical buckets where feasible; integrity verified via checksums; quarterly restore tests simulate region or bucket loss.  
- Databases (e.g., Cloud SQL/managed data stores): Automated daily backups with configured retention; point‑in‑time recovery where supported; quarterly restore to a staging project for validation.  
- Artifact Registry (GAR): Backups or replication/config export retained; verify artifact/attestation availability during DR tests.  
- GitHub: Repositories are hosted by GitHub; enforce branch protections and required reviews; periodic mirrored backups of critical repositories to GCS (at least weekly) are recommended; export organization configuration as code where feasible.  
- SaaS Exports: For critical SaaS (e.g., CRM, finance, HR), schedule periodic exports or enable vendor backup features to support continuity of operations.

# CI/CD, Access, and Secrets Recovery

- CI/CD (GitHub Actions): Validate ability to rebuild critical services after an outage; ensure runners and OIDC trust to Google Cloud can be re‑established; store workflow definitions as code; keep copies of environment protection rules.  
- Credentials & Secrets: Break‑glass access and DigiCert code signing credentials are vaulted; recovery requires CEO and CTO approval. After a disaster-related incident, rotate impacted secrets and certificates per the Cryptography Policy.  
- IAM Recovery: Ensure group‑based access can be restored via Google Workspace and Google Cloud IAM; maintain documented mapping of roles to groups and projects.

# Continuity of Critical Services

Procedures for maintaining continuity of critical services in a disaster are provided in Appendix A.

Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO) are provided in Appendix B.

Continuity strategy overview:

| Key Business Process | Continuity Strategy |
| :---- | :---- |
| Customer (Production) Service Delivery | Rely on Google Cloud Platform availability commitments and SLAs; prioritize regional redundancy where technically feasible. |
| IT Operations | Not dependent on HQ; critical data backed up to alternate locations; device and SaaS access via Google Workspace SSO/MFA. |
| Email & Collaboration | Utilize Google Workspace and its distributed nature; rely on Google’s SLAs. |
| Finance, Legal, and HR | All systems are vendor‑hosted SaaS applications; rely on vendor SLAs and export/backup capabilities. |
| Sales and Marketing | All systems are vendor‑hosted SaaS applications. |

## Plan Activation

This BC/DR plan shall be automatically activated in the event of the loss or unavailability of a Mesh Intelligent Technologies, Inc. office, or a natural disaster (e.g., severe weather, regional power outage, earthquake) affecting the larger region of operations.

### Activation Checklist (Initial 60 Minutes)

1. Declare severity (Sev‑1 for production impact; Sev‑2/3 for corporate ops).  
2. Assign Command & Control roles; start event log and timeline.  
3. Stabilize safety and communications (Slack, phone, Google Meet).  
4. Triage systems: GCP (prod), Google Workspace, GitHub Actions, critical SaaS.  
5. Initiate failover/workarounds per scenario; freeze non‑essential changes.  
6. Draft initial internal and (if applicable) customer status messages.  
7. Validate backups/restoration paths if data risk suspected.

Working Group Protocol: Form a working group of relevant stakeholders immediately upon activation; schedule repeating calendar invites (e.g., every 30–60 minutes) for status and decision checkpoints until resolution.

| Version | Date | Description | Author | Approved by |
| :---: | :---: | :--- | :--- | :--- |
| 1.0.0 | 01-Jan-2023 | Initial Plan | Georgia Donmoyer | Tsavo Knott (CEO) |
| 1.1.0 | 19-Aug-2025 | 2025 Refresh | Executive Leadership | Tsavo Knott (CEO) |

# Appendix A – Business Continuity Procedures by Scenario

## HQ Offline (power and/or network)

- CRM, video conferencing, and corporate email unaffected (SaaS).  
- HQ staff offline temporarily; remote staff unaffected.

Procedure:
1. HQ staff relocate to home offices (target 30–60 minutes).
2. Verify telephony, CRM, and email connectivity at home offices (target 10 minutes).
3. Remotely resume normal operations.

## Cloud Services Degradation/Outage (Non‑Provider‑Wide)

- Scoped service degradation or outage in GCP or a critical SaaS provider.  
- Production services impacted depending on subsystem.

Procedure:
1. Engage incident response; identify blast radius and apply mitigations.  
2. Execute failover or rollback where feasible; increase communication cadence to stakeholders.  
3. Document impacts and update risk register if needed.

## Provider‑Wide Outage Communications (Out of Scope Operationally)

- If a provider‑wide outage occurs (e.g., major GCP regional disruption), Mesh Intelligent Technologies, Inc. will follow provider guidance and SLAs.  
- Communicate status to customers, pause non‑critical changes, and enable read‑only modes where feasible to reduce risk and preserve RPO objectives.  
- Post‑event, capture lessons learned and evaluate feasibility of additional redundancy within provider regions.

## Disaster Event at HQ (regional severe weather or building access loss)

- Corporate facilities inaccessible; production services unaffected.  
- Staff move to remote‑only operations.

Procedure:
1. Activate remote‑work continuity; verify endpoints meet MDM posture.  
2. Notify customers of any support delays; prioritize critical service operations.  
3. Shift any physical‑dependent activities to remote alternatives.

## SaaS Tools Down (Email/CRM/Video Conferencing)

Impact: Collaboration and support triage impacted. Production unaffected.

Procedures:
- Email down (Google Workspace): Use alternate channels (Slack, phone); queue external communications via support channels until restoration.  
- CRM down: Switch to interim tracking in a restricted Google Sheet; reconcile to CRM when restored.  
- Video Conferencing down: Utilize backup provider; reschedule non‑critical meetings.

## ML Model Serving Rollback (AI Scenario)

Impact: Degraded model behavior or serving outage; customer‑visible model quality issues.

Procedure:
1. Identify last known good model revision (Hugging Face VCS commit/hash) and corresponding data/config.  
2. Pin deployment manifests to the prior revision; rebuild artifacts and publish to Artifact Registry.  
3. Redeploy with guarded toggles; monitor KPIs and error rates.  
4. Communicate status to stakeholders/customers if service quality impacted; record decision and verification evidence.  
5. Open a follow‑up work item to root cause model degradation; store evidence under `evidence/bcdr/<event>/`.

## Incident Closure & After‑Action

1. Confirm services restored and access normalized.  
2. Rotate impacted secrets or credentials per Cryptography Policy.  
3. Conduct After‑Action Review within 10 business days; document lessons learned and assign improvements.  
4. Update risk register and BC/DR procedures as needed.

# Appendix B – RTOs/RPOs

| Rank | Asset | Affected Assets | Business Impact | Users | Owners | RTO | RPO | Notes |
| :---: | ----- | ----- | ----- | ----- | ----- | :---: | :---: | ----- |
| 1 | Google Cloud (Production) | Core services | Potential service disruption | All customers | Head of Cloud, CTO | ≤ 4 hours | ≤ 24 hours | Aligned to Legal & Security Policies (BCP/DR). |
| 2 | Google Workspace | Email & collaboration | Communication delays | All | Corporate Secretary, HR | ≤ 8 hours | ≤ 24 hours | Vendor SLA dependent. |
| 3 | Artifact Registry (GAR) | Images & attestations | Deployment delays | Engineering | Head of CI/CD | ≤ 8 hours | ≤ 24 hours | Verify provenance during DR. |
| 4 | CI/CD (GitHub Actions) | Build & release | Slow releases/patching | Engineering | Head of CI/CD | ≤ 8 hours | ≤ 24 hours | Offline builds for emergency patches. |
| 5 | Corporate Office | Site | Office access loss | All | Corporate Secretary, HR | N/A | N/A | Activate remote work. |
| 6 | Finance/Legal/HR SaaS | Records & operations | Operational delays | G&A | G&A Owners | ≤ 48 hours | ≤ 24 hours | Vendor SLA dependent. |

# Appendix C1 – Critical Systems & Backup Schedule Summary

| System | Backup/Protection | Retention | Test Cadence |
| :---- | :---- | :---- | :---- |
| GCS (critical buckets) | Server‑side encryption, versioning (where feasible); checksums | ≥ 35 days (per Legal policy); longer for archives as needed | Quarterly restore drills |
| Cloud SQL / managed DBs | Automated daily backups; PITR where supported | Per service defaults + business needs | Quarterly restore to staging |
| Artifact Registry (GAR) | Artifact availability + attestation retention | Align to release retention; attestations retained with artifacts | Validate in DR exercises |
| GitHub (source/CI) | Hosted; config as code; weekly GCS mirror of critical repos (recommended) | 90+ days for mirrors | Semiannual repo restore test |
| Google Workspace | Vendor‑managed; export critical records where required | Per vendor | Annual export verification |

# Appendix C2 – BC/DR Testing Calendar (Overview)

| Quarter | Exercise | Scope |
| :---- | :---- | :---- |
| Q1 | Tabletop | HQ outage + comms drill |
| Q2 | Technical DR | Cloud SQL restore + GAR validation |
| Q3 | Communications drill | Call‑tree and alternate channels |
| Q4 | Technical DR | GCS restore + CI/CD rebuild |
# Appendix C – Vendor & SaaS Continuity Matrix (Abbreviated)

| Service | Purpose | Continuity Strategy |
| :---- | :---- | :---- |
| Google Cloud Platform | Production infrastructure | Provider SLAs; multi‑zone/region where feasible; backups & DR tests |
| Google Workspace | Email, docs, collaboration | Provider SLAs; alternate channels (Slack/phone) |
| GitHub Enterprise | Source control & CI/CD | Protected environments; configuration as code; mirrored backups |
| Sentry | Monitoring/telemetry | Provider SLAs; export critical alerts where feasible |
| Segment/Mixpanel | Analytics | Provider SLAs; throttle non‑critical ingestion during DR |
| Paddle/HubSpot | Billing/CRM | Provider SLAs; periodic data exports |

# Appendix D – Communication Templates

Templates for internal and external communications during BC/DR events are maintained in the Google Drive data room (Corporate Secretary). Templates include initial notice, status updates, and resolution summaries.

# Appendix E – Evidence Index

Evidence of BC/DR testing, backup restores, communications drills, and lessons learned is stored in this repository:

- Repository: https://github.com/pieces-app/soc-II-policy  
- Path: `evidence/bcdr/` with dated subfolders for each exercise and test  



