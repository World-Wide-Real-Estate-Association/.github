# World Wide Real Estate Association — GitHub Automation Repository

This repository contains GitHub Actions workflows and governance documents that drive the pull-request learning flow and enforce security/compliance readiness.

## Repository purpose
- Guide contributors through a structured pull-request lifecycle course (steps 0–6 and finish).
- Enforce workflow security standards and immutable action pinning.
- Run governance and security controls continuously for reliability and compliance.

## Structure
- `.github/workflows/`  
  Step workflows and validation/security/governance gates.
- `.github/steps/`  
  Step instructions and current-step state (`-step.txt`).
- repository root (`./`)  
  Security and telemetry governance policy documents.

## Key workflows
- `0-welcome.yml` to `6-merge-your-pull-request.yml`: step progression workflows.
- `7-validate-workflows.yml`: YAML and workflow structure/security invariant validation.
- `8-security-gates.yml`: secret scanning and dependency advisory review.
- `9-governance-readiness.yml`: required governance-document section validation.

## Security and governance documents
- `SECURITY_POLICY.md`
- `SECURE_IMPLEMENTATION_CHECKLIST.md`
- `SECURITY_READINESS_REPORT.md`
- `ZERO_TRUST_GOVERNANCE_UPDATE_TEMPLATE.md`
- `TELEMETRY_KPI_COMPLIANCE_FRAMEWORK.md`

## Operational expectations
- Keep all third-party GitHub Actions pinned to immutable commit SHAs.
- Keep default workflow permissions read-only and scope write permissions to the minimum required job.
- Keep `persist-credentials: false` on checkout steps.
- Require validation and security workflows to pass before merge.

## Next implementation priorities
1. Enforce required status checks in branch protection/rulesets.
2. Add CODEOWNERS coverage for workflow and governance files.
3. Maintain weekly/monthly/quarterly governance cadence from policy docs.
