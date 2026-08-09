# Finding Classification & Treatment Deadline Methodology

## 1. Purpose

This methodology defines how every questionnaire response is converted into a classified, scored finding with a defined remediation SLA. It is the mechanism that drives consistency across assessors and across the 12 CCM domains in scope.

## 2. Finding Label

| Label | Meaning |
|---|---|
| **Critical Security finding** (Critical Security finding - Automatic Escalation) | A gap in a control area determined by the program to carry inherent elevated risk regardless of context (e.g., MFA for privileged/remote access, incident response planning, background verification, security awareness training). Any finding under a Critical Security finding-tagged question is automatically escalated to the TPRM Program Manager for visibility, even if scored below Critical. |
| **Standard finding** | A standard finding, scored and tracked through the normal workflow without automatic escalation. |

## 3. Finding Type

| Type | Meaning | Typical Evidence |
|---|---|---|
| **Missing Capability** | The gap is in a *policy, procedure, plan, or program* - something the organization has or has not documented and operationalized. | Policies, plans, test reports, training records |
| **Technical misconfiguration** | The gap is in a *live technical control* - something that is or is not actually configured/enforced in production. | Configuration screenshots, tool exports, scan reports, live demos |

This distinction matters because a missing *policy* and a missing *live control* carry different urgency - an unconfigured control is an active exposure today, while a missing policy is a governance gap that may already be substantively covered by informal practice. The treatment deadline matrix (below) reflects this by giving Technical misconfiguration findings shorter SLAs than Missing Capability findings at every severity level.

## 4. Response Scenario

Every question is evaluated against one of three scenarios, each requiring a different closure ask:

| Scenario | Description | Remediation Ask |
|---|---|---|
| **"No"** | Vendor states the control/process does not exist | Full build-and-implement ask, with defined requirements list |
| **"Yes" - without evidence** | Vendor claims the control exists but provided no supporting evidence | Evidence-only ask - vendor already claims capability, needs to substantiate it |
| **"Yes" - with partial evidence** | Vendor provided evidence, but it does not fully demonstrate all required attributes | Gap-specific ask - only the missing attributes need to be addressed |

## 5. Severity Scoring

| Severity | Score | Criteria |
|---|---|---|
| **Critical** | 10 | Directly exposes confidential/regulated data, or represents a control the program treats as non-negotiable (e.g., no MFA on privileged access, no incident response capability) |
| **High** | 5 | Material control gap with realistic exploitation/failure path, but with some compensating factor or limited blast radius |
| **Moderate** | 1 | Governance or process maturity gap with low near-term likelihood of exploitation |

## 6. Treatment Deadline Matrix

Remediation SLA is determined by **Severity Ã— Finding Type**:

| Assessment Finding Classification | Missing Capability | Technical misconfiguration |
|---|---|---|
| **Critical (10)** | 120 days (4 months) | 30 days (1 month) |
| **High (5)** | 180 days (6 months) | 90 days (3 months) |
| **Moderate (1)** | 365 days (12 months) | 180 days (6 months) |

**Reading example:** A Critical-severity Technical misconfiguration finding (e.g., encryption not enabled in production) has a 30-day SLA, while a Critical-severity Missing Capability finding (e.g., no incident response plan at all) has a 120-day SLA - reflecting that building a program from scratch takes longer than flipping a configuration setting, even though both are Critical.

## 7. Escalation

- **Critical Security finding-labeled findings** are visible to the TPRM Program Manager immediately upon identification, regardless of severity score.
- Findings that miss their treatment deadline are escalated per the ladder in `07-remediation-tracking/remediation-plan.md`.
- Any finding still open at **Critical** severity past its SLA is escalated to the CISO for a risk acceptance, compensating control, or contract remedy decision.


