# Acceptable Use Policy

| Document control | Value |
|---|---|
| Policy ID | CS-GRC-POL-01 |
| Owner | GRC Lead (simulated role) |
| Applies to | Employees, contractors, interns, and approved third parties |
| Issue date | September 2026 |
| Version / status | 1.0 / Portfolio draft; simulated approval required |
| Review cadence | At least annually and after a material incident or technology change |
| Related documents | Identity & Authentication Standard; Access Control Policy; Data Classification & Handling Policy; Incident Reporting & Response Policy |

> **Portfolio status:** This is a proposed policy for a fictional company. It has not been approved, implemented, or tested in a real Cyberdyne Systems environment. It must be reviewed against applicable law, contracts, and actual business requirements before operational use.

## 1. Purpose

Set clear, risk-based rules for the responsible use of Cyberdyne Systems information, systems, networks, cloud services, collaboration tools, and endpoint devices. The goal is to reduce preventable security incidents while enabling legitimate work.

## 2. Scope

This policy applies to all people who access Cyberdyne Systems systems or information, and to all company-managed or company-authorized devices, identities, applications, networks, repositories, cloud accounts, and storage locations. The assumed environment for this portfolio scenario is a 50-person SaaS startup using Google Workspace, Slack, GitHub, AWS, and employee laptops.

## 3. Policy requirements

### 3.1 Authorized use and accountability

- Use company accounts and services for authorized business purposes. Limited personal use is permitted only when lawful, reasonable, does not disrupt work, and does not create material cost, security, or reputational risk.
- Protect company credentials, customer information, source code, infrastructure details, and business records from unauthorized access or disclosure.
- Complete assigned security awareness training and acknowledge this policy at onboarding and after material revisions.
- Follow the stricter requirement where this policy conflicts with a contract, an approved security standard, or applicable law. Escalate uncertainty to the GRC Lead rather than guessing.

### 3.2 Devices and endpoint security

- Use company-managed laptops for company data and privileged work unless an exception has been approved in writing.
- Keep operating systems, browsers, endpoint protection, and business applications supported and updated. As an operational target, remediate actively exploited or critical vulnerabilities within 72 hours where feasible, other critical vulnerabilities within 7 calendar days, high-risk vulnerabilities within 14 calendar days, and routine updates within 30 calendar days. The IT Administrator must document risk-based deviations and compensating measures.
- Enable full-disk encryption, automatic screen lock after no more than 10 minutes of inactivity, and supported endpoint protection on company-managed laptops.
- Lock the screen when leaving a device unattended. Do not disable security agents, disk encryption, logging, device management, or endpoint controls without written authorization.
- Report lost, stolen, tampered-with, or unexpectedly accessed devices immediately through the incident reporting process.

### 3.3 Internet, email, and collaboration tools

- Treat unexpected attachments, login prompts, QR codes, file-sharing invitations, OAuth permission requests, and urgent payment or credential requests as potential phishing until verified.
- Do not use personal email, personal cloud storage, consumer messaging accounts, or unapproved file-transfer services to store or transmit company information.
- Share files through approved company services with named recipients, least-privilege permissions, and expiry dates where supported. Avoid public links; use them only with documented approval and a time-bound business justification.
- Do not send passwords, API keys, private keys, recovery codes, session cookies, or other secrets in Slack messages, tickets, email, source code, or documents. Use approved secret-management channels.

### 3.4 Software, source code, and cloud services

- Install software only from trusted sources and only where permitted by the device-management and software-approval process.
- Use approved repositories and organization-managed accounts for source code. Do not publish proprietary source code, customer data, secrets, internal architecture, or vulnerability details in public repositories without explicit authorization.
- Do not create personal cloud accounts, shadow IT services, personal access tokens, cloud access keys, integrations, bots, or OAuth applications for business use without approval from the system owner or IT Administrator.
- Never disable branch protection, required reviews, logging, MFA, or cloud security controls to bypass a workflow. Raise a change request when a control blocks a legitimate task.
- Use production environments only for assigned duties. Production data must not be copied to local test systems or development environments unless the data owner approves an appropriate minimization or masking plan.

### 3.5 AI tools and external services

- Do not submit Confidential or Restricted information, customer data, source code, credentials, security findings, or non-public business information to public AI assistants or external services unless the service has been approved for that data class and the data owner has authorized the use.
- Verify generated content before using it for security, legal, customer, or operational decisions. AI output does not replace a required human review.
- Do not use company resources for unlawful activity, harassment, unauthorized surveillance, cryptocurrency mining, testing systems without authorization, or attempts to evade monitoring or access restrictions.

### 3.6 Remote work and travel

- Use trusted networks. Avoid conducting privileged administration over public Wi-Fi unless a company-approved secure connection is used.
- Prevent shoulder-surfing and unauthorized viewing of screens or printed materials. Keep devices in personal possession while travelling and do not leave them unattended in vehicles or public spaces.
- Report border searches, device seizure, suspected tampering, or unusual authentication prompts to IT and the GRC Lead promptly where lawful and safe to do so.
- Personal devices may access company resources only through an approved, documented BYOD exception with appropriate authentication, access restrictions, and separation of company data.

### 3.7 Monitoring and privacy

Company systems may log authentication, administrative actions, security events, device posture, network activity, and use of company services for security, support, compliance, and incident investigation. Monitoring must be proportionate to the stated business purpose, access to logs must be restricted, and any employee notice or consultation required by applicable law must be completed before monitoring begins. This policy does not authorize indiscriminate access to personal accounts or personal content.

## 4. Responsibilities

- **All users:** follow this policy, protect data and credentials, complete training, and report suspected incidents promptly.
- **Managers:** ensure staff understand applicable requirements and request access only for a justified business need.
- **IT Administrator:** maintain endpoint and identity baselines, document deviations, and disable unauthorized configurations where appropriate.
- **GRC Lead:** own the policy, track acknowledgements and exceptions, and coordinate periodic review.
- **Data owners:** approve external sharing and use of sensitive information where this policy requires owner approval.

## 5. Reporting, exceptions, and violations

Suspected phishing, malware, data exposure, lost devices, unauthorized access, accidental disclosure, or policy bypass must be reported immediately using `#security-incident` in the company Slack workspace or `security@cyberdyne.example`. Do not put passwords, tokens, or unredacted sensitive data in the initial report. Follow the Incident Reporting & Response Policy.

Exceptions require a documented business reason, affected systems/data, risk assessment, compensating controls, accountable owner, expiry date, and approval by the system owner plus the GRC Lead. Exceptions expire after 180 days at most unless re-approved. No exception can override applicable law or a binding customer/contractual obligation. See `templates/policy-exception-request.md`.

Violations may result in access restriction, retraining, formal HR action, or contract remedies, subject to applicable law and company procedures. Good-faith reporting is encouraged and retaliation for raising a concern is prohibited.

## 6. Compliance checks and review

At least quarterly, the IT Administrator should review endpoint-management coverage, encryption status, endpoint-protection status, and overdue critical updates. At least annually, the GRC Lead should review training completion, policy acknowledgements, incident trends, exception records, and changes in the technology stack. Findings must be tracked to closure with an owner and due date.

## 7. References

- [NIST Cybersecurity Framework (CSF) 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1)
