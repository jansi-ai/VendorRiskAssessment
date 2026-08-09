# Vendor Questionnaire Responses - Extended Assessment

**Vendor:** Vantage Cloud Systems
**Completed By:** R. Chen, Head of Security & Compliance (fictional)
**Date Returned:** 2026-03-20
**Evidence Reference:** See `04-evidence-repository/evidence-log.md`

Legend: âœ… = Yes, with evidence provided Â· ðŸŸ¡ = Yes, evidence missing or partial Â· âŒ = No

---

## BCR - Business Continuity Management & Operational Resilience

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-BCR-01 | âœ… | BCP v3.1, approved by COO 2025-12-01, includes RTO 4hr/RPO 1hr, scope, and BIA. | EVD-BCR-01 |
| Q-BCR-02 | ðŸŸ¡ | "We test our BC plan regularly." No test report attached. | EVD-BCR-02 |

## CCC - Change Control & Configuration Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-CCC-01 | âœ… | Change Management Policy v2.0, requires logging and approval for all production changes. | EVD-CCC-01 |
| Q-CCC-02 | ðŸŸ¡ | Formal CAB exists for major releases; minor/hotfix changes approved informally via Slack thread, not consistently logged in the change system. | EVD-CCC-02 |

## CEK - Cryptography, Encryption & Key Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-CEK-01 | âœ… | Key Management Policy v1.4 covers rotation (90-day), storage (AWS KMS), and crypto-periods. | EVD-CEK-01 |
| Q-CEK-02 | ðŸŸ¡ | "All data is encrypted at rest and in transit." No configuration screenshot or scan report provided. | EVD-CEK-02 |

## DCS - Datacenter Security

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-DCS-01 | âœ… | Asset register includes a Risk Category column; reviewed quarterly. | EVD-DCS-01 |
| Q-DCS-02 | âœ… | 100% AWS-hosted; physical access inherited from AWS SOC 2 report (AWS Artifact access confirmed). | EVD-DCS-02 |

## DSP - Data Security & Privacy Lifecycle Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-DSP-01 | ðŸŸ¡ | Data Security Policy v2.2 shared - covers classification and retention, but data flow diagram is undated and not confirmed to be reviewed annually. | EVD-DSP-01 |
| Q-DSP-02 | âŒ | "We do not currently have a dedicated DLP solution in the application layer." | N/A |

## HRS - Human Resources Security

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-HRS-01 | âœ… | Background Verification Policy + redacted sample BGV form provided. | EVD-HRS-01 |
| Q-HRS-02 | ðŸŸ¡ | Annual security awareness training confirmed (LMS completion export, 95%), but no evidence of a post-training comprehension quiz. | EVD-HRS-02 |

## IAM - Identity & Access Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-IAM-01 | âœ… | IAM Policy v3.0 - unique IDs, password policy (12-char min, 90-day rotation), least-privilege RBAC. | EVD-IAM-01 |
| Q-IAM-02 | âŒ | "MFA is available but not currently enforced for all privileged accounts or all remote access paths - enforcement is in progress." | N/A |

## IVS - Infrastructure & Virtualization Security

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-IVS-01 | âœ… | CIS Benchmark-aligned hardening baseline document provided for Linux and container images. | EVD-IVS-01 |
| Q-IVS-02 | ðŸŸ¡ | Network diagram provided but last updated 2024-10 (~17 months old); no evidence of annual review. | EVD-IVS-02 |

## LOG - Logging & Monitoring

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-LOG-01 | âœ… | Logging & Monitoring Policy v1.2 defines event types, 13-month retention, annual scope review. | EVD-LOG-01 |
| Q-LOG-02 | ðŸŸ¡ | "We use a centralized SIEM." No screenshot demonstrating tamper protection, NTP sync, or specific event capture was provided. | EVD-LOG-02 |

## SEF - Security Incident Management, E-Discovery & Cloud Forensics

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-SEF-01 | âœ… | Incident Response Plan v4.0 - RACI matrix, breach notification SLA (72 hrs), legal stakeholder inclusion confirmed. | EVD-SEF-01 |
| Q-SEF-02 | ðŸŸ¡ | "IR plan is tested periodically." No tabletop after-action report or test date provided. | EVD-SEF-02 |

## TVM - Threat & Vulnerability Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-TVM-01 | âœ… | Vulnerability Management Standard v2.1 + current scan report (Tenable, dated 2026-03-01) provided. | EVD-TVM-01 |
| Q-TVM-02 | âŒ | "Our current scans are unauthenticated and run on a quarterly basis." | N/A |

## UEM - Universal Endpoint Management

| ID | Response | Vendor Notes | Evidence Ref |
|---|---|---|---|
| Q-UEM-01 | âœ… | CrowdStrike Falcon deployed fleet-wide; screenshot confirms EDR, real-time scanning, daily definition updates. | EVD-UEM-01 |
| Q-UEM-02 | ðŸŸ¡ | "All company laptops use full-disk encryption." No configuration screenshot (e.g., BitLocker/FileVault management console) provided. | EVD-UEM-02 |

---

**Vendor Certification:** "I certify that the responses provided above are accurate and complete to the best of my knowledge as of the date submitted." - R. Chen, Head of Security & Compliance, Vantage Cloud Systems


