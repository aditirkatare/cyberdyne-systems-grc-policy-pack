# 30/60/90-Day Implementation Roadmap

**Clock starts only after real executive approval.** The phases below are a proposed sequencing plan for the fictional 50-person SaaS scenario, not a record of completed work.

## Days 0-30: Establish ownership and minimum viable controls

### Governance and discovery
- Name policy owners, system owners, data owners, an executive risk approver, and an incident response lead.
- Confirm business services, systems, data flows, critical assets, existing commitments, and applicable legal/contractual obligations.
- Review and approve the five policies, then publish a versioned policy register with owner, approval date, and next review date.
- Create the risk acceptance and policy exception workflow, including expiry and review requirements.

### Fast baseline
- Export workforce accounts, privileged groups, cloud accounts, GitHub organization roles, Slack admin roles, and service identities.
- Enforce MFA across supported core services; prioritize phishing-resistant MFA for privileged accounts.
- Confirm endpoint inventory, disk encryption, endpoint protection, OS update status, and device-lock settings.
- Establish the incident channel, alternate contact path, initial severity definitions, and escalation roster.

### Exit evidence
- Approved policy register and ownership matrix.
- Baseline access inventory and MFA coverage report.
- Endpoint coverage report with remediation tickets.
- Incident contact card and a completed incident-intake dry run.

## Days 31-60: Operationalize and collect evidence

- Move role-based application access into approved groups; identify and remove stale users, personal-owned critical assets, dormant tokens, and unnecessary admin grants.
- Launch documented joiner/mover/leaver tickets and validate the offboarding sequence in a controlled test account.
- Classify high-value datasets, confirm approved storage locations, review external sharing, and remove unnecessary public links.
- Set security logging requirements for authentication, admin changes, GitHub, AWS, and endpoint alerts based on platform capability.
- Configure secret scanning and remediation workflow where available; document where scanning coverage is absent.
- Train staff on phishing reporting, sensitive-data handling, and safe use of approved tools. Collect acknowledgements.
- Start evidence collection with owner, cadence, location, access restriction, and retention notes.

### Exit evidence
- Sampled access requests with approvals and provisioning completion.
- Test leaver ticket with revocation evidence.
- First privileged access review with action closure.
- Data inventory/classification sample and external-sharing review.
- Security-log source inventory and training completion report.

## Days 61-90: Test, remediate, and report

- Execute the audit test plan and record pass/fail/partial results with evidence references.
- Run a tabletop exercise for compromised cloud credentials or exposed repository token; record decisions and communication gaps.
- Re-score risks based on actual evidence; do not reuse target residual scores without validating controls.
- Review exceptions and overdue remediation items with accountable owners.
- Present a concise GRC status update: critical/high risks, MFA coverage, access-review completion, leaver timing, endpoint gaps, incident response readiness, and overdue actions.
- Agree the next-quarter control improvement backlog and policy-review schedule.

### Exit evidence
- Completed test log and remediation tracker.
- Tabletop exercise report with assigned corrective actions.
- Updated risk register grounded in implementation evidence.
- Management review notes and next-quarter priorities.

## Suggested operating metrics

| Metric | Proposed target | Cadence | Owner |
|---|---:|---|---|
| Active workforce MFA coverage | 100%, with documented exceptions | Monthly | IT Administrator |
| Privileged-access reviews completed | 100% each quarter | Quarterly | System owners / IT |
| Standard access reviews completed | 100% each half-year | Semiannual | Managers / system owners |
| High-risk leaver disablement | At effective time for involuntary/high-risk cases | Per leaver; monthly roll-up | People Ops + IT |
| Standard leaver access disablement | Within 1 hour of effective termination | Per leaver; monthly roll-up | People Ops + IT |
| Active policy exceptions with current approval and expiry | 100% | Monthly | GRC Lead |
| Critical audit findings past due | 0 without documented risk acceptance | Monthly | GRC Lead + owner |
| Incident tabletop | At least one annually | Annual | Incident Response Lead |

Metrics should report denominator, exclusions, evidence source, reporting period, and owner. A green percentage without a complete population can be misleading.
