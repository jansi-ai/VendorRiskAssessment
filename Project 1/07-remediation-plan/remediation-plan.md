# Remediation Plan — Corrective Action Plans (CAPs)

**Vendor:** CloudVault Data Solutions
**Tracked By:** M. Osei, GRC/TPRM Analyst 
**Plan Issued:** 2026-03-10
**Status as of:** 2026-07-15 (mid-cycle checkpoint, ahead of annual reassessment)

Each finding from `05-risk-assessment/auditor-risk-assessment.md` is assigned a Corrective Action Plan (CAP) with a named owner, target date, and verification method. Findings F-03 and F-04 are consolidated into a single CAP (CAP-03) since they share a common root cause.

| CAP ID | Finding(s) | Corrective Action | Owner | Target Date | Status | Verification Method | Actual Closure Date |
|---|---|---|---|---|---|---|---|
| CAP-01 | F-01 | Enforce MFA platform-wide as mandatory (not customer-configurable) for all end-user accounts; remove opt-out capability from tenant admin console | VP Engineering, CloudVault | 2026-04-24 (45 days) | ✅ **Closed** | Re-tested Okta policy configuration; confirmed MFA enforcement flag is now platform-level, not tenant-configurable. 100% of active accounts sampled (n=25) required MFA at login. | 2026-04-18 |
| CAP-02 | F-02 | Engage third-party firm to conduct penetration test; commit to contractual 12-month max cadence going forward | CISO, CloudVault | 2026-05-09 (60 days) | ✅ **Closed** | New penetration test report reviewed, dated 2026-04-30; no Critical/High findings open beyond internal SLA. Cadence commitment added to next contract renewal terms. | 2026-04-30 |
| CAP-03 | F-03, F-04 | Automate deprovisioning for 100% of accounts (eliminate manual/legacy process); implement automated alerting for any revocation exceeding 24-hour SLA | IT Operations Director, CloudVault | 2026-05-09 (60 days) | ✅ **Closed** | Sampled 10 subsequent deprovisioning events post-implementation; all completed within SLA (avg. 3.2 hours, fully automated). Legacy manual process retired. | 2026-05-02 |
| CAP-04 | F-05 | Conduct full DR failover test (not tabletop) and re-baseline testing cadence to every 12 months | Head of Infrastructure, CloudVault | 2026-06-08 (90 days) | ✅ **Closed** | Full failover test report reviewed, dated 2026-05-28. RTO achieved: 3h 40m (within 4h target). RPO achieved: 45min (within 1hr target). | 2026-05-28 |
| CAP-05 | F-06 | Implement application-layer DLP controls (bulk export/download monitoring and rate-limiting/alerting) | CISO, CloudVault | 2026-07-08 (120 days) | 🟡 **In Progress** | Vendor reports DLP tooling selected (Netskope) and in pilot with 20% of tenants; full rollout targeted for 2026-08-15 | — |
| CAP-06 | F-07 | Formalize and approve subprocessor due-diligence checklist; apply retroactively to existing subprocessor list | Director of Compliance, CloudVault | 2026-06-08 (90 days) | ✅ **Closed** | Approved checklist document reviewed (v1.0, approved 2026-05-20); confirmed applied retroactively to all 4 existing subprocessors with no material findings. | 2026-05-20 |
| CAP-07 | F-08 | Define and publish formal remediation SLA for Medium (60 days) and Low (90 days) severity vulnerabilities | Head of Engineering, CloudVault | 2026-06-08 (90 days) | ✅ **Closed** | Updated Vulnerability Management Standard v2.4 reviewed; SLAs now documented and reflected in ticketing system SLA fields. | 2026-06-01 |
| CAP-08 | F-09 | No CAP required — informational finding, tracked for awareness pending vendor's Q4 2026 BYOK roadmap delivery | Product Management, CloudVault | 2026-12-31 (roadmap target, not a compliance deadline) | 🔵 **Monitoring** | Will be re-verified at next annual assessment; no compensating action required at current risk tier | — |

## Remediation Status Summary

| Status | Count |
|---|---|
| ✅ Closed & Verified | 6 |
| 🟡 In Progress | 1 |
| 🔵 Monitoring (no CAP required) | 1 |
| ❌ Overdue | 0 |

## Escalation Notes

- **CAP-01 (F-01, High severity)** was prioritized and closed 7 days ahead of its 45-day target given its High inherent risk rating and Meridian's executive visibility requirement per Policy §4.
- **CAP-05** remains the only open item as of this checkpoint; it is tracking to its original target date and does not require escalation at this time. GRC will follow up for confirmation of full rollout by 2026-08-15.
- No findings required risk acceptance or contract remedy escalation to the CISO — all CAPs were accepted and resourced by CloudVault without pushback.
