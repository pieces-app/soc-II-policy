# Google Workspace Admin Baseline

Scope: Applies to all Google Workspace users and admins.

- Identity & Access: SSO/MFA required for all users; enforce strong MFA (FIDO2/TOTP) and block SMS except break-glass.
- Anti-Phishing & Malware: Enable advanced phishing/attachment protections; quarantine suspicious content; train users to report.
- Admin Roles: Assign least-privilege admin roles; review quarterly and on role change; log all admin actions.
- Audit & Logs: Retain audit logs per policy (≥ 365 days for security-relevant logs where feasible); export evidence as required.
- Device Management: Enforce MDM for devices accessing Restricted/Confidential data (per Asset Mgmt Policy); require screen lock, encryption, updates.
- Data Loss Prevention: Apply label-aware DLP for sharing and download restrictions on Confidential content; exceptions time-bound and logged.
- Evidence: Store admin config exports/screenshots under `evidence/ops/workspace/`.
