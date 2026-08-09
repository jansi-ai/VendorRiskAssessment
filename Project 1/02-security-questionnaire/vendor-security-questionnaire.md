# Vendor Security Questionnaire (Tier 1 — Critical)

**Vendor:** CloudVault Data Solutions
**Sent By:** Meridian Financial Services — GRC/TPRM Team
**Date Issued:** 2026-02-03
**Response Due:** 2026-02-24
**Frameworks Referenced:** NIST CSF 2.0, ISO/IEC 27001:2022 Annex A, SOC 2 Trust Services Criteria, CSA CAIQ v4

**Instructions to Vendor:** For each question, provide a response and reference supporting evidence (policy excerpt, screenshot, certification, audit report page) where indicated. Evidence should be labeled with the corresponding Question ID (e.g., `EVD-AC-01`).

---

## A. Organizational & Governance (GOV)

| ID | Question |
|---|---|
| Q-GOV-01 | Does your organization maintain a documented, board/executive-approved Information Security Policy, reviewed at least annually? |
| Q-GOV-02 | Do you have a dedicated CISO or equivalent security leadership role? |
| Q-GOV-03 | Do you hold current SOC 2 Type II, ISO 27001, or equivalent third-party attestation? Provide report date and scope. |
| Q-GOV-04 | Do you maintain cyber liability insurance? Provide coverage amount. |
| Q-GOV-05 | Do you conduct annual security awareness training for all employees, including phishing simulation? |

## B. Data Security & Encryption (DS)

| ID | Question |
|---|---|
| Q-DS-01 | Is customer data encrypted at rest? Specify algorithm/key length. |
| Q-DS-02 | Is customer data encrypted in transit? Specify TLS version(s) supported. |
| Q-DS-03 | Do you support customer-managed encryption keys (BYOK/HYOK)? |
| Q-DS-04 | Is Meridian's data logically or physically segregated from other tenants (multi-tenancy model)? |
| Q-DS-05 | What is your data retention and secure deletion process upon contract termination? |
| Q-DS-06 | Do you have a documented Data Loss Prevention (DLP) capability? |

## C. Access Control & Identity Management (AC)

| ID | Question |
|---|---|
| Q-AC-01 | Is multi-factor authentication (MFA) enforced for all administrative/privileged accounts? |
| Q-AC-02 | Is MFA enforced for all end-user accounts accessing Meridian data? |
| Q-AC-03 | Do you follow a least-privilege / role-based access control (RBAC) model? |
| Q-AC-04 | How frequently are user access rights reviewed/recertified? |
| Q-AC-05 | Is access revoked within a defined SLA upon employee termination? Specify SLA. |
| Q-AC-06 | Do you support SSO/SAML integration with customer identity providers? |

## D. Network & Infrastructure Security (NET)

| ID | Question |
|---|---|
| Q-NET-01 | Are firewalls and network segmentation implemented between production, staging, and corporate environments? |
| Q-NET-02 | Do you perform continuous vulnerability scanning of production infrastructure? Frequency? |
| Q-NET-03 | Do you conduct annual third-party penetration testing? Provide date of most recent test. |
| Q-NET-04 | Is intrusion detection/prevention (IDS/IPS) deployed across production environments? |
| Q-NET-05 | What cloud infrastructure provider(s) host the service (e.g., AWS, Azure, GCP)? Which regions? |

## E. Application Security & SDLC (APP)

| ID | Question |
|---|---|
| Q-APP-01 | Is a Secure Software Development Lifecycle (SSDLC) formally documented and followed? |
| Q-APP-02 | Are static (SAST) and dynamic (DAST) application security testing tools used in the CI/CD pipeline? |
| Q-APP-03 | Do you maintain a documented patch management SLA for critical vulnerabilities? Specify SLA. |
| Q-APP-04 | Is there a public bug bounty or responsible disclosure program? |

## F. Incident Response & Breach Notification (IR)

| ID | Question |
|---|---|
| Q-IR-01 | Do you maintain a documented, tested Incident Response Plan? Date of last tabletop exercise? |
| Q-IR-02 | What is your contractual breach notification SLA to customers? |
| Q-IR-03 | Have you experienced a data breach or material security incident in the last 24 months? If yes, describe and provide remediation summary. |
| Q-IR-04 | Do you maintain 24/7 security monitoring (SOC/SIEM)? In-house or outsourced? |

## G. Business Continuity & Disaster Recovery (BCDR)

| ID | Question |
|---|---|
| Q-BCDR-01 | Do you maintain a documented Business Continuity / Disaster Recovery Plan? |
| Q-BCDR-02 | What are your Recovery Time Objective (RTO) and Recovery Point Objective (RPO)? |
| Q-BCDR-03 | When was the BCDR plan last tested, and what were the results? |
| Q-BCDR-04 | Do you maintain geographically redundant backups? Backup frequency and retention? |

## H. Compliance & Legal (COMP)

| ID | Question |
|---|---|
| Q-COMP-01 | Are you compliant with GDPR and/or CCPA as applicable to data processed? |
| Q-COMP-02 | Will you execute a Data Processing Agreement (DPA) and/or Business Associate Agreement (BAA) if applicable? |
| Q-COMP-03 | Do you maintain audit logs sufficient to support a regulatory or customer audit request? Retention period? |

## I. Fourth-Party / Subprocessor Risk (SUB)

| ID | Question |
|---|---|
| Q-SUB-01 | Provide a complete list of subprocessors with access to Meridian data, and the service each provides. |
| Q-SUB-02 | Do you contractually flow down equivalent security and privacy obligations to subprocessors? |
| Q-SUB-03 | Are subprocessors subject to the same due diligence/assessment process as your organization is subject to from customers? |

## J. Physical Security (PHYS)

| ID | Question |
|---|---|
| Q-PHYS-01 | If self-hosted (non-cloud) infrastructure is used, describe physical access controls at data center facilities. |
| Q-PHYS-02 | Are data center facilities SOC 2 / ISO 27001 certified independently (e.g., AWS/Azure compliance)? |

---

*End of Questionnaire — 30 questions across 10 domains.*
