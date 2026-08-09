# Auditor Risk Assessment & Findings

**Vendor:** CloudVault Data Solutions
**Assessment Type:** Tier 1 Annual TPRM Assessment (New Vendor Onboarding)
**Assessor:** M. Osei, GRC/TPRM Analyst (fictional) — reviewed by K. Whitfield, Senior Security Auditor (fictional)
**Assessment Period:** 2026-02-21 to 2026-03-05
**Methodology:** Independent review of vendor questionnaire responses (`03-vendor-responses/`) against submitted evidence (`04-vendor-evidence/`), cross-referenced to NIST CSF 2.0, ISO 27001:2022 Annex A, and SOC 2 Trust Services Criteria control objectives.

## 1. Scope of Review

This assessment covers all 10 domains of the Vendor Security Questionnaire (30 questions). Each vendor claim was validated against the corresponding evidence artifact. Discrepancies, gaps, or unsubstantiated claims are documented as formal findings below.

## 2. Overall Assessment Summary

CloudVault Data Solutions demonstrates a **generally mature security program** appropriate for a Tier 1 critical SaaS vendor, including current SOC 2 Type II attestation, strong encryption practices, documented incident response, and an active application security program (SAST/DAST, bug bounty). No findings identified during this assessment rise to **Critical** severity, and no evidence of an unremediated breach involving Meridian-relevant data was found.

However, **9 findings** were identified, concentrated in three themes: (1) inconsistent enforcement of authentication and deprovisioning controls at the end-user level, (2) testing/validation activities (penetration test, DR failover test) that have lapsed beyond the vendor's own stated cadence, and (3) immature/undocumented processes for subprocessor due diligence and lower-severity patch management. These are consistent with a growing SaaS company that has strong foundational controls but has not yet fully operationalized consistency at scale.

**Recommendation:** Approve CloudVault for engagement at Tier 1, contingent on Corrective Action Plans (CAPs) for High and Medium findings per `07-remediation-plan/`, with re-verification prior to or at the 12-month reassessment.

## 3. Findings Register

| Finding ID | Domain | Title | Severity | Control Reference | Related Question(s) / Evidence |
|---|---|---|---|---|---|
| F-01 | Access Control | MFA not mandatory for standard end-user accounts | **High** | NIST CSF PR.AA-03; ISO 27001 A.8.5; SOC 2 CC6.1 | Q-AC-02 / EVD-AC-02 |
| F-02 | Network Security | Penetration test exceeds vendor's stated annual cadence (15 months since last test) | **Medium** | NIST CSF ID.RA-01; ISO 27001 A.8.8; SOC 2 CC4.1 | Q-NET-03 / EVD-NET-03 |
| F-03 | Governance | SOC 2 report exception: untimely access revocation for 3 sampled terminated users | **Medium** | NIST CSF PR.AA-01; ISO 27001 A.5.18; SOC 2 CC6.2 | Q-GOV-03 / EVD-GOV-03 |
| F-04 | Access Control | Manual deprovisioning process for legacy/contractor accounts (10% of population) lacks consistent SLA adherence | **Medium** | NIST CSF PR.AA-01; ISO 27001 A.5.18 | Q-AC-05 / EVD-AC-05 |
| F-05 | Business Continuity | DR full failover test exceeds 12-month cadence (18 months since last full test; tabletop-only since) | **Medium** | NIST CSF ID.RA-01; ISO 27001 A.5.30; SOC 2 A1.2 | Q-BCDR-03 / EVD-BCDR-03 |
| F-06 | Data Security | Data Loss Prevention (DLP) not implemented at the application layer, limited to outbound email | **Medium** | NIST CSF PR.DS-05; ISO 27001 A.8.12 | Q-DS-06 / EVD-DS-06 |
| F-07 | Fourth-Party Risk | Subprocessor due-diligence process not formalized (checklist exists only in draft) | **Low** | NIST CSF GV.SC-06; ISO 27001 A.5.19 | Q-SUB-03 / EVD-SUB-03 |
| F-08 | Application Security | No formal remediation SLA for Medium/Low severity vulnerabilities | **Low** | NIST CSF ID.RA-01; ISO 27001 A.8.8 | Q-APP-03 / EVD-APP-03 |
| F-09 | Data Security | Customer-managed encryption keys (BYOK) not currently available | **Low (Informational)** | NIST CSF PR.DS-01; ISO 27001 A.8.24 | Q-DS-03 / EVD-DS-03 |

## 4. Detailed Findings

### F-01 — MFA Not Mandatory for Standard End-User Accounts (High)

**Condition:** MFA is available and defaulted on for new tenants but remains customer-configurable/optional for existing standard end-user accounts. Vendor-reported adoption is 78%, meaning approximately 22% of end-user accounts with access to Meridian data may authenticate with a single factor.

