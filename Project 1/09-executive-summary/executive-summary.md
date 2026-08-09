# Executive Summary — Vendor Risk Assessment

**Vendor:** CloudVault Data Solutions
**Service:** Cloud document storage, e-signature, and workflow automation
**Vendor Tier:** Tier 1 — Critical
**Assessment Period:** 2026-02-03 (questionnaire issued) → 2026-07-15 (residual assessment)
**Prepared For:** CISO, TPRM Program Manager, Vendor Contract Owner
**Prepared By:** GRC / TPRM Team

## 1. Purpose

This summary presents the outcome of Meridian Financial Services' annual Tier 1 third-party risk assessment of CloudVault Data Solutions and requests formal risk acceptance / vendor approval, per Vendor Risk Management Policy §4.

## 2. Bottom Line Up Front (BLUF)

**CloudVault Data Solutions is approved to continue as a Tier 1 vendor.** The assessment identified 9 findings (1 High, 5 Medium, 3 Low at inherent risk). Following a structured remediation program, 8 of 9 findings have been closed and independently verified, reducing aggregate scored risk by approximately **78%**. One Medium-rated finding (application-layer DLP rollout) remains open and is being tracked to closure under standard program monitoring — it does not require executive risk acceptance.

## 3. Assessment Process

1. Standardized 30-question security questionnaire issued across 10 control domains (`02-security-questionnaire/`)
2. Vendor responses collected and evidence independently validated (`03`, `04`)
3. Independent auditor assessment produced 9 findings against NIST CSF / ISO 27001 / SOC 2 control objectives (`05`)
4. Each finding scored using Likelihood × Impact methodology (`06`)
5. Corrective Action Plans issued with named owners and target dates (`07`)
6. Remediation independently re-verified and residual risk re-scored (`08`)

## 4. Key Findings & Outcomes

| Rating (Inherent) | Count | Rating (Residual) | Count |
|---|---|---|---|
| Critical | 0 | Critical | 0 |
| High | 1 | High | 0 |
| Medium | 5 | Medium | 1 |
| Low | 3 | Low | 8 |

**Highlight — F-01 (MFA Enforcement, High → Low):** The most significant gap identified was that multi-factor authentication was not mandatory for standard end-user accounts (~22% of accounts unprotected). CloudVault remediated this within 39 days by making MFA platform-enforced and removing the customer opt-out, closing our single highest-priority item well ahead of the 45-day target.

**Open Item — F-06 (Application-layer DLP, Medium):** DLP tooling for the SaaS application layer (beyond email) is in pilot rollout (20% of tenants) and targeted for full deployment by 2026-08-15. GRC will independently verify closure and update the residual risk register at that time; no compensating control is required in the interim given no evidence of active exploitation risk.

## 5. Positive Observations

- Current SOC 2 Type II attestation with unqualified opinion (one minor exception, since remediated)
- Mature application security program: SAST/DAST in CI/CD, public bug bounty program
- 24/7 SOC monitoring via MSSP with Splunk SIEM
- Transparent, prompt disclosure and remediation of a prior minor incident (non-production data exposure, March 2025)
- High responsiveness throughout the CAP process — no findings required escalation, pushback, or contract remedy

## 6. Recommendation & Sign-Off

**Recommendation:** Approve CloudVault Data Solutions for continued engagement as a Tier 1 vendor. Continue standard annual reassessment cadence (next due: 2027-03-05), with an interim check-in for CAP-05 (F-06) closure targeted for 2026-08-15.

| Approver | Role | Decision | Date |
|---|---|---|---|
| *(fictional signature)* K. Whitfield | Senior Security Auditor | Recommend Approval | 2026-07-15 |
| *(fictional signature)* — | TPRM Program Manager | Approved (Medium-risk monitoring authority) | 2026-07-16 |
| *(fictional signature)* — | CISO | Acknowledged — no High/Critical residual risk requiring CISO acceptance | 2026-07-16 |

---
*This document, and all findings, scores, names, and dates referenced above, are fictional and created for portfolio demonstration purposes only.*
