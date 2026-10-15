# Security Incident Reporting & Response Policy

| Document control | Value |
|---|---|
| Policy ID | CS-GRC-POL-05 |
| Owner | Incident Response Lead (simulated role), with GRC coordination |
| Applies to | All workforce members, contractors, systems, cloud services, devices, and company/customer data |
| Issue date | September 2026 |
| Version / status | 1.0 / Portfolio draft; simulated approval required |
| Review cadence | At least annually; after significant incidents, tabletop exercises, or material system changes |
| Related documents | All policies in this pack; `templates/incident-intake.md` |

> **Portfolio status:** This is a proposed response policy and illustrative service target, not evidence that a staffed 24/7 response function exists. A real organization must confirm contacts, staffing, escalation paths, legal obligations, and provider capabilities before approval.

## 1. Purpose

Establish a consistent way to report, triage, investigate, contain, eradicate, recover from, and learn from suspected security incidents. Fast, good-faith reporting is more important than proving an incident before escalation.

## 2. What to report

Report immediately when you suspect or observe any of the following:

- A lost or stolen company laptop, phone, token, security key, or storage device.
- A phishing message, suspicious login prompt, unexpected MFA request, malware alert, or unusual account recovery event.
- Unauthorized account access, unexplained privilege changes, suspicious OAuth grants, exposed access keys, secrets in a repository, or unexpected administrator activity.
- Customer or company data sent to the wrong recipient, made publicly accessible, downloaded unexpectedly, or disclosed through an unapproved service.
- Unexpected production changes, unusual cloud behavior, service disruption that may be security-related, or evidence of tampering.
- A third-party security notification, vulnerability exploitation, suspected insider misuse, or any event that could affect confidentiality, integrity, or availability.

Near misses and mistaken clicks should also be reported. Staff must not delay a report while trying to investigate independently.

## 3. How to report

Use the company Slack channel `#security-incident` or email `security@cyberdyne.example`. For a suspected active compromise, use the fastest available route to contact the Incident Response Lead or IT Administrator as well. If Slack or email may be compromised or unavailable, use a separately verified contact path established during implementation.

Include, if known: reporter and safe contact method; time first noticed and time zone; affected account/device/system; what happened; relevant message, alert, ticket, or log location; potential data affected; actions already taken; and whether the activity is continuing. Do not include passwords, MFA codes, private keys, access tokens, unnecessary personal data, or full copies of sensitive records in the initial message. Use a secure evidence location and share access with responders only.

## 4. Severity and initial response targets

These are proposed internal planning targets for the simulated 50-person company, not contractual SLAs or guarantees. The Incident Response Lead must validate staffing and tool coverage before these targets are adopted.

| Severity | Illustrative trigger | Acknowledgement / triage target | Minimum response expectation |
|---|---|---|---|
| **SEV-1 Critical** | Confirmed or strongly suspected production compromise, active unauthorized access to Restricted/customer data, broad credential compromise, destructive activity, or material service outage caused by malicious activity. | Acknowledge within 15 minutes during the designated on-call coverage period; immediately escalate to the executive sponsor and relevant system owner. | Assign an incident commander, establish a timeline, preserve evidence, prioritize containment, and assess customer/legal notification needs. If 24/7 coverage is not staffed, document the real coverage gap and escalation arrangement. |
| **SEV-2 High** | Compromised privileged account, active malware on a device with sensitive access, unauthorized repository/cloud access, or credible suspected data exfiltration without confirmed broad impact. | Acknowledge within 1 hour during staffed coverage. | Assign an owner, investigate scope, implement proportionate containment, and provide regular updates to affected stakeholders. |
| **SEV-3 Moderate** | Suspicious activity requiring investigation but with no confirmed material compromise, a limited policy breach, or an isolated endpoint alert. | Acknowledge within 1 business day. | Triage, gather evidence, decide whether escalation is needed, and document closure or further action. |
| **SEV-4 Low / Informational** | Benign security question, near miss, blocked event, or low-risk weakness that does not require incident command. | Acknowledge within 3 business days. | Record, route to the appropriate owner, and use for awareness or backlog improvement as appropriate. |