**Criteria:** Meridian's minimum control expectations (Policy §6) require MFA enforcement for all accounts with access to confidential data, not solely privileged accounts.

**Cause:** Product design historically treated MFA as tenant-configurable rather than platform-enforced; no compensating control (e.g., risk-based/adaptive authentication) confirmed for non-MFA sessions.

**Effect:** Increased likelihood of unauthorized access via credential compromise (phishing, credential stuffing) for the ~22% of accounts without MFA, directly exposing confidential financial records and PII.

**Auditor Opinion:** This is the most significant gap identified in this assessment given the sensitivity of data in scope, and is the primary driver of this finding's High severity rating.

### F-02 — Penetration Test Cadence Lapse (Medium)

**Condition:** Most recent third-party penetration test was dated 2024-11-15, approximately 15 months prior to this assessment, exceeding the vendor's own stated annual cadence and Meridian's Tier 1 minimum expectation.

**Criteria:** Policy §6 requires evidence of testing/assessment activity within the last 12 months for Tier 1 vendors.

**Effect:** Newly introduced vulnerabilities in the 15-month gap have not been independently validated; weekly automated scanning (Qualys) partially mitigates but does not replace manual penetration testing (e.g., business logic flaws, chained exploits).

### F-03 — SOC 2 Exception: Untimely Access Revocation (Medium)

**Condition:** The vendor's own SOC 2 Type II report notes an exception where 3 of a sampled population of terminated users had access revoked outside the vendor's documented SLA.

**Criteria:** Consistency between stated policy (24-hour revocation SLA) and independently tested operating effectiveness (SOC 2 Section IV).

**Effect:** This is independently corroborated by our own evidence review (EVD-AC-05), which found a similar exception in a small internal sample — suggesting this is a systemic, not isolated, gap in the manual deprovisioning workflow.

### F-04 — Manual Deprovisioning SLA Adherence (Medium)

**Condition:** Sample testing of 5 deprovisioning tickets for legacy/contractor accounts found 1 instance where revocation took 32 hours against a 24-hour SLA.

**Effect:** Confirms and reinforces F-03; the manual (non-automated) 10% of the account population represents disproportionate risk relative to its size.

*(Note: F-03 and F-04 are related but tracked separately as they originate from independent evidence sources — vendor's own SOC 2 auditor and Meridian's direct sample testing, respectively. They are consolidated into a single CAP in the remediation plan.)*

### F-05 — DR Full Failover Test Cadence Lapse (Medium)

**Condition:** Last full DR failover test was 2024-08-20 (~18 months prior). Only a tabletop exercise has been conducted since (2025-09).

**Effect:** A tabletop exercise validates decision-making and communication but does not confirm technical recoverability (RTO: 4 hrs / RPO: 1 hr) under real failover conditions.

### F-06 — DLP Limited to Email Channel (Medium)

**Condition:** DLP tooling (Proofpoint) is scoped only to outbound corporate email; no DLP control confirmed within the SaaS application itself (e.g., preventing bulk export/exfiltration of stored documents).

**Effect:** Given the service's core function is document storage of confidential data, absence of application-layer DLP represents a gap in defense-in-depth against insider threat or compromised-account bulk exfiltration.

### F-07 — Subprocessor Due Diligence Not Formalized (Low)

**Condition:** A subprocessor onboarding checklist exists but is marked "draft — not yet approved"; the vendor confirmed the review process is currently ad hoc.

**Effect:** Elevated fourth-party risk if a future subprocessor is onboarded without consistent security vetting; low likelihood in the near term given a small, stable subprocessor list.

### F-08 — No Formal SLA for Medium/Low Vulnerability Remediation (Low)

**Condition:** Critical (14-day) and High (30-day) vulnerability SLAs are defined; Medium/Low severity vulnerabilities are remediated "best-effort" without a defined SLA.

**Effect:** Risk of vulnerability accumulation over time in lower-severity findings, which can be chained into higher-impact exploits.

### F-09 — No Customer-Managed Encryption Keys / BYOK (Low — Informational)

**Condition:** BYOK/HYOK is on the vendor's roadmap for Q4 2026 but not currently available.

**Effect:** Limits Meridian's ability to independently revoke vendor access to data via key control; acceptable at current risk tier given AES-256 vendor-managed encryption is in place, but should be revisited at next renewal.

## 5. Auditor Conclusion

No findings in this assessment are rated Critical. One finding (F-01) is rated High and requires a CAP with executive visibility. Proceed to `06-risk-scoring/` for formal likelihood/impact scoring of each finding, and `07-remediation-plan/` for CAP tracking.
