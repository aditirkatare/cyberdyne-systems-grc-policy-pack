# Identity, Password & Authentication Standard

| Document control | Value |
|---|---|
| Policy ID | CS-GRC-STD-02 |
| Owner | IT Administrator, with GRC oversight |
| Applies to | Workforce identities, privileged identities, and non-human/service identities |
| Issue date | September 2026 |
| Version / status | 1.0 / Portfolio draft; simulated approval required |
| Review cadence | At least annually and after significant identity-platform changes |
| Related documents | Acceptable Use Policy; Access Control Policy; Incident Reporting & Response Policy |

> **Portfolio status:** Proposed standard for a fictional company, not an implemented or audited control environment.

## 1. Purpose and scope

Define minimum requirements for authenticating users and services accessing Google Workspace, Slack, GitHub, AWS, company laptops, production systems, and other company-approved services. Authentication strength must be proportionate to the value of the account and the impact of compromise.

## 2. Identity lifecycle and account ownership

- Every workforce user must have a unique, individually attributable account. Shared human accounts are prohibited.
- Identity creation, role changes, suspension, recovery, and deletion must follow the Access Control Policy and be linked to an approved request or HR event.
- Company-managed identity services and organization-owned application tenants must be used where available. Personal identities must not own critical company repositories, cloud resources, or integrations.
- Non-human identities must have a named owner, a defined purpose, minimum permissions, documented credential storage, and a review date.

## 3. Multi-factor authentication

- MFA is mandatory for all workforce accounts in Google Workspace, Slack, GitHub, AWS, remote access, and other services that support it.
- Phishing-resistant MFA, such as FIDO2/WebAuthn security keys or passkeys, is required for privileged administrators and production-capable accounts where supported. If unavailable, use the strongest supported MFA method and document a time-bound remediation plan.
- SMS or voice one-time codes must not be the preferred method for privileged access. Their use requires documented justification where stronger methods are unavailable.
- MFA recovery methods must be protected to the same standard as the primary account. Recovery codes must be stored in an approved password manager or another approved secure location, never in source code or shared notes.
- MFA enrollment and recovery events should be logged. Unexpected MFA prompts, device enrollment notices, or authentication fatigue prompts must be reported as potential incidents.

## 4. Password and passphrase requirements

- Use a unique password or passphrase for every company account. Do not reuse personal passwords for business services.
- Use the company-approved password manager to generate and store passwords. Passwords must not be shared, emailed, pasted into tickets, or stored in plaintext files.
- Where a password is user-created, use a long password or passphrase; the system configuration should support at least 15 characters where passwords are the sole authentication factor and must not impose arbitrary complexity rules that encourage predictable substitutions. If MFA is always required, the company may configure a lower minimum only after a documented risk review and must still support long passwords.
- Block known-compromised or commonly used passwords where the identity provider supports this capability. Do not require routine calendar-based password changes solely as a ritual; require immediate change when compromise is suspected or confirmed, when a credential is exposed, or when a service provider mandates it for a documented reason.
- Password reset flows must verify the requester using approved recovery controls. Help-desk staff must never ask a user to reveal their current password or MFA code.

## 5. Privileged and high-impact accounts

- Separate everyday user activity from administrative activity where supported. Privileged identities must not be used for routine web browsing, email, or general collaboration.
- Grant administrative access to the minimum number of named personnel required to perform the function. Require documented approval from the system owner and IT Administrator.
- Use time-bound or just-in-time privilege elevation where technically feasible. Record the business purpose and retain relevant logs for privileged actions.
- Emergency or break-glass accounts must be tightly limited, protected by strong MFA, monitored, tested at least quarterly, and used only when normal administrative access is unavailable. Every use requires an incident or change record and post-use review within one business day.

## 6. Service accounts, API keys, and secrets

- Prefer short-lived credentials and workload identity over long-lived access keys wherever the platform supports them.
- Store secrets in an approved password manager or secrets manager with access limited to named maintainers. Do not hard-code secrets in repositories, images, build logs, environment files committed to version control, or tickets.
- Assign each service identity one documented owner and business purpose. Grant only permissions needed for its specific function; prohibit interactive login unless technically necessary and specifically approved.
- Review service identities and long-lived tokens at least quarterly. Rotate credentials on suspected exposure, ownership change, privilege change, or provider requirement. Where short-lived credentials are not available, document an expiry or rotation interval based on risk, with 180 days as the maximum default for static secrets absent an approved compensating design.
- Revoke tokens, keys, OAuth grants, SSH keys, and app passwords when no longer needed or when the owner leaves or changes roles. Secret exposure must be treated as a security incident, even if the secret is later deleted from the visible file.

## 7. Authentication logging and monitoring

The IT Administrator should enable available logging for sign-ins, MFA changes, password resets, failed login bursts, new OAuth grants, privileged actions, key creation, and account recovery. Alert thresholds should be tuned to reduce alert fatigue without suppressing meaningful high-risk behavior. Log access must be restricted and changes to logging configuration must be recorded.

## 8. Exceptions and enforcement

An exception must identify the affected service and users, the reason stronger authentication is unavailable, exposure duration, compensating measures, accountable owner, approval, and expiry. Exceptions involving privileged access require explicit executive sponsor acceptance if material residual risk remains after GRC review. Review all active exceptions at least monthly; each exception expires within 180 days unless re-approved.

## 9. Validation evidence

Expected evidence includes MFA-coverage exports, password-manager deployment records, privileged group membership, authentication configuration screenshots or exports, service-account inventory, secret-scanning results, exception approvals, and quarterly review tickets. Store evidence in an access-restricted company location and redact secrets and unnecessary personal data.

## 10. References

- [NIST SP 800-63B-4: Digital Identity Guidelines - Authentication and Authenticator Management](https://doi.org/10.6028/NIST.SP.800-63b-4)
- [NIST CSF 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1)
