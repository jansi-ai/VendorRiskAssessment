# Third-Party / Vendor Risk Management Policy

**Document Owner:** GRC / Information Security Team
**Applies To:** Meridian Financial Services 
**Version:** 1.2
**Effective Date:** 2026-01-15
**Review Cycle:** Annual

## 1. Purpose

This policy establishes the requirements for identifying, assessing, monitoring, and managing information security and compliance risks introduced by third-party vendors and service providers that access, process, store, or transmit Meridian data, or that connect to Meridian systems.

## 2. Scope

Applies to all third parties, including SaaS providers, cloud hosting providers, managed service providers, and subcontractors ("fourth parties") who:

- Store, process, or transmit Meridian confidential, PII, or regulated data
- Connect to Meridian's network or systems
- Provide services supporting a critical business process

## 3. Vendor Risk Tiering

| Tier | Criteria | Assessment Frequency | Assessment Depth |
|---|---|---|---|
| **Tier 1 — Critical** | Access to confidential/regulated data, or supports a critical business process; no readily available substitute | Annual | Full questionnaire + evidence review + on-site/virtual audit option |
| **Tier 2 — High** | Access to internal or confidential data; not mission-critical | Annual | Full questionnaire + evidence review |
| **Tier 3 — Moderate** | Limited data access, non-critical function | Every 2 years | Abbreviated questionnaire |
| **Tier 4 — Low** | No data access, no system connectivity | Onboarding only | Self-attestation |

CloudVault Data Solutions (this repository's scenario vendor) is classified **Tier 1 — Critical** due to storage of customer PII and financial records.

## 4. Assessment Lifecycle

1. **Scoping & Tiering** — Business owner and GRC jointly determine tier at onboarding.
2. **Questionnaire Distribution** — Standardized questionnaire issued based on tier (see `02-security-questionnaire/`).
3. **Response & Evidence Collection** — Vendor submits responses and supporting evidence (SOC 2 report, pen test summary, policies, certifications).
4. **Independent Assessment** — GRC/security analyst reviews responses against evidence, tests control claims, and documents findings.
5. **Risk Scoring** — Each finding is scored using the inherent risk matrix (Likelihood × Impact).
6. **Remediation** — Findings above the acceptable risk threshold require a Corrective Action Plan (CAP) with an owner and due date.
7. **Residual Risk Rating** — Upon CAP closure (or acceptance of risk), residual risk is re-scored.
8. **Approval / Risk Acceptance** — Findings rated **Critical** or **High** residual risk require formal sign-off from the CISO or designated risk owner before contract execution or renewal.
9. **Continuous Monitoring** — Tier 1/2 vendors are subject to annual reassessment, contract-triggered reassessment, and ad hoc reassessment following a reported breach or material change in service.

## 5. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| **Business/Contract Owner** | Initiates vendor engagement, provides business context, participates in risk acceptance |
| **GRC / TPRM Analyst** | Issues questionnaire, reviews evidence, drafts risk assessment and findings |
| **Security Auditor / Assessor** | Independently validates controls, assigns risk ratings, documents findings |
| **CISO / Risk Owner** | Approves risk acceptance for Critical/High residual risk; final sign-off authority |
| **Vendor** | Completes questionnaire accurately, provides evidence, remediates findings per CAP |

## 6. Minimum Control Expectations (Tier 1 Vendors)

- Independent third-party audit report (SOC 2 Type II or ISO 27001 certificate) issued within the last 12 months
- Data encrypted at rest (A  ES-256 or equivalent) and in transit (TLS 1.2+)
- Documented incident response plan with breach notification SLA ≤ 72 hours
- Multi-factor authentication enforced for all privileged and remote access
- Documented business continuity / disaster recovery plan tested within the last 12 months
- Subprocessor (fourth-party) inventory disclosed and flowed down equivalent security obligations

## 7. Non-Compliance

Vendors that fail to meet minimum control expectations and decline or fail to remediate within agreed CAP timelines are escalated to the CISO for a risk acceptance, compensating control, or contract termination decision.

## 8. Related Documents

- `02-security-questionnaire/` — Vendor Security Questionnaire
- `06-risk-scoring/` — Risk Scoring Methodology
- Data Classification Policy *(not included in this portfolio)*
- Incident Response Policy *(not included in this portfolio)*
