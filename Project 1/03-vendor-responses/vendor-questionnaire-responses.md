# Vendor Questionnaire Responses

**Vendor:** CloudVault Data Solutions
**Completed By:** J. Ramirez, Director of Security & Compliance 
**Date Returned:** 2026-02-20
**Evidence Reference:** See `04-vendor-evidence/evidence-log.md` for corresponding artifact IDs

---

## A. Organizational & Governance (GOV)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-GOV-01 | Yes. Information Security Policy last approved by the Board Risk Committee on 2025-11-10; reviewed annually. | EVD-GOV-01 |
| Q-GOV-02 | Yes. CloudVault has a full-time CISO (reporting to the COO) in place since 2022. | EVD-GOV-02 |
| Q-GOV-03 | Yes. SOC 2 Type II report issued 2025-09-30, covering the period 2024-10-01 to 2025-09-30, scope: Security and Availability Trust Services Criteria. | EVD-GOV-03 |
| Q-GOV-04 | Yes. $5M cyber liability coverage via Chubb, policy renews annually. | EVD-GOV-04 |
| Q-GOV-05 | Yes. Annual security awareness training (98% completion FY2025) plus quarterly phishing simulations. | EVD-GOV-05 |

## B. Data Security & Encryption (DS)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-DS-01 | Yes. AES-256 encryption at rest for all customer data stores. | EVD-DS-01 |
| Q-DS-02 | Yes. TLS 1.2 and TLS 1.3 supported; TLS 1.0/1.1 disabled as of 2024. | EVD-DS-02 |
| Q-DS-03 | Not currently supported. Customer-managed keys (BYOK) are on the 2026 Q4 product roadmap but not yet available. | EVD-DS-03 |
| Q-DS-04 | Logical segregation via tenant-scoped database schemas; no dedicated single-tenant option offered at current contract tier. | EVD-DS-04 |
| Q-DS-05 | Data is soft-deleted for 30 days post-termination, then permanently purged from primary and backup systems within 90 days total. | EVD-DS-05 |
| Q-DS-06 | Partial. DLP is implemented for outbound email only via a third-party gateway; not yet implemented for the SaaS application layer itself. | EVD-DS-06 |

## C. Access Control & Identity Management (AC)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-AC-01 | Yes. MFA is enforced for 100% of administrative and privileged accounts via Okta. | EVD-AC-01 |
| Q-AC-02 | Partial. MFA is available and defaulted on for new tenants, but is **optional/customer-configurable** for existing end-user accounts — approximately 78% adoption org-wide per last internal audit. | EVD-AC-02 |
| Q-AC-03 | Yes. RBAC model with 4 defined roles (Admin, Manager, Standard User, Read-Only); least privilege enforced by default role assignment. | EVD-AC-03 |
| Q-AC-04 | Quarterly access recertification for privileged/admin accounts; annual for standard user accounts. | EVD-AC-04 |
| Q-AC-05 | Access is revoked within 24 hours of termination per internal SLA; automated via HRIS-to-Okta integration for 90% of accounts, manual process for remaining legacy accounts. | EVD-AC-05 |
| Q-AC-06 | Yes. SAML 2.0 and OIDC SSO supported with major IdPs (Okta, Azure AD, Google Workspace). | EVD-AC-06 |

## D. Network & Infrastructure Security (NET)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-NET-01 | Yes. VPC segmentation isolates production, staging, and corporate networks; documented in network architecture diagram. | EVD-NET-01 |
| Q-NET-02 | Yes. Automated vulnerability scanning runs weekly via Qualys against all production assets. | EVD-NET-02 |
| Q-NET-03 | Yes, annually. Most recent penetration test conducted **2024-11-15** (approx. 15 months ago at time of this assessment). | EVD-NET-03 |
| Q-NET-04 | Yes. AWS GuardDuty deployed across all production accounts for IDS/threat detection. | EVD-NET-04 |
| Q-NET-05 | Hosted on AWS, primary region us-east-1, with disaster recovery in us-west-2. | EVD-NET-05 |

