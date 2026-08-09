# Remediation Plan - Corrective Action Plans (CAPs)

**Vendor:** Vantage Cloud Systems
**Findings Issued:** 2026-04-10
**Tracked By:** A. Reyes, TPRM Analyst (fictional)
**Status as of:** 2026-08-01 (interim checkpoint)

Each CAP's due date is auto-calculated from the finding's Severity Ã— Type per `02-finding-classification-methodology/` and mirrored in `06-risk-scoring/risk-register.xlsx`.

| CAP ID | Finding | Corrective Action | Owner | Due Date | Status | Verification Notes |
|---|---|---|---|---|---|---|
| CAP-01 | F-IAM-02 | Enforce MFA platform-wide for 100% of privileged accounts and all remote access paths; remove any bypass/exception path | Head of Security, Vantage Cloud | 2026-05-10 | âœ… **Closed** | Re-verified via live demo (2026-05-06): 100% of sampled privileged accounts (n=15) required MFA at login; VPN gateway confirmed MFA-gated |
| CAP-02 | F-DSP-02 | Implement application-layer DLP (export/download monitoring with alerting) | CISO, Vantage Cloud | 2026-07-09 | ðŸŸ¡ **In Progress** | Tooling selected (Microsoft Purview); pilot on 30% of tenants as of checkpoint; full rollout targeted 2026-08-20 |
| CAP-03 | F-LOG-02 | Provide SIEM configuration evidence demonstrating tamper protection, NTP sync, and required event capture | Head of Infrastructure, Vantage Cloud | 2026-07-09 | âœ… **Closed** | Screenshots reviewed 2026-06-18; all required event types and tamper-protection settings confirmed |
| CAP-04 | F-TVM-02 | Switch to authenticated scanning; increase cadence to monthly minimum | Head of Engineering, Vantage Cloud | 2026-07-09 | âœ… **Closed** | Tenable scan configuration reviewed 2026-06-25; credentialed scanning enabled, monthly schedule confirmed active |
| CAP-05 | F-CEK-02 | Provide configuration evidence for encryption at rest and in transit | Head of Infrastructure, Vantage Cloud | 2026-07-09 | âœ… **Closed** | AWS KMS config + SSL Labs scan (Grade A) reviewed 2026-06-10 |
| CAP-06 | F-BCR-02 | Conduct and document a Business Continuity exercise | Head of Operations, Vantage Cloud | 2027-04-10 | ðŸ”µ **Scheduled** | Exercise scheduled for 2026-10; not yet due |
| CAP-07 | F-CCC-02 | Formalize minor/hotfix change approval into the change management system (eliminate informal Slack-only approvals) | Head of Engineering, Vantage Cloud | 2027-04-10 | ðŸŸ¡ **In Progress** | Process update drafted; rollout to engineering teams in progress |
| CAP-08 | F-DSP-01 | Date and formally schedule annual review of the data flow diagram | Head of Security, Vantage Cloud | 2027-04-10 | ðŸ”µ **Scheduled** | Not yet due |
| CAP-09 | F-HRS-02 | Add a post-training comprehension quiz to the security awareness program | Head of People Ops, Vantage Cloud | 2027-04-10 | ðŸ”µ **Scheduled** | Not yet due; planned for next training cycle (Q4 2026) |
| CAP-10 | F-IVS-02 | Update network segmentation diagram and establish annual review cadence | Head of Infrastructure, Vantage Cloud | 2027-04-10 | ðŸ”µ **Scheduled** | Not yet due |
| CAP-11 | F-SEF-02 | Conduct and document an incident response tabletop exercise | CISO, Vantage Cloud | 2027-04-10 | ðŸ”µ **Scheduled** | Not yet due |
| CAP-12 | F-UEM-02 | Provide endpoint encryption management console evidence | Head of IT, Vantage Cloud | 2026-10-07 | âœ… **Closed** | BitLocker management console screenshot reviewed 2026-06-30; 100% of managed endpoints (n=210) confirmed encrypted |

## Status Summary

| Status | Count |
|---|---|
| âœ… Closed & Verified | 6 |
| ðŸŸ¡ In Progress | 2 |
| ðŸ”µ Scheduled (not yet due) | 4 |
| âŒ Overdue | 0 |

## Escalation Ladder

| Trigger | Action |
|---|---|
| CAP passes its due date without closure | Automatic escalation to TPRM Program Manager |
| Critical Security finding-labeled finding still open 15 days past due | Escalation to CISO for visibility |
| Critical-severity finding still open past due | Escalation to CISO for risk acceptance / compensating control / contract remedy decision |
| Vendor disputes a finding | Routed to TPRM Program Manager for adjudication before escalation |

## Notes at This Checkpoint

- **CAP-01 (F-IAM-02, Critical/Critical Security finding)** was closed 4 days ahead of its 30-day deadline - appropriately prioritized given its severity and label.
- **CAP-02 (F-DSP-02, High)** is the only High-severity item still open; it is tracking to its original 90-day deadline and does not currently require escalation.
- No CAP has missed its treatment deadline as of this checkpoint.


