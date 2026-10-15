# Cyberdyne Systems | Startup GRC Policy Pack

**Author:** Aditi Rajendra Katare  
**Project date:** September 2026  
**Project type:** Independent GRC portfolio simulation  
**Scenario:** Fictional 50-person SaaS startup

> **Important scope statement**  
> Cyberdyne Systems in this repository is a fictional case-study company. This project is a proposed policy design exercise only. No real company environment was accessed, audited, or secured. The documents are not approved corporate policy, legal advice, or proof of compliance with any framework or regulation.

## Project overview

This repository models the work a first GRC hire might do to establish a practical security-policy baseline at an early-stage SaaS company. The assumed environment uses Google Workspace, Slack, GitHub, AWS, and employee laptops. The pack focuses on policies and evidence that a small team could realistically own, review, and test.

### Included deliverables

| Deliverable | Purpose |
|---|---|
| 5 core policies / standards | Set minimum expectations for acceptable use, authentication, access lifecycle, data handling, and incident response. |
| NIST CSF 2.0 / CIS Controls v8.1 mapping | Show an indicative relationship between policy requirements and recognized control outcomes. This is not a formal compliance mapping. |
| Risk register | Prioritize illustrative risks using a 5×5 likelihood-impact model and proposed treatment plans. Residual scores are targets, not measured results. |
| Evidence register | Define what evidence could demonstrate operation, who owns it, and how often it should be collected. |
| Audit test plan | Specify repeatable sample-based checks with pass criteria and follow-up for failures. |
| 30/60/90-day roadmap | Turn written requirements into a phased implementation and validation plan. |
| RACI and operating model | Clarify role ownership for a small startup without assuming a full compliance department. |
| Reusable templates | Provide policy-exception, incident-intake, access-request, and access-review working forms. |
| Compiled policy pack | A formatted DOCX/PDF version of the five core policies is provided alongside the source Markdown. |

## Repository structure

```text
.
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── policies/
│   ├── 01-acceptable-use-policy.md
│   ├── 02-identity-password-authentication-standard.md
│   ├── 03-access-control-joiner-mover-leaver-policy.md
│   ├── 04-data-classification-and-handling-policy.md
│   └── 05-security-incident-reporting-and-response-policy.md
├── docs/
│   ├── audit-test-plan.md
│   ├── control-mapping.csv
│   ├── evidence-register.csv
│   ├── implementation-roadmap.md
│   ├── policy-exception-register-template.csv
│   ├── project-notes-and-assumptions.md
│   ├── resume-and-linkedin-summary.md
│   ├── risk-register.csv
│   └── roles-and-responsibilities.md
├── templates/
│   ├── access-request.md
│   ├── access-review-checklist.md
│   ├── incident-intake.md
│   └── policy-exception-request.md
└── deliverables/
    ├── Cyberdyne_Systems_GRC_Policy_Pack.docx
    ├── Cyberdyne_Systems_GRC_Policy_Pack.md
    └── Cyberdyne_Systems_GRC_Policy_Pack.pdf
```

## Framework alignment

The pack uses these references as design inputs:

- **NIST Cybersecurity Framework (CSF) 2.0:** provides outcome-oriented governance and cybersecurity functions. The policy set particularly touches Govern, Identify, Protect, Detect, Respond, and Recover.
- **CIS Critical Security Controls v8.1:** informs practical safeguards such as account management, access control, data protection, secure configuration, audit log management, awareness, and incident response.
- **NIST SP 800-63B-4:** informs authentication and authenticator-management design decisions.

The mapping is intentionally **indicative, not an assertion of certification, conformity, or compliance**. Mapping to a control family does not mean the control is implemented or effective. A real program would validate framework versions, contractual obligations, system architecture, data flows, and jurisdiction-specific privacy/security requirements.

## Key design choices

- **Least privilege and lifecycle control:** access requires business justification and independent approval, is reviewed on a set cadence, and is revoked through a defined offboarding process.
- **Risk-based authentication:** mandatory MFA, stronger methods for privileged identities where supported, password-manager use, and careful service-secret handling.
- **Usable data labels:** Public, Internal, Confidential, and Restricted classes with progressively stronger handling rules.
- **Fast incident reporting:** report suspicions and near misses promptly; responders distinguish verified facts from hypotheses and document evidence handling.
- **Evidence by design:** each major policy objective has potential evidence, an owner, cadence, and a test procedure.
- **Exceptions are temporary:** documented scope, risk, compensating controls, accountable approver, expiry, and periodic review.

## How to review or extend this project

1. Start with the five files under `policies/` and check whether each requirement is clear, assignable, and testable.
2. Review `docs/project-notes-and-assumptions.md` before applying the pack to a different organization or technical stack.
3. Follow `docs/implementation-roadmap.md` to plan configuration, communication, evidence collection, and validation.
4. Use `docs/control-mapping.csv` and `docs/evidence-register.csv` as living workbooks rather than one-time documents.
5. Use `docs/audit-test-plan.md` to test control design and, later, control operation. Record failures as findings with owners and due dates.
6. Replace the fictional contacts, targets, roles, and tooling assumptions with validated organizational details before real use.

## Suggested success measures for a future implementation

These are proposed targets for a hypothetical implementation, not current performance claims:

- 100% of active workforce accounts enrolled in MFA, with documented exceptions.
- 100% of privileged and production-capable access reviewed quarterly.
- All standard workforce access reviewed at least every six months.
- High-risk leaver access disabled at the effective termination time; standard leaver access disabled within the defined one-hour operational target.
- 100% of active exceptions have an owner, approver, compensating controls, and unexpired review date.
- At least one incident tabletop completed annually, with corrective actions assigned and tracked.

## Portfolio resume wording

> **Startup GRC Policy Pack | Independent Portfolio Project | September 2026**  
> Designed a simulated security-policy baseline for a fictional 50-person SaaS startup. Authored five core policies covering acceptable use, authentication, joiner-mover-leaver access, data classification, and incident response; developed an indicative NIST CSF 2.0 / CIS Controls v8.1 mapping, risk and evidence registers, an audit test plan, reusable GRC templates, and a 30/60/90-day implementation roadmap.

Describe this as a **policy-design / GRC portfolio simulation**, not as an implemented company-wide security program or a completed compliance audit.

## References

1. NIST, [The NIST Cybersecurity Framework (CSF) 2.0](https://doi.org/10.6028/NIST.CSWP.29), February 2024.
2. NIST, [SP 800-63B-4: Digital Identity Guidelines - Authentication and Authenticator Management](https://doi.org/10.6028/NIST.SP.800-63b-4), July 2025.
3. Center for Internet Security, [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1).
4. NIST, [SP 1299: CSF 2.0 Resource and Overview Guide](https://doi.org/10.6028/NIST.SP.1299), February 2024.

---

**Prepared by Aditi Rajendra Katare | September 2026**  
*Fictional case study. Draft for review. No implementation or independent validation is claimed.*
