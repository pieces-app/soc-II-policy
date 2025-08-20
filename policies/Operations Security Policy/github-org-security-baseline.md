# GitHub Organization Security Baseline

Scope: Applies to all production repositories.

- Branch Protection: Require PR reviews (≥ 1 non-author; ≥ 2 for critical repos), required status checks, up-to-date branches, and dismiss stale approvals on new commits.
- CODEOWNERS: Define reviewers for critical paths; enforce required reviewers via org policy.
- Secret Protection: Enable GHAS secret scanning and push protection; delegated bypass only with documented exception.
- Dependabot: Enable security updates org-wide; monitor/merge per SLAs.
- Actions Security: Pin actions by commit SHA; restrict repository/org secrets; prefer environment secrets with least privilege.
- Environments & Deployments: Protect production with required reviewers and deployment gates; audit approvals.
- Runners: Scope self-hosted runners by labels and repository allowlists; prefer GitHub-hosted where feasible.
- Identity to Cloud: Use OIDC/workload identity for GCP; prohibit long-lived cloud keys in CI.
- Evidence: Store screenshots/exports under `evidence/ops/github/`.