## E. Application Security & SDLC (APP)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-APP-01 | Yes. SSDLC documented; security requirements and threat modeling required at design phase for major features. | EVD-APP-01 |
| Q-APP-02 | Yes. SAST (Semgrep) runs on every pull request; DAST (OWASP ZAP) runs weekly against staging. | EVD-APP-02 |
| Q-APP-03 | Critical vulnerabilities: 14-day SLA. High: 30 days. Medium/Low: best-effort, no formal SLA. | EVD-APP-03 |
| Q-APP-04 | Yes. Public bug bounty program hosted on HackerOne since 2023. | EVD-APP-04 |

## F. Incident Response & Breach Notification (IR)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-IR-01 | Yes. Incident Response Plan last tabletop-tested 2025-06-12. | EVD-IR-01 |
| Q-IR-02 | Contractual breach notification SLA: 72 hours from confirmed determination of a reportable incident. | EVD-IR-02 |
| Q-IR-03 | Yes — one incident in the last 24 months. In March 2025, a misconfigured S3 bucket briefly exposed non-production test data (no real customer PII involved) for approximately 6 hours before detection and remediation. Root cause analysis completed; bucket policy automation implemented to prevent recurrence. | EVD-IR-03 |
| Q-IR-04 | Yes. 24/7 SOC outsourced to a managed security service provider (MSSP), with Splunk SIEM. | EVD-IR-04 |

## G. Business Continuity & Disaster Recovery (BCDR)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-BCDR-01 | Yes. BCDR plan maintained and reviewed annually. | EVD-BCDR-01 |
| Q-BCDR-02 | RTO: 4 hours. RPO: 1 hour. | EVD-BCDR-02 |
| Q-BCDR-03 | Last full DR failover test: **2024-08-20** (approx. 18 months ago). Tabletop-only exercise conducted 2025-09. | EVD-BCDR-03 |
| Q-BCDR-04 | Yes. Automated backups every 6 hours, replicated cross-region (us-east-1 → us-west-2), 35-day retention. | EVD-BCDR-04 |

## H. Compliance & Legal (COMP)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-COMP-01 | Yes, GDPR and CCPA compliance programs in place; DPO appointed. | EVD-COMP-01 |
| Q-COMP-02 | Yes, standard DPA available and will be executed as part of contracting. BAA not applicable (no PHI processed). | EVD-COMP-02 |
| Q-COMP-03 | Yes. Application and infrastructure audit logs retained for 13 months, exportable via API. | EVD-COMP-03 |

## I. Fourth-Party / Subprocessor Risk (SUB)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-SUB-01 | Subprocessor list: AWS (hosting), Twilio (SMS/MFA delivery), SendGrid (transactional email), Stripe (billing only, no document data). Full list maintained on public Trust Center page. | EVD-SUB-01 |
| Q-SUB-02 | Yes. Standard subprocessor agreements include confidentiality, security, and data protection clauses flowed down from CloudVault's customer contracts. | EVD-SUB-02 |
| Q-SUB-03 | Partial. New subprocessors undergo a security review before onboarding; however, this review is not yet standardized against a formal, documented due-diligence checklist (currently ad hoc). | EVD-SUB-03 |

## J. Physical Security (PHYS)

| ID | Vendor Response | Evidence Ref |
|---|---|---|
| Q-PHYS-01 | Not applicable — no self-hosted/on-premises infrastructure; 100% AWS-hosted. | N/A |
| Q-PHYS-02 | Yes. AWS data centers are independently SOC 2 / ISO 27001 certified; inherited compliance documented in AWS Artifact. | EVD-PHYS-01 |

---

**Vendor Certification:** "I certify that the responses provided above are accurate and complete to the best of my knowledge as of the date submitted." — J. Ramirez, Director of Security & Compliance, CloudVault Data Solutions
