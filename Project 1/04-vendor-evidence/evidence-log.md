# Vendor Evidence Log

**Vendor:** CloudVault Data Solutions
**Reviewed By:** M. Osei, GRC/TPRM Analyst 
**Review Period:** 2026-02-21 to 2026-03-05

This log tracks every evidence artifact submitted by the vendor, its type, the question(s) it supports, and the reviewer's validation status. In a live engagement these would be actual file attachments (PDF excerpts, screenshots, report pages); in this portfolio they are represented as a structured index with reviewer notes to demonstrate the evidence-validation workflow.

| Evidence ID | Related Question(s) | Evidence Type | Description | Date of Evidence | Validation Status | Reviewer Notes |
|---|---|---|---|---|---|---|
| EVD-GOV-01 | Q-GOV-01 | Policy excerpt | Information Security Policy v4.2, board approval signature page | 2025-11-10 | ✅ Validated | Signature and version control confirmed current |
| EVD-GOV-02 | Q-GOV-02 | Org chart | Security org chart showing CISO reporting line | 2026-01-15 | ✅ Validated | — |
| EVD-GOV-03 | Q-GOV-03 | SOC 2 Type II report | Full report, Section III (Description of Systems) and Section IV (Test of Controls), 1 exception noted (see Finding F-03) | 2025-09-30 | ✅ Validated (with exception noted) | Auditor's opinion is unqualified; one control exception noted in Section IV related to access review timeliness for 3 sampled terminated users |
| EVD-GOV-04 | Q-GOV-04 | Insurance certificate | Certificate of cyber liability insurance, Chubb, $5M aggregate | 2026-01-01 | ✅ Validated | Coverage confirmed active through 2027-01-01 |
| EVD-GOV-05 | Q-GOV-05 | Training completion report | LMS export showing 98% completion rate FY2025 | 2026-01-10 | ✅ Validated | — |
| EVD-DS-01 | Q-DS-01 | Architecture doc / AWS KMS config screenshot | Confirms AES-256 encryption at rest via AWS KMS | 2026-01-20 | ✅ Validated | — |
| EVD-DS-02 | Q-DS-02 | SSL Labs scan report | TLS configuration scan of app.cloudvault.example | 2026-02-18 | ✅ Validated | TLS 1.0/1.1 confirmed disabled; grade A |
| EVD-DS-03 | Q-DS-03 | Product roadmap excerpt | BYOK listed as "planned Q4 2026" | 2026-02-01 | ⚠️ Noted — gap, not evidence of control | Confirms feature does not currently exist |
| EVD-DS-04 | Q-DS-04 | Architecture doc | Multi-tenancy data model diagram | 2026-01-20 | ✅ Validated | Logical segregation confirmed; no evidence of dedicated tenancy option |
| EVD-DS-05 | Q-DS-05 | Data retention policy | Data Retention & Deletion Standard v2.0 | 2025-08-01 | ✅ Validated | — |
| EVD-DS-06 | Q-DS-06 | DLP tool configuration screenshot | Proofpoint DLP config for outbound email only | 2026-01-25 | ⚠️ Partial | Confirms DLP scope limited to email; no application-layer DLP evidence provided |
| EVD-AC-01 | Q-AC-01 | Okta admin policy screenshot | MFA enforcement policy for admin group | 2026-02-10 | ✅ Validated | — |
| EVD-AC-02 | Q-AC-02 | Okta adoption report | MFA adoption metrics, 78% of end users | 2026-02-10 | ⚠️ Gap confirmed | Evidence confirms vendor's self-reported gap; MFA not mandatory for standard end-user tier |
| EVD-AC-03 | Q-AC-03 | RBAC role matrix | Role/permission matrix document | 2025-12-01 | ✅ Validated | — |
| EVD-AC-04 | Q-AC-04 | Access recertification log | Q4 2025 privileged access review sign-off | 2025-12-15 | ✅ Validated | — |
| EVD-AC-05 | Q-AC-05 | HRIS-Okta integration doc + manual process SOP | Deprovisioning workflow documentation | 2025-10-01 | ⚠️ Partial | 10% of accounts (legacy/contractor) rely on manual process with no evidence of consistent SLA adherence — sampled 5 tickets, 1 exceeded 24-hr SLA (32 hrs) |
| EVD-AC-06 | Q-AC-06 | SSO configuration guide | SAML/OIDC setup documentation | 2026-01-05 | ✅ Validated | — |
| EVD-NET-01 | Q-NET-01 | Network architecture diagram | VPC segmentation diagram | 2025-11-01 | ✅ Validated | — |
| EVD-NET-02 | Q-NET-02 | Qualys scan schedule + sample report | Weekly scan configuration and Feb 2026 sample results | 2026-02-15 | ✅ Validated | 3 medium findings from sample scan, all within SLA remediation window |
| EVD-NET-03 | Q-NET-03 | Penetration test report | Third-party (Redacted Firm) pen test summary report | 2024-11-15 | ⚠️ Aging evidence | Report is 15 months old at assessment date; exceeds 12-month annual cadence commitment |
| EVD-NET-04 | Q-NET-04 | AWS GuardDuty configuration screenshot | GuardDuty enabled across all production accounts | 2026-01-30 | ✅ Validated | — |
| EVD-NET-05 | Q-NET-05 | AWS account/region inventory | Region and account structure export | 2026-01-30 | ✅ Validated | — |
| EVD-APP-01 | Q-APP-01 | SSDLC policy document | Secure SDLC Standard v3.1 | 2025-09-01 | ✅ Validated | — |
| EVD-APP-02 | Q-APP-02 | CI/CD pipeline configuration screenshot | Semgrep + OWASP ZAP integration in pipeline | 2026-01-12 | ✅ Validated | — |
| EVD-APP-03 | Q-APP-03 | Patch management SLA policy | Vulnerability Management Standard v2.3 | 2025-07-01 | ⚠️ Partial | Confirms no formal SLA for Medium/Low severity vulnerabilities |
| EVD-APP-04 | Q-APP-04 | HackerOne program page | Public bug bounty program listing | 2026-02-01 | ✅ Validated | — |
| EVD-IR-01 | Q-IR-01 | Tabletop exercise after-action report | IR tabletop summary and action items | 2025-06-12 | ✅ Validated | — |
| EVD-IR-02 | Q-IR-02 | Master Services Agreement excerpt | Breach notification clause, Section 9.3 | 2025-01-01 | ✅ Validated | — |
| EVD-IR-03 | Q-IR-03 | Incident postmortem report | S3 misconfiguration incident RCA and remediation | 2025-03-14 | ✅ Validated | No real customer data confirmed exposed; corrective action (automated bucket policy enforcement) verified implemented |
| EVD-IR-04 | Q-IR-04 | MSSP contract + Splunk dashboard screenshot | 24/7 SOC monitoring confirmation | 2026-01-05 | ✅ Validated | — |
| EVD-BCDR-01 | Q-BCDR-01 | BCDR plan document | Business Continuity & Disaster Recovery Plan v5.0 | 2025-10-01 | ✅ Validated | — |
| EVD-BCDR-02 | Q-BCDR-02 | BCDR plan excerpt | RTO/RPO targets defined | 2025-10-01 | ✅ Validated | — |
| EVD-BCDR-03 | Q-BCDR-03 | DR test report | Last full failover test report | 2024-08-20 | ⚠️ Aging evidence | Full failover test exceeds 12-month target cadence; only tabletop conducted since |
| EVD-BCDR-04 | Q-BCDR-04 | Backup configuration screenshot | AWS Backup cross-region replication config | 2026-01-30 | ✅ Validated | — |
| EVD-COMP-01 | Q-COMP-01 | Privacy program documentation | GDPR/CCPA compliance program overview, DPO appointment letter | 2025-06-01 | ✅ Validated | — |
| EVD-COMP-02 | Q-COMP-02 | Standard DPA template | Data Processing Agreement template | 2025-01-01 | ✅ Validated | — |
| EVD-COMP-03 | Q-COMP-03 | Log retention configuration | Audit log retention settings (13 months) | 2026-01-20 | ✅ Validated | — |
| EVD-SUB-01 | Q-SUB-01 | Public Trust Center subprocessor list | Subprocessor list screenshot | 2026-02-15 | ✅ Validated | Cross-checked against contract Exhibit C — consistent |
| EVD-SUB-02 | Q-SUB-02 | Sample subprocessor agreement clause | Confidentiality/security flow-down clause excerpt | 2025-05-01 | ✅ Validated | — |
| EVD-SUB-03 | Q-SUB-03 | Subprocessor onboarding checklist (draft) | Informal review checklist, marked "draft — not yet approved" | 2026-01-10 | ⚠️ Gap confirmed | No formalized, approved due-diligence process exists |
| EVD-PHYS-01 | Q-PHYS-02 | AWS Artifact compliance report reference | AWS SOC 2 / ISO 27001 report access confirmation | 2026-01-30 | ✅ Validated | — |

## Evidence Summary

| Status | Count |
|---|---|
| ✅ Validated | 29 |
| ⚠️ Partial / Gap / Aging | 8 |
| ❌ Not Provided | 0 |
| **Total Evidence Items Reviewed** | **37** |

All items flagged ⚠️ above are carried forward into `05-risk-assessment/auditor-risk-assessment.md` as formal findings.
