# BC/DR Activation Runbook (One-Page)

Purpose: Fast, practical checklist to activate and manage Business Continuity and Disaster Recovery (BC/DR) events. Evidence for all actions is stored in this repository under `evidence/bcdr/` with dated folders.

References:
- Legal & Security Policies (Customer-Facing) – Business Continuity & Disaster Recovery (Section 4), Notifications (privacy/regulatory): `LEGAL_POLICY_2025_COUNSEL_VERIFIED.md`
- BC/DR Plan (2025): `business-continuity-and-disaster-recovery-plan-2025.md`
- Repo root: https://github.com/pieces-app/soc-II-policy

Severity Definitions (quick):
- Sev-1: Production customer impact (availability/data risk)
- Sev-2: Critical internal platform impact (CI/CD, Workspace) without prod outage
- Sev-3: Corporate operations impact only

Command & Control (assign at activation):
- Incident Commander: CEO (Tsavo Knott) or delegate (CTO: Mark Widman)
- Operations Lead (Production): Head of Cloud Infrastructure (Hiro Tamada)
- CI/CD Lead: Head of CI/CD & DevOps (Nathan Courtney)
- Communications Lead: Corporate Secretary & CPO (Mack Myers) with Legal Counsel
- People/Logistics: HR (AirCFO: Katie Storm)
- Scribe: Assigned by Corporate Secretary (maintains event log and decisions)
- Technical SMEs (as needed): Chief AI Officer (Sam Jones), app/service owners

0–15 Minutes (Activate & Stabilize)
1. Declare severity and activate BC/DR; open an event log in `evidence/bcdr/YYYY-MM-DD-<short-name>/event-log.md`.
2. Confirm safety and primary comms: Slack, phone/SMS, Google Meet bridge.
3. Assign C2 roles above; start timeline (timestamps, actions, owners).
4. Initial triage: GCP (prod: GAR/GCS/Cloud SQL), Google Workspace, GitHub Actions, critical SaaS (CRM, billing, support).
5. Freeze non-essential changes; protect RPO (read-only modes where feasible).

15–30 Minutes (Assess & Communicate)
6. Identify blast radius; document affected regions/projects/services.
7. Operations Lead proposes mitigation (failover/rollback/workarounds); IC approves.
8. Comms Lead drafts internal status; if customer impact, prepare external notice (see templates) consistent with Legal policy.
9. Validate backups and recovery points for any at-risk data (Cloud SQL PITR, GCS versioning).

30–60 Minutes (Execute & Verify)
10. Execute failover/rollback; monitor KPIs; confirm GAR artifact/attestation availability.
11. Re-establish CI/CD path (Actions runners, OIDC to GCP); enable emergency patch path if needed.
12. Confirm Workspace/Collab alternatives (phone/SMS) for team continuity.
13. Send customer update if Sev-1; review regulatory notification triggers with Legal.

Customer & Regulatory Notifications
- Follow Legal & Security Policies Section 4 (BCP/DR) and notification guidance (privacy/regulatory).
- Comms cadence depends on severity; store copies in `evidence/bcdr/<event>/comms/`.

Recovery & Post-Event
14. Verify service restoration; remove change freezes; re-enable protections.
15. Rotate impacted credentials (e.g., DigiCert, cloud secrets) per Cryptography Policy.
16. After-Action Review within 10 business days; document lessons learned, owners, due dates.
17. File evidence: test outputs, screenshots, logs, final report in `evidence/bcdr/<event>/`.

Key Contact Pointers (not secrets)
- On-call/key contacts: Google Drive data room (Corporate Secretary)
- Vendor status pages: GCP, GitHub, Google Workspace, critical SaaS
- Risk Register link (Vanta) for material changes

Templates
- Initial internal: “We are investigating a [Sev-X] event impacting [systems]. Next update in [time].”
- Initial external (if Sev-1): “We’re experiencing a service disruption affecting [scope]. Our team is working to restore services. Next update by [time]. We apologize for the inconvenience.”

Evidence Checklist (file in event folder)
- Timeline/event log, decisions, mitigations
- Screenshots/logs of triage, failover/restore
- Customer/regulatory messages
- Root cause summary and action items

Ownership
- Maintainer: Corporate Secretary & CPO (runbook updates)
- Approver: CEO (or delegate)
