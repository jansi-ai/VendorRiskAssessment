# Third-Party Risk Management (TPRM) Program — Portfolio Project

## Overview

This repository is a portfolio artifact demonstrating an end-to-end **Third-Party / Vendor Risk Management (TPRM)** lifecycle for a SaaS vendor security assessment, built to reflect real-world GRC and cybersecurity audit practice.

**⚠️ Disclaimer:** All company names, vendor names, personnel, findings, and data in this repository are **fictional** and created solely to demonstrate GRC/TPRM methodology, documentation standards, and analytical skills for a job application portfolio. No real organization, individual, or vendor is represented.

## Scenario

| | |
|---|---|
| **Assessing Organization** | Meridian Financial Services (fictional mid-size fintech, SOC 2 Type II obligated) |
| **Vendor Under Review** | CloudVault Data Solutions (fictional SaaS document management / cloud storage provider) |
| **Service Provided** | Cloud-based document storage, e-signature, and workflow automation processing customer PII and financial records |
| **Data Classification** | Confidential — includes PII, account numbers, and transaction metadata |
| **Assessment Trigger** | New vendor onboarding — annual recurring assessment thereafter |
| **Frameworks Referenced** | NIST CSF 2.0, NIST SP 800-53 Rev. 5, ISO/IEC 27001:2022, SOC 2 Trust Services Criteria, CSA CAIQ v4, GDPR / CCPA |

## Repository Structure

```
tprm-portfolio/
├── README.md                                  <- You are here
├── 01-vendor-risk-management-policy/          <- Program governance & policy
├── 02-security-questionnaire/                 <- Standardized vendor questionnaire (sent to vendor)
├── 03-vendor-responses/                       <- Vendor's completed questionnaire responses
├── 04-vendor-evidence/                        <- Evidence log mapping responses to supporting artifacts
├── 05-risk-assessment/                        <- Auditor's control testing & findings (gap analysis)
├── 06-risk-scoring/                           <- Risk scoring methodology + risk register (inherent risk)
├── 07-remediation-plan/                       <- Findings tracked to closure (CAPs, owners, due dates)
├── 08-residual-risk/                          <- Post-remediation residual risk scoring & re-rating
└── 09-executive-summary/                      <- Board/leadership-level summary & risk acceptance decision
```

## TPRM Lifecycle Represented

1. **Policy & Scoping** — Vendor tiering criteria and assessment cadence (`01`)
2. **Questionnaire Design** — Domain-based security questionnaire aligned to NIST CSF functions (`02`)
3. **Vendor Response Collection** — Vendor self-attestation (`03`)
4. **Evidence Collection & Validation** — SOC 2 reports, pen test summaries, policy excerpts, screenshots referenced by ID (`04`)
5. **Independent Risk Assessment** — Auditor testing, control gap analysis, findings with severity ratings (`05`)
6. **Risk Scoring (Inherent)** — Likelihood × Impact scoring methodology and register (`06`)
7. **Remediation Tracking** — Corrective Action Plans (CAPs) with owners and SLAs (`07`)
8. **Residual Risk Scoring** — Re-scored risk after remediation validation (`08`)
9. **Executive Reporting** — Summary for risk acceptance / vendor approval decision (`09`)

## Key Skills Demonstrated

- Vendor risk questionnaire design (NIST CSF / ISO 27001 / SOC 2 aligned)
- Evidence-based control validation and audit trail documentation
- Risk assessment methodology (likelihood/impact matrices, inherent vs. residual risk)
- Findings and gap analysis writing (auditor voice)
- Remediation / Corrective Action Plan (CAP) tracking
- Executive-level risk communication and risk acceptance documentation

## How to Navigate

Each folder is numbered in lifecycle order. Question IDs (e.g., `Q-AC-01`) are consistent across the questionnaire, vendor responses, evidence log, and findings documents so you can trace a single control end-to-end — from the question asked, to the vendor's answer, to the evidence reviewed, to the finding, to its remediation, to its final residual rating.
