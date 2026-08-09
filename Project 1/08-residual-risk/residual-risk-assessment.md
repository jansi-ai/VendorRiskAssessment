# Residual Risk Assessment

**Vendor:** CloudVault Data Solutions
**Assessment Type:** Post-Remediation Re-Scoring
**Assessor:** M. Osei, GRC/TPRM Analyst (fictional)
**Assessment Date:** 2026-07-15
**Reference:** Findings and CAPs per `05-risk-assessment/` and `07-remediation-plan/`

## 1. Purpose

This document re-scores each finding's Likelihood and Impact following implementation and independent verification of its Corrective Action Plan (CAP), producing a **Residual Risk Rating**. Per methodology (`06-risk-scoring/risk-scoring-methodology.md` §4), residual scoring reflects the assessor's judgment of remediation *effectiveness*, not merely CAP closure status.

## 2. Residual Scoring Approach

For each finding:
- If the CAP is **Closed & Verified**, Likelihood is reduced to reflect the new control (typically to 1–2) and Impact is reduced where the control also limits blast radius (e.g., automated alerting reduces exposure window).
- If the CAP is **In Progress**, Likelihood/Impact are only partially reduced to reflect partial mitigation (e.g., pilot-stage rollout).
- If **no CAP was required** (informational finding), the score is carried forward unchanged and re-evaluated at the next annual cycle.

## 3. Residual Risk Register

See [`residual-risk-register.xlsx`](./residual-risk-register.xlsx) for the full scored comparison of Inherent vs. Residual risk for all 9 findings.

## 4. Narrative Summary by Finding

| Finding | Inherent Rating | Residual Rating | Rationale |
|---|---|---|---|
| F-01 (MFA) | High (20) | **Low (2)** | Platform-level MFA enforcement verified across 100% of sampled active accounts; the primary attack vector (unauthenticated single-factor accounts) is eliminated. |
| F-02 (Pen test cadence) | Medium (12) | **Low (2)** | Current pen test on file (30 days old at assessment); cadence commitment now contractual, reducing recurrence likelihood. |
| F-03 (SOC 2 access exception) | Medium (9) | **Low (2)** | Root cause (manual process) eliminated via CAP-03; independently re-sampled with 100% SLA adherence. |
| F-04 (Manual deprovisioning) | Medium (9) | **Low (2)** | Same remediation as F-03 — automated deprovisioning removes the manual process entirely. |
| F-05 (DR failover test) | Medium (12) | **Low (2)** | Full failover test successfully executed and met RTO/RPO targets; cadence re-baselined to 12 months. |
| F-06 (Application-layer DLP) | Medium (8) | **Medium (6)** | Partial mitigation only — DLP tooling in pilot on 20% of tenants at time of this assessment; residual risk remains elevated until full rollout is verified. **This CAP remains open and is the primary focus of the next interim check-in (target 2026-08-15).** |
| F-07 (Subprocessor due diligence) | Low (4) | **Low (1)** | Formal checklist approved and retroactively applied; residual risk minimal. |
| F-08 (Vuln SLA) | Low (4) | **Low (1)** | Formal SLA published and operationalized in ticketing system. |
| F-09 (BYOK unavailable) | Low (3) | **Low (3)** | Unchanged — no compensating control implemented or required at current risk tier; tracked for the vendor's Q4 2026 roadmap delivery. |

## 5. Overall Residual Risk Posture

Of the original **9 findings** (1 High, 5 Medium, 3 Low at inherent rating), the residual risk posture as of this assessment is **8 Low, 1 Medium**, with the single remaining Medium item (F-06) actively tracked to closure.

**Aggregate Risk Reduction:** The vendor's total inherent risk score across all findings was 89 (sum of individual scores); residual is 20 — an approximate **78% reduction** in aggregate scored risk following remediation.

## 6. Risk Acceptance Decision

Per Policy §4 and the acceptance thresholds in `06-risk-scoring/risk-scoring-methodology.md` §6:

- No findings remain at High or Critical residual rating → **no CISO risk acceptance required** at this time.
- F-06 (Medium residual) falls under **TPRM Program Manager** approval authority for continued monitoring pending full DLP rollout.

**Decision:** ✅ **CloudVault Data Solutions is approved to continue as a Tier 1 vendor**, with F-06 tracked as an open item to be closed and verified before the next annual reassessment (target: 2027-03-05). See `09-executive-summary/` for the leadership-level summary and formal sign-off record.
