# Secure-by-Default Implementation Checklist

## Rough draft gate
- [ ] Data is classified (public/internal/sensitive) per component.
- [ ] Trust boundaries and data flows are documented.
- [ ] Zero Trust verification points are identified for all privileged actions.
- [ ] Secrets are only referenced from secure stores.
- [ ] Encryption expectations are defined (in transit + at rest).
- [ ] RBAC roles and least-privilege permissions are identified.
- [ ] Logging/audit events are defined for auth, writes, and failures.
- [ ] Detection rules cover auth anomalies, privilege escalation, and policy drift.
- [ ] Retention/deletion expectations are defined for each data type.
- [ ] Threat assumptions and key abuse cases are listed.
- [ ] CI security gates are green (workflow validation, secret scan, dependency advisory review).
- [ ] Telemetry and KPI data sources are approved against a regional compliance baseline.
- [ ] Collection is aggregate-first and excludes unnecessary personal/regulated data by default.

## Final draft gate
- [ ] All high/critical security findings are remediated or formally accepted with justification.
- [ ] Branch protection requires security checks before merge.
- [ ] Access permissions were reviewed and reduced where possible.
- [ ] Tokens and credentials were rotated if scope changed.
- [ ] Security-relevant tests and checks are reproducible.
- [ ] Incident response owner and escalation path are documented.
- [ ] Risk acceptances are documented with owner, expiry, and compensating controls.
- [ ] Pipeline performance and failure trends are reviewed without weakening controls.
- [ ] Final readiness report and remediation backlog are published.
- [ ] Security control-path tests show no bypass path for required approval and validation gates.
- [ ] Stability and maintainability checks are completed for long-lived operation.

## Operating cadence gate
- [ ] A structured weekly update is published with status, risks, and mitigations.
- [ ] A monthly governance review is completed for access, dependencies, and policy drift.
- [ ] A quarterly Zero Trust posture recertification is completed and archived.
- [ ] Owners and approvers for security decisions are explicitly documented.
- [ ] Regional legal/control mapping is reviewed and updated when laws or market scope change.
