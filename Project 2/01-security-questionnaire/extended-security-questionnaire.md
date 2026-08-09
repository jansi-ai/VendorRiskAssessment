# Extended Third-Party Security Assessment Questionnaire

**Vendor:** Vantage Cloud Systems
**Issued By:** Solstice Technologies Inc. - TPRM Program
**Framework:** CSA Cloud Controls Matrix (CCM) v4
**Date Issued:** 2026-03-02
**Response Due:** 2026-03-23

**Instructions to Vendor:** Answer each question and attach supporting evidence referencing the Question ID (e.g., `EVD-IAM-02`). Each question below lists its **Finding Name**, **Label**, and **Type** - these drive how any gap identified will be classified and scored if your response or evidence does not fully satisfy the requirement.

---

## BCR - Business Continuity Management & Operational Resilience

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-BCR-01 | Are business continuity management and operational resilience policies and procedures in place, including a documented BCP with recovery objectives (RTO/RPO), scope, and roles/responsibilities? | Business Continuity Plan | Standard finding | Missing Capability |
| Q-BCR-02 | Are the business continuity and operational resilience plans exercised and tested at least annually, and when significant changes occur? | Business Continuity Exercises | Standard finding | Missing Capability |

## CCC - Change Control & Configuration Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-CCC-01 | Are risk management policies and procedures associated with changes to organizational assets (applications, systems, infrastructure, configuration) implemented and maintained? | Change Management Policy & Procedures | Standard finding | Missing Capability |
| Q-CCC-02 | Are all production changes formally reviewed, tested, and approved (e.g., via a Change Advisory Board or equivalent) prior to deployment? | Change Approval Process | Standard finding | Missing Capability |

## CEK - Cryptography, Encryption & Key Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-CEK-01 | Are cryptography, encryption, and key management policies implemented and maintained (key storage, rotation, crypto-periods, approved algorithms)? | Cryptographic Key Management | Standard finding | Missing Capability |
| Q-CEK-02 | Is data at rest and in transit cryptographically protected using approved standards (e.g., AES-256, TLS 1.2+)? | Data at Rest and in Transit | Standard finding | Technical misconfiguration |

## DCS - Datacenter Security

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-DCS-01 | Are physical and logical assets classified and documented based on organizational business risk? | Asset Risk Classification | Standard finding | Missing Capability |
| Q-DCS-02 | Is physical access to facilities hosting infrastructure controlled, logged, and reviewed? | Physical Access Control | Standard finding | Missing Capability |

## DSP - Data Security & Privacy Lifecycle Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-DSP-01 | Are policies and procedures in place for the classification, protection, and handling of data throughout its lifecycle, including a maintained data flow diagram? | Data Security & Privacy Lifecycle Management | Standard finding | Missing Capability |
| Q-DSP-02 | Are Data Loss Prevention (DLP) controls implemented to prevent unauthorized exfiltration of confidential data? | Data Loss Prevention | Standard finding | Technical misconfiguration |

## HRS - Human Resources Security

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-HRS-01 | Are background verification policies and procedures in place for all new employees, including remote employees, contractors, and third parties? | Background Verification | Standard finding | Missing Capability |
| Q-HRS-02 | Is a security awareness training program implemented for all employees, including annual cadence, phishing-relevant content, and a comprehension assessment? | Security Awareness Training | **Critical Security finding** | Missing Capability |

## IAM - Identity & Access Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-IAM-01 | Are identity and access management policies and procedures implemented and maintained (unique IDs, authentication requirements, least-privilege authorization, password policy)? | Identity and Access Management Policy | Standard finding | Missing Capability |
| Q-IAM-02 | Is multi-factor authentication (MFA) enforced for all privileged accounts and all remote access to company infrastructure? | Privileged & Remote Access MFA | **Critical Security finding** | Technical misconfiguration |

## IVS - Infrastructure & Virtualization Security

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-IVS-01 | Is every operating system, hypervisor, and infrastructure control plane hardened to a documented security baseline? | Security Baseline / Hardening Standard | Standard finding | Missing Capability |
| Q-IVS-02 | Is network segmentation documented (diagram showing zones, ACLs, and confidential-data-handling zones), reviewed at least annually? | Network Segmentation | Standard finding | Missing Capability |

## LOG - Logging & Monitoring

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-LOG-01 | Are logging and monitoring policies and procedures established, defining event types logged, retention period, and review cadence? | Logging and Monitoring Policy | Standard finding | Missing Capability |
| Q-LOG-02 | Does a centralized log management platform generate tamper-protected, NTP-synchronized audit records capturing login failures, privileged activity, and anomalous events? | Security Event Logging | **Critical Security finding** | Technical misconfiguration |

## SEF - Security Incident Management, E-Discovery & Cloud Forensics

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-SEF-01 | Is a security incident response plan established covering roles/responsibilities, notification protocols, containment, and breach notification requirements? | Incident Response Plan | **Critical Security finding** | Missing Capability |
| Q-SEF-02 | Is the security incident response plan tested at planned intervals (e.g., annual tabletop or live exercise)? | Incident Response Testing | Standard finding | Missing Capability |

## TVM - Threat & Vulnerability Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-TVM-01 | Are policies and procedures implemented to identify, report, and prioritize remediation of vulnerabilities, including a defined scanning program? | Vulnerability Management Policy & Program | **Critical Security finding** | Missing Capability |
| Q-TVM-02 | Are vulnerability scans authenticated and run at least monthly against production infrastructure? | Authenticated Scan Frequency | Standard finding | Technical misconfiguration |

## UEM - Universal Endpoint Management

| ID | Question | Finding Name | Label | Type |
|---|---|---|---|---|
| Q-UEM-01 | Are anti-malware detection and prevention (EDR) technologies configured and actively monitored on all managed endpoints? | Anti-Malware / EDR | Standard finding | Technical misconfiguration |
| Q-UEM-02 | Is storage encryption enabled on all managed endpoints to protect data from unauthorized disclosure? | Endpoint Storage Encryption | Standard finding | Technical misconfiguration |

---

*End of Questionnaire - 24 questions across 12 CCM domains.*