Any responder may raise severity when new evidence increases potential impact. Reduce severity only with a documented rationale from the Incident Response Lead. Applicable legal, regulatory, contractual, cyber-insurance, or law-enforcement deadlines supersede these internal targets.

## 5. Response lifecycle

### 5.1 Record and triage

Create an incident record with a unique ID, timestamps in UTC where practical, reporter, affected assets, severity, assigned incident commander, initial facts, open questions, and links to evidence. Separate verified facts from assumptions or hypotheses. Record source and time of each significant observation.

### 5.2 Contain

Choose containment that reduces harm while protecting evidence and business continuity. Examples include disabling a compromised identity, revoking sessions and tokens, isolating an endpoint, restricting a public repository or storage bucket, applying a cloud permission block, or temporarily disabling an integration. Where feasible, record who authorized and performed each action, the time, expected side effects, and result. Do not perform actions outside your authority; escalate when a high-impact change is required.

### 5.3 Preserve evidence

Preserve relevant logs, alerts, messages, file hashes, access records, cloud audit events, and device details. Use read-only exports or approved acquisition procedures where feasible. Maintain a simple chain-of-custody record for evidence intended for legal, disciplinary, contractual, or forensic use: evidence ID, description, source, collector, collection time, method/tool and version if known, hash where appropriate, storage location, access/transfers, and integrity verification. Restrict access to evidence; do not circulate sensitive artifacts in general chat.

Do not wipe, reimage, delete, or power off a potentially compromised device unless an authorized responder determines that action is necessary to contain active harm or protect people. Do not run unapproved tools or conduct invasive investigation without authorization.

### 5.4 Eradicate and recover

Remove the cause where understood, rotate/revoke exposed credentials, remediate exploited weaknesses, rebuild or restore affected systems using trusted procedures, and validate that access controls and monitoring are functioning before returning a system to normal operation. The system owner approves service restoration with the Incident Response Lead. Record residual risk and any temporary compensating controls.

### 5.5 Communicate and close

The Incident Response Lead coordinates status updates with the executive sponsor, IT, affected system/data owners, People Ops, and legal/privacy counsel when available and appropriate. Only an authorized spokesperson may make external customer, regulator, press, or public statements. Do not speculate or make commitments beyond verified facts. Legal/privacy counsel and responsible business leaders determine whether and when notifications are required under applicable law and contracts.

Close the incident record only when scope and impact have been documented to a reasonable level, containment and recovery actions have owners and status, required notifications have been assessed, evidence is preserved, and follow-up tasks are assigned. Material incidents require a lessons-learned review within 10 business days of containment, unless the Incident Response Lead documents why more time is needed.

## 6. Roles and decision authority

- **Reporter:** reports quickly, preserves context, and avoids unauthorized investigation.
- **Incident Response Lead / Incident Commander:** owns triage, severity, coordination, timeline, containment recommendations, and closure readiness.
- **IT Administrator / system owner:** executes approved technical actions and validates recovery.
- **GRC Lead:** maintains process documentation, evidence tracking, risk register updates, policy exceptions, metrics, and corrective actions.
- **Executive sponsor:** makes material business-risk decisions and provides resources; accepts residual risk only where authorized.
- **Legal/privacy counsel and authorized communications lead:** assess legal/contractual notifications and approve external messaging in coordination with business leadership.
- **People Ops:** supports employee communications and HR processes as appropriate.

## 7. Retaliation, confidentiality, and reporting hygiene

Good-faith reporting is encouraged even when an employee has clicked a link or made a mistake. Retaliation for raising a security concern is prohibited. Incident details must be shared only with people who need them to respond. Do not post incident evidence publicly or discuss customer-impact claims outside the authorized response group.

## 8. Testing and continuous improvement

At least annually, conduct a tabletop exercise covering a realistic scenario such as compromised Google Workspace credentials, leaked GitHub token, exposed AWS storage, or lost laptop with a valid session. Record participants, scenario, decisions, timing, gaps, owner, and due date. Track lessons learned and repeat tests after major changes. Review incident metrics quarterly, including time to acknowledge, time to contain, incidents by root cause, recurring vulnerabilities, reporting delays, and overdue corrective actions.

## 9. References

- [NIST CSF 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1)
- [NIST SP 800-63B-4](https://doi.org/10.6028/NIST.SP.800-63b-4) for identity-related incident context
