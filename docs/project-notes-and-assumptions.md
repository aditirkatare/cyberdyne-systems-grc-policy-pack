# Project Notes, Assumptions & Limitations

## Scenario assumptions

- Cyberdyne Systems is fictional and is used only as a case-study name.
- The modeled organization has approximately 50 employees and delivers a SaaS product.
- The assumed core environment includes Google Workspace, Slack, GitHub, AWS, and employee laptops. Actual products, licenses, identity federation, centralized logging, endpoint management, and security staffing have not been validated.
- A GRC Lead, IT Administrator, Incident Response Lead, executive sponsor, People Ops contact, system owners, and data owners are modeled roles. At a small startup, one person may hold more than one role, but approvals for high-risk access should still be independent where feasible.
- `security@cyberdyne.example` and `#security-incident` are illustrative contact routes. They must not be treated as real contact channels.
- Proposed effective dates and response targets are design assumptions only.

## Risk scoring method

Likelihood and impact each use a 1-5 scale. Score = likelihood × impact. Bands are 1-4 Low, 5-9 Moderate, 10-14 High, 15-19 Very High, and 20-25 Critical. These bands help rank the case-study risks and are not derived from a mandatory external standard. The register's residual scores represent a proposed target state after planned treatment, not observed effectiveness. Real residual risk must be reassessed after control implementation and evidence-based testing.

## Mapping method

Policy requirements are mapped to high-level categories in NIST CSF 2.0 and control areas in CIS Controls v8.1 based on their subject matter. This is an informal cross-reference intended to guide review. It is not a complete framework assessment, official mapping, certification, attestation, or legal compliance determination. Verify the exact wording and applicability of each cited reference for a real organization.

## Assumptions requiring validation before operational use

1. Applicable countries, privacy/data-protection laws, breach-notification rules, employment rules, and sector-specific obligations.
2. Customer contracts, DPAs, security schedules, cyber-insurance conditions, and external commitments.
3. Actual system architecture, SSO/SCIM availability, MFA capabilities, device management, logging retention, backup/restore, secrets management, and cloud guardrails.
4. On-call staffing, incident response coverage, alternate communication route, escalation contacts, and authority to isolate systems.
5. Data inventory, data residency, retention/deletion requirements, and customer-data classification rules.
6. HR offboarding workflow and timing, device-return logistics, vendor access, and records preservation requirements.
7. Approval authority, risk tolerance, evidence retention, and the organization's risk acceptance process.

## Out of scope for this first policy pack

This pack does not constitute a complete ISMS, risk assessment of a real environment, Business Continuity/Disaster Recovery Plan, Secure SDLC standard, vulnerability-management standard, supplier-risk program, privacy notice, data-processing agreement, backup standard, cryptographic key-management standard, business impact analysis, penetration test, SOC 2 report, ISO 27001 certification, or regulatory compliance audit. These would be sensible follow-on deliverables based on business context.

## Quality principle

A policy is only one part of a control. For credible implementation, pair each requirement with configuration, an accountable owner, operational procedure, evidence, a test, and corrective action when it fails.
