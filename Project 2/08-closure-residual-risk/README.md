# Extended Third-Party Security Assessment Program - CSA CCM Domain-Based TPRM Portfolio

## What this repository is

This is a portfolio artifact demonstrating a **structured, multi-domain supplier security assessment program**, modeled on how mature enterprise Third-Party Risk Management (TPRM) teams run vendor security reviews against the **Cloud Security Alliance Cloud Controls Matrix (CSA CCM v4)** - the same domain taxonomy used by CAIQ-based supplier questionnaires industry-wide.

It is a companion piece to the `tprm-portfolio` repository in this profile (which walks a single-vendor lifecycle end to end). This repository instead demonstrates depth across **12 control domains**, a **formal finding classification & SLA methodology**, and the **operational workflow** an assessor runs a supplier through from kickoff to closure.

** Disclaimer:** All company names, vendor names, personnel, tool names, findings, and data in this repository are **fictional**, created solely to demonstrate GRC/TPRM methodology and documentation standards for a job application portfolio. No real organization, individual, or vendor is represented.

## Scenario

| | |
|---|---|
| **Assessing Organization** | Solstice Technologies Inc. (fictional enterprise SaaS company) |
| **Vendor Under Review** | Vantage Cloud Systems (fictional cloud-hosted ERP / business systems provider) |
| **Assessment Program** | Extended Third-Party Security Assessment - Tier 1 Supplier |
| **Framework** | CSA Cloud Controls Matrix (CCM) v4 - 12 domains in scope |
| **Assessment Channel** | Questionnaire platform (e.g., OneTrust / Archer / ServiceNow) + live evidence review + workflow tracking  |
  
## How to Read This Repository

Unlike a simple pass/fail checklist, this program classifies every question by:
- **Finding Label** - `Critical Security finding` (Critical Security finding - Automatic escalation) vs. `Standard finding` (standard finding)
- **Finding Type** - `Missing Capability` (a missing policy/process) vs. `Technical misconfiguration` (a missing or unverified technical control)
- **Response Scenario** - every question has three possible supplier response patterns tracked separately: *"No"*, *"Yes" without evidence*, and *"Yes" with partial evidence* - each requiring a different remediation ask

This classification then drives **risk scoring and treatment deadlines** (`02`, `06`), so a Critical Missing Capability finding gets a different SLA than a Critical Technical misconfiguration finding - this is the core mechanic of the program.

## Repository Structure

```
tprm-ccm-portfolio/
README.md                                    <- You are here
00-program-overview/                         <- Assessment workflow (kickoff â†’ closure)
01-security-questionnaire/                   <- 12-domain CCM-aligned questionnaire
02-finding-classification-methodology/       <- Classification rules + treatment deadline matrix
03-vendor-responses/                         <- Vendor's completed questionnaire responses
04-evidence-repository/                      <- Evidence log, MFA solutions inventory, vuln tool inventory
05-risk-assessment-findings/                 <- Auditor's findings, classified and labeled
06-risk-scoring/                              <- risk-register.xlsx - classification-driven scoring + auto SLA
07-remediation-tracking/                      <- CAPs tracked against the treatment deadline matrix
08-closure-residual-risk/                     <- Finding closure verification & residual risk summary
09-executive-summary/                         <- Leadership summary & sign-off
```

## Domains Covered (CSA CCM v4)

| Code | Domain |
|---|---|
| BCR | Business Continuity Management & Operational Resilience |
| CCC | Change Control & Configuration Management |
| CEK | Cryptography, Encryption & Key Management |
| DCS | Datacenter Security |
| DSP | Data Security & Privacy Lifecycle Management |
| HRS | Human Resources Security |
| IAM | Identity & Access Management |
| IVS | Infrastructure & Virtualization Security |
| LOG | Logging & Monitoring |
| SEF | Security Incident Management, E-Discovery & Cloud Forensics |
| TVM | Threat & Vulnerability Management |
| UEM | Universal Endpoint Management |

## Suggested Reading Order

1. Start with `00-program-overview/assessment-workflow.md` to see the end-to-end process
2. Read `02-finding-classification-methodology/` before the findings - it explains the scoring logic everything downstream depends on
3. Follow one finding (e.g., **F-IAM-01**, MFA enforcement) through `01` â†’ `03` â†’ `04` â†’ `05` â†’ `06` â†’ `07` â†’ `08` to see the full trace
4. Finish with `09-executive-summary/` for the leadership-level view

## Skills Demonstrated

- Designing a domain-based (CSA CCM) supplier questionnaire with structured finding taxonomy
- Multi-scenario response handling (no answer / unverified claim / partial evidence)
- SLA-driven remediation methodology tied to finding severity *and* finding type
- Evidence inventory management (including cross-supplier tooling registers - MFA solutions, vulnerability scanning tools)
- End-to-end assessment workflow design (kickoff, evidence collection, findings, remediation, closure)
- Executive risk reporting and sign-off documentation


