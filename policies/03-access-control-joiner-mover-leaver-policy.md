# Access Control & Joiner-Mover-Leaver Policy

| Document control | Value |
|---|---|
| Policy ID | CS-GRC-POL-03 |
| Owner | IT Administrator, with GRC oversight |
| Applies to | Workforce users, contractors, vendors, administrators, and service identities |
| Issue date | September 2026 |
| Version / status | 1.0 / Portfolio draft; simulated approval required |
| Review cadence | At least annually; access reviews at the cadences below |
| Related documents | Identity, Password & Authentication Standard; Data Classification & Handling Policy; Incident Reporting & Response Policy |

> **Portfolio status:** Proposed policy for a fictional 50-person SaaS company. Approval and actual technical implementation have not occurred.

## 1. Purpose

Ensure access to applications, repositories, cloud environments, customer data, and corporate devices is authorized, appropriate to a person's role, time-bound where possible, and removed promptly when no longer required.

## 2. Core principles

- **Least privilege:** grant only the minimum access required for assigned duties.
- **Need to know:** access to Confidential and Restricted information requires a defined business need.
- **Named accountability:** each human account must map to one person; shared human accounts are prohibited.
- **Approval before access:** the request and approval must be recorded before routine access is provisioned.
- **Separation of duties:** requesters must not approve their own access. High-impact access requires a system owner or delegated approver independent of the requester.
- **Time-bounded access:** contractor, vendor, incident-response, and temporary project access must have an expiry date.

## 3. Access request and provisioning

1. The manager or accountable sponsor submits an access request using `templates/access-request.md` or the company's ticket system.
2. The request states the user's identity, role, business justification, systems/groups/permissions, data sensitivity, start date, expiry date (if temporary), and manager or sponsor.
3. The system owner approves the requested level of access. Requests for AWS production, customer-data export, organization-owner privileges, repository administration, or other high-impact permissions also require IT Administrator review.
4. IT provisions access through organization-managed identities and groups, records completion, and links the request to the approved role or group.
5. The requester and manager are notified. Access is not considered approved merely because it was technically possible to grant.

Routine access should be provisioned within two business days after a complete approval. Production or administrative access must be individually attributable and should use separate privileged accounts where supported. Emergency access may be granted under the break-glass process, but must be recorded and reviewed by the next business day.

## 4. Joiners

People Ops must notify IT and the hiring manager before the user's start date. Access is provisioned only after an authorized start is confirmed and required onboarding checks are complete. The baseline should include a unique company identity, mandatory MFA, approved password manager access, least-privilege collaboration access, device-management enrollment, endpoint protection, and policy/security-training acknowledgement. Production access is not part of the default onboarding bundle.

## 5. Movers and role changes

Managers must submit role changes before or promptly when responsibilities change. IT must compare new permissions to existing permissions, remove access no longer needed, and grant new access only after required approval. Do not accumulate permissions as a user moves between roles. Temporary project privileges must expire automatically where supported or be tracked with a specific review date.

## 6. Leavers and urgent termination

People Ops or the authorized manager must notify IT of a termination or contract end as soon as the timing is confirmed. At the effective termination time, IT must disable interactive sign-in for company identities and revoke active sessions where supported. The operational target is to complete disabling the primary identity, privileged access, VPN/remote access, and access to Google Workspace, Slack, GitHub, and AWS within 1 hour of the effective time; for involuntary or high-risk departures, coordinate a synchronized disablement at the effective time. Where a tool cannot be disabled centrally, remove access directly and record the result.

The offboarding checklist must also cover: revocation of MFA authenticators and recovery options; removal of group memberships and app assignments; revocation of tokens, app passwords, OAuth grants, SSH keys, cloud access keys and personal access tokens; transfer of repository, document, calendar, and service ownership; recovery of company devices and badges; preservation of business records; and confirmation from relevant system owners. Do not delete the person's work product or logs as a substitute for transferring ownership.

## 7. Access reviews

- Review privileged access, AWS production access, organization-owner/admin roles, customer-data export permissions, and break-glass accounts at least quarterly.
- Review all other workforce access at least every six months.
- Review contractor/vendor access monthly and at the end of the engagement.
- The reviewer must be the manager or system/data owner, not the sole subject of the review. The reviewer records each account as retain, modify, or revoke with rationale and completion date.
- IT tracks removals and modifications to completion, with a target of five business days for standard review actions and immediate handling for clearly unauthorized or high-risk access.
- Evidence must include the population reviewed, reviewer, review date, decisions, exceptions, and closure tickets. A screenshot of a few accounts without a population/export is insufficient evidence of a complete review.

## 8. Vendors and third parties

Third-party access requires a named internal sponsor, an approved business purpose, minimum permissions, MFA where supported, contractual confidentiality/security terms appropriate to the engagement, and a defined expiry date. Prefer separate accounts or federated access. Vendors must not share accounts or retain access after the engagement ends. Access to customer or Restricted data requires data-owner approval and a documented purpose.

## 9. Service and automation identities

Each service identity must have an owner, function, approved permissions, secure credential storage, rotation/revocation plan, and review cadence. Service identities must not be used as substitutes for human attribution. Remove obsolete identities and disable unused keys or tokens. See the Identity, Password & Authentication Standard for credential requirements.

## 10. Exceptions, evidence, and review

Exceptions follow the policy-exception process. They must specify the identity, access, systems, reason, compensating controls, accountable risk owner, approval, and expiry. Access-control evidence must be protected from broad access and retained under the company's records schedule; the project default is at least 12 months unless law, contract, incident preservation, or an approved schedule requires otherwise.

At least annually, the GRC Lead should analyze access-review completion, late offboarding actions, stale accounts, privilege accumulation, and overdue exceptions. Recurring failures require a tracked corrective-action plan.

## 11. References

- [NIST CSF 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1)
