# Evidence Log - Extended Assessment

**Vendor:** Vantage Cloud Systems
**Reviewed By:** A. Reyes, TPRM Analyst (fictional)
**Review Period:** 2026-03-21 to 2026-04-02

| Evidence ID | Question | Evidence Type | Description | Validation Status | Notes |
|---|---|---|---|---|---|
| EVD-BCR-01 | Q-BCR-01 | Policy document | BCP v3.1, executive approval page | âœ… Validated | RTO/RPO, BIA, scope all confirmed present |
| EVD-BCR-02 | Q-BCR-02 | - | No test report provided | âš ï¸ Gap | Vendor claim not substantiated |
| EVD-CCC-01 | Q-CCC-01 | Policy document | Change Management Policy v2.0 | âœ… Validated | - |
| EVD-CCC-02 | Q-CCC-02 | CAB minutes + Slack export sample | Partial change log evidence | âš ï¸ Partial | Confirms informal/inconsistent minor-change tracking |
| EVD-CEK-01 | Q-CEK-01 | Policy document | Key Management Policy v1.4 | âœ… Validated | - |
| EVD-CEK-02 | Q-CEK-02 | - | No configuration screenshot or scan provided | âš ï¸ Gap | Vendor claim not substantiated |
| EVD-DCS-01 | Q-DCS-01 | Asset register export | Risk Category column confirmed | âœ… Validated | - |
| EVD-DCS-02 | Q-DCS-02 | AWS Artifact access confirmation | Inherited SOC 2 physical security | âœ… Validated | - |
| EVD-DSP-01 | Q-DSP-01 | Policy document + data flow diagram | Data Security Policy v2.2, DFD undated | âš ï¸ Partial | DFD present but review cadence unverifiable |
| EVD-HRS-01 | Q-HRS-01 | Policy + redacted form | Background Verification Policy | âœ… Validated | - |
| EVD-HRS-02 | Q-HRS-02 | LMS completion export | 95% completion FY2025 | âš ï¸ Partial | No quiz/assessment evidence |
| EVD-IAM-01 | Q-IAM-01 | Policy document | IAM Policy v3.0 | âœ… Validated | - |
| EVD-IVS-01 | Q-IVS-01 | Hardening baseline document | CIS-aligned baseline, Linux + containers | âœ… Validated | - |
| EVD-IVS-02 | Q-IVS-02 | Network diagram | Dated 2024-10 | âš ï¸ Aging evidence | Exceeds 12-month review target |
| EVD-LOG-01 | Q-LOG-01 | Policy document | Logging & Monitoring Policy v1.2 | âœ… Validated | - |
| EVD-LOG-02 | Q-LOG-02 | - | No SIEM screenshot provided | âš ï¸ Gap | Vendor claim not substantiated |
| EVD-SEF-01 | Q-SEF-01 | Policy document | Incident Response Plan v4.0 | âœ… Validated | - |
| EVD-SEF-02 | Q-SEF-02 | - | No tabletop report provided | âš ï¸ Gap | Vendor claim not substantiated |
| EVD-TVM-01 | Q-TVM-01 | Policy + scan report | Vulnerability Mgmt Standard v2.1, Tenable scan 2026-03-01 | âœ… Validated | - |
| EVD-UEM-01 | Q-UEM-01 | Configuration screenshot | CrowdStrike Falcon console, fleet-wide | âœ… Validated | - |
| EVD-UEM-02 | Q-UEM-02 | - | No management console screenshot provided | âš ï¸ Gap | Vendor claim not substantiated |

## Evidence Summary

| Status | Count |
|---|---|
| âœ… Validated | 11 |
| âš ï¸ Partial / Gap / Aging | 9 |
| **Total Evidence Items Reviewed** | **20** |

All âš ï¸-flagged items are carried forward as findings in `05-risk-assessment-findings/auditor-findings-report.md`. Questions answered "No" outright (Q-DSP-02, Q-IAM-02, Q-TVM-02) had no evidence to review and are findings by definition.

---

## Supporting Registers

This assessment also references two cross-cutting technical inventories maintained by the TPRM program (useful when the same tooling recurs across multiple suppliers under review):

- [`mfa-solutions-inventory.md`](./mfa-solutions-inventory.md) - MFA solutions observed across suppliers, mapped to remote access vs. privileged access coverage
- [`vulnerability-tool-inventory.md`](./vulnerability-tool-inventory.md) - Vulnerability scanning tools/services observed across suppliers


