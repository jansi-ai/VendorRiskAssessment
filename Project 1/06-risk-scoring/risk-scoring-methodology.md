# Risk Scoring Methodology

## 1. Purpose

This document defines the quantitative methodology used to score each finding identified during vendor risk assessment, producing a consistent **Inherent Risk Rating** (pre-remediation) that is later re-scored as **Residual Risk** (post-remediation) in `08-residual-risk/`.

## 2. Scoring Model: Likelihood × Impact

Each finding is scored on two independent 1–5 scales. The product of the two scores (1–25) determines the overall risk rating.

### 2.1 Likelihood Scale

| Score | Rating | Definition |
|---|---|---|
| 1 | Rare | Would only occur in exceptional circumstances; no evidence of prior occurrence |
| 2 | Unlikely | Could occur but not expected under normal operating conditions |
| 3 | Possible | Might occur at some point; comparable incidents have occurred at similar organizations |
| 4 | Likely | Will probably occur in most circumstances; some evidence of near-miss or partial occurrence |
| 5 | Almost Certain | Expected to occur; evidence of prior occurrence or active exploitation trend industry-wide |

### 2.2 Impact Scale

| Score | Rating | Definition |
|---|---|---|
| 1 | Negligible | No meaningful impact to confidentiality, integrity, availability, or compliance posture |
| 2 | Minor | Limited operational impact; no data exposure; easily contained |
| 3 | Moderate | Some data or service impact; contained to non-critical data or limited user population |
| 4 | Major | Significant exposure of confidential/regulated data, or material service disruption |
| 5 | Severe | Large-scale breach of regulated data (PII/financial), regulatory/legal exposure, or critical service outage |

### 2.3 Risk Score & Rating Bands

`Risk Score = Likelihood × Impact`

| Score Range | Rating | Color | Response Expectation |
|---|---|---|---|
| 1 – 4 | **Low** | 🟢 Green | Monitor; remediate opportunistically |
| 5 – 9 | **Medium** | 🟡 Yellow | Remediate within 90 days; track via CAP |
| 10 – 15 | **High** | 🟠 Orange | Remediate within 45 days; CAP with named owner and executive visibility |
| 16 – 25 | **Critical** | 🔴 Red | Remediate within 15 days or escalate for risk acceptance / contract remedy at CISO level; may pause onboarding |

## 3. Scoring Inputs

Likelihood and Impact scores are assigned by the assessor based on:
- Evidence quality and validation status (`04-vendor-evidence/`)
- Sensitivity of data in scope (confirmed: PII, financial account data)
- Vendor tier (Tier 1 — highest scrutiny)
- Industry threat intelligence relevant to the control gap (e.g., credential-based attacks trending for MFA-related findings)
- Whether the gap has a compensating control

## 4. Inherent vs. Residual Risk

- **Inherent Risk** — the risk score assigned based on the finding as originally identified, assuming no remediation has yet occurred. This is what appears in the Risk Register (`risk-register.xlsx`) below.
- **Residual Risk** — the risk score re-assigned after a Corrective Action Plan (CAP) has been implemented and independently verified (see `08-residual-risk/`). Residual risk reflects the effectiveness of the remediation, not merely its completion.

## 5. Risk Register

See [`risk-register.xlsx`](./risk-register.xlsx) for the full scored register of all 9 findings from `05-risk-assessment/auditor-risk-assessment.md`, including Likelihood, Impact, calculated Inherent Risk Score, and Rating (auto-calculated via formula).

## 6. Risk Acceptance Thresholds

| Residual Rating | Approval Authority Required |
|---|---|
| Low | GRC Analyst — no further approval needed |
| Medium | TPRM Program Manager |
| High | CISO |
| Critical | CISO + Business Owner + (if applicable) Legal/Compliance sign-off |
