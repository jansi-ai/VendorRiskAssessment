# Auditor Findings Report

**Vendor:** Vantage Cloud Systems
**Assessor:** A. Reyes, TPRM Analyst (fictional) - reviewed by D. Okonkwo, Senior Security Auditor (fictional)
**Assessment Period:** 2026-03-21 to 2026-04-10
**Methodology:** `02-finding-classification-methodology/finding-classification-and-treatment-deadlines.md`

## 1. Summary

Of 24 questions across 12 CCM domains, **12 findings** were identified: **1 Critical**, **4 High**, and **7 Moderate**. Three findings carry the **Critical Security finding** label (automatic escalation) and were flagged to the TPRM Program Manager immediately upon identification, independent of their severity score.

## 2. Findings Register

| Finding ID | Domain | Question | Finding Name | Label | Type | Response Scenario | Severity |
|---|---|---|---|---|---|---|---|
| F-IAM-02 | IAM | Q-IAM-02 | Privileged & Remote Access MFA | **Critical Security finding** | Technical misconfiguration | "No" | **Critical (10)** |
| F-DSP-02 | DSP | Q-DSP-02 | Data Loss Prevention | Standard finding | Technical misconfiguration | "No" | **High (5)** |
| F-LOG-02 | LOG | Q-LOG-02 | Security Event Logging | **Critical Security finding** | Technical misconfiguration | "Yes" - no evidence | **High (5)** |
| F-TVM-02 | TVM | Q-TVM-02 | Authenticated Scan Frequency | Standard finding | Technical misconfiguration | "No" | **High (5)** |
| F-CEK-02 | CEK | Q-CEK-02 | Data at Rest and in Transit | Standard finding | Technical misconfiguration | "Yes" - no evidence | **High (5)** |
| F-BCR-02 | BCR | Q-BCR-02 | Business Continuity Exercises | Standard finding | Missing Capability | "Yes" - no evidence | Moderate (1) |
| F-CCC-02 | CCC | Q-CCC-02 | Change Approval Process | Standard finding | Missing Capability | "Yes" - partial | Moderate (1) |
| F-DSP-01 | DSP | Q-DSP-01 | Data Security & Privacy Lifecycle Mgmt | Standard finding | Missing Capability | "Yes" - partial | Moderate (1) |
| F-HRS-02 | HRS | Q-HRS-02 | Security Awareness Training | **Critical Security finding** | Missing Capability | "Yes" - partial | Moderate (1) |
| F-IVS-02 | IVS | Q-IVS-02 | Network Segmentation | Standard finding | Missing Capability | "Yes" - partial (aging) | Moderate (1) |
| F-SEF-02 | SEF | Q-SEF-02 | Incident Response Testing | Standard finding | Missing Capability | "Yes" - no evidence | Moderate (1) |
| F-UEM-02 | UEM | Q-UEM-02 | Endpoint Storage Encryption | Standard finding | Technical misconfiguration | "Yes" - no evidence | Moderate (1) |

## 3. Auto-Calculated Treatment Deadlines

Per the matrix in `02-finding-classification-methodology/`, each finding's SLA is determined by Severity Ã— Type:

| Finding ID | Severity | Type | Treatment Deadline | Due Date (from 2026-04-10 issuance) |
|---|---|---|---|---|
| F-IAM-02 | Critical | Technical misconfiguration | 30 days | 2026-05-10 |
| F-DSP-02 | High | Technical misconfiguration | 90 days | 2026-07-09 |
| F-LOG-02 | High | Technical misconfiguration | 90 days | 2026-07-09 |
| F-TVM-02 | High | Technical misconfiguration | 90 days | 2026-07-09 |
| F-CEK-02 | High | Technical misconfiguration | 90 days | 2026-07-09 |
| F-BCR-02 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-CCC-02 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-DSP-01 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-HRS-02 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-IVS-02 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-SEF-02 | Moderate | Missing Capability | 365 days | 2027-04-10 |
| F-UEM-02 | Moderate | Technical misconfiguration | 180 days | 2026-10-07 |

## 4. Detailed Findings - Critical & High Only

### F-IAM-02 - Privileged & Remote Access MFA (Critical, Critical Security finding)

**Condition:** MFA is technically available in the vendor's identity platform but is not enforced for privileged accounts or for remote access paths into company infrastructure. Vendor confirms enforcement is "in progress" with no committed date.

**Criteria:** Program minimum control expectation - MFA is mandatory, not optional, for any path into infrastructure hosting or processing Solstice data.

**Effect:** Single-factor privileged/remote access is one of the most common initial access vectors in vendor-side breaches; this finding is rated Critical and labeled Critical Security finding reflecting the program's zero-tolerance stance on this specific control.

**Escalation:** Flagged to TPRM Program Manager same-day per Critical Security finding protocol; 30-day treatment deadline applies (Critical + Technical misconfiguration).

### F-DSP-02 - Data Loss Prevention (High)

**Condition:** No DLP solution is implemented at the application layer; vendor stated this outright ("No").

**Effect:** Given the vendor's SaaS platform stores confidential business-system data, absence of DLP limits detection of bulk export/exfiltration activity from a compromised or malicious account.

### F-LOG-02 - Security Event Logging (High, Critical Security finding)

**Condition:** Vendor claims a centralized SIEM but did not provide evidence of tamper protection, NTP synchronization, or the specific event types the program requires (login failures, privileged activity, anomalous events).

**Effect:** An unsubstantiated logging claim on a Critical Security finding-labeled control is treated with the same urgency as observing the gap directly, since it cannot currently be relied upon for incident detection or forensic reconstruction.

### F-TVM-02 - Authenticated Scan Frequency (High)

**Condition:** Vendor confirmed scans are unauthenticated and run quarterly, below the monthly-minimum, authenticated-scan requirement.

**Effect:** Unauthenticated scans materially under-detect vulnerabilities compared to credentialed scans; combined with a quarterly cadence, this represents a meaningful blind spot for newly disclosed vulnerabilities.

### F-CEK-02 - Data at Rest and in Transit (High)

**Condition:** Vendor claims full encryption coverage but did not provide a configuration screenshot or scan report to substantiate the claim.

**Effect:** Given the sensitivity of data in scope, an unsubstantiated encryption claim is treated as High severity despite the underlying control possibly already being correctly implemented - the program requires proof, not attestation alone, for this control.

*(Moderate findings F-BCR-02, F-CCC-02, F-DSP-01, F-HRS-02, F-IVS-02, F-SEF-02, F-UEM-02 follow the same "condition / criteria / effect" structure and are tracked in full in the CAP register - see `07-remediation-tracking/remediation-plan.md`.)*

## 5. Auditor Conclusion

No finding in this assessment is scored above Critical, and the sole Critical finding has a clear, achievable remediation path already in progress at the vendor. Proceed to `06-risk-scoring/risk-register.xlsx` for the consolidated scoring workbook, and `07-remediation-tracking/` for CAP tracking against the treatment deadlines above.


