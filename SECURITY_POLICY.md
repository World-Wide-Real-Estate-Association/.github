# Security Protection Policy

## 1) Data classification
- **Public:** Intended for open publication; no confidentiality requirement.
- **Internal:** Operational and workflow data for maintainers; limit write access.
- **Sensitive:** Credentials, tokens, personal data, and any security-relevant metadata; strictly restricted access.

## 2) Encryption requirements
- **In transit:** Require TLS 1.2+ for all network communication.
- **At rest:** Use platform-managed encryption for repositories, logs, artifacts, and backups.
- **Secrets:** Store only in managed secret stores (for this repository: GitHub Actions secrets); never hardcode.

## 3) Access control (RBAC)
- Use least privilege by default.
- Keep workflow default permissions read-only; grant write only at job scope when required.
- Restrict merge rights and administrative actions to designated maintainers.
- Require pull-request review before merging protected branches.

## 4) Audit logging
- Keep CI workflow run history and review events enabled.
- Preserve security gate run results for investigation and compliance evidence.
- Record remediation decisions in pull requests when security gates fail and exceptions are approved.

## 5) Retention and deletion
- Define retention periods for logs and artifacts according to policy and regulatory needs.
- Remove obsolete artifacts and rotate secrets on schedule and after incidents.
- Immediately revoke and replace exposed credentials when detected.

## 6) Minimum controls before release
- Workflow structure validation passes.
- Secret scanning passes.
- Dependency advisory review passes.
- No unreviewed high-severity security findings remain open.
