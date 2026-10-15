# Data Classification & Handling Policy

| Document control | Value |
|---|---|
| Policy ID | CS-GRC-POL-04 |
| Owner | GRC Lead; individual data owners remain accountable for assigned datasets |
| Applies to | All company, customer, workforce, product, and operational information handled by the company |
| Issue date | September 2026 |
| Version / status | 1.0 / Portfolio draft; simulated approval required |
| Review cadence | At least annually and when data uses or obligations materially change |
| Related documents | Acceptable Use Policy; Access Control Policy; Incident Reporting & Response Policy |

> **Portfolio status:** Classification categories and handling rules are proposed for a fictional company. They are not a legal classification scheme and do not establish compliance with any specific privacy regulation.

## 1. Purpose

Provide a consistent way to classify information by sensitivity and define how it may be collected, accessed, stored, shared, transmitted, retained, and disposed of. Classification should guide controls without implying that labels alone make data secure.

## 2. Roles and default classification

The data owner assigns or confirms a classification, approves permitted uses and sharing, and sets retention based on business needs, customer contracts, and applicable obligations. Anyone creating or receiving information must protect it according to its known classification. If uncertain, treat information as Confidential until the data owner clarifies it. Customer production data defaults to Confidential; authentication secrets, private keys, and high-impact production credentials are Restricted.

## 3. Classification levels

| Class | Definition and examples | Minimum handling |
|---|---|---|
| **Public** | Information approved for unrestricted public release, such as published marketing material or public documentation. | The data owner or Communications approver must authorize publication. Confirm the material contains no secrets, personal data, customer content, internal URLs, or other embedded sensitive information. |
| **Internal** | Routine company information not intended for public release, such as internal meeting notes, general procedures, non-sensitive project plans, and workforce announcements. | Store in approved company systems. Share with workforce members who need it. External sharing requires an accountable business owner and a legitimate purpose. |
| **Confidential** | Information whose unauthorized disclosure could harm customers, employees, or the company, such as customer contact details, non-public business plans, contracts, support tickets, non-public source code, and ordinary production logs that may contain identifiers. | Limit access by role and need to know. Use approved company storage and encrypted transmission. External sharing requires data-owner approval, recipient verification, least-privilege access, and expiry where supported. Avoid local copies and use masking for testing where feasible. |
| **Restricted** | Highest-sensitivity information whose disclosure or alteration could create serious harm, including passwords, MFA recovery codes, private keys, secrets, sensitive authentication material, production credentials, and high-impact customer datasets or exports designated by the data owner. | Access only to explicitly authorized personnel. Store in an approved secrets manager or approved restricted-access repository. Encrypt in transit and at rest. Log privileged access where technically feasible. Do not place in public or personal services, source code, general chat, public issue trackers, or unapproved AI tools. External transfer requires documented business need, data-owner approval, recipient validation, and approved secure transfer method. |

Classification is based on sensitivity and potential impact, not merely file format or storage location. Datasets may contain information in multiple classes; apply the highest relevant classification unless fields are reliably segregated and the data owner approves a different treatment.

## 4. Collection, storage, and access

- Collect and retain only information required for a defined business purpose. Data owners should review unnecessary collection and long-lived copies.
- Store company information only in approved organization-managed Google Workspace, Slack, GitHub, AWS, or other services approved for the relevant data class.
- Access must follow the Access Control Policy. Grant data access by named role or group, avoid broad links and public buckets, and review access when a user's role changes.
- Encrypt Confidential and Restricted information in transit using current secure transport protocols supported by the platform. Use provider or platform encryption at rest as a baseline; Restricted data must use approved secrets management or storage controls appropriate to its risk.
- Do not copy production customer data into development, demonstration, training, or personal environments unless a data owner approves a documented need and suitable minimization, masking, access restriction, and deletion plan.
- Before uploading data to a repository, issue tracker, chat, analytics tool, or AI service, confirm the destination is approved for that classification.

## 5. Sharing and transfer

Before external sharing, the sender must verify the recipient's identity and authority, confirm business need, select the minimum necessary dataset, use an approved transfer method, and set access restrictions or expiry dates where supported. The data owner approves external sharing of Confidential and all Restricted data. Public links, anonymous downloads, personal email, consumer file-sharing, and unapproved external AI tools are prohibited for Confidential and Restricted information.

For exports, include the purpose, requesting party, approving data owner, fields included, transfer method, recipient, and planned deletion/retention date in the ticket or record. Use redaction, aggregation, synthetic data, or pseudonymization when it meets the task's needs. Pseudonymized information may remain personal or sensitive data under applicable law and must not automatically be treated as anonymous.

## 6. Retention and secure disposal

Each data owner must document retention and deletion requirements based on business use, customer commitments, and applicable legal obligations. When no specific schedule has been approved, the owner must avoid indefinite retention and propose a schedule for GRC review. Deletion must cover active copies and, where feasible, replicas and exports under the company's control. Backups may age out under the approved backup schedule; do not promise immediate physical erasure from immutable backups unless the technical design supports it. Devices and media must be securely wiped or destroyed before reuse, return, or disposal using a method appropriate to the media and data sensitivity.

## 7. Data incidents

Accidental disclosure, wrong-recipient sharing, public repository exposure, lost media, suspicious downloads, suspected exfiltration, and unauthorized access must be reported immediately under the Incident Reporting & Response Policy. Do not silently delete, overwrite, or alter the only evidence of the event. Preserve context and share the location of the exposure with authorized responders without redistributing the sensitive content.

## 8. Review and evidence

Evidence may include a data inventory, approved classifications, repository visibility settings, external sharing logs, storage policies, access-control exports, retention/deletion records, and approved data-transfer tickets. GRC should sample high-risk datasets and review externally shared Confidential/Restricted data at least quarterly, where platform evidence supports the review.

## 9. References

- [NIST CSF 2.0](https://doi.org/10.6028/NIST.CSWP.29)
- [CIS Critical Security Controls v8.1](https://www.cisecurity.org/controls/v8-1)
