# Supplier Security Assessment Workflow

**Program:** Extended Third-Party Security Assessment (Tier 1)
**Tooling Represented:** Questionnaire platform (OneTrust-style) for distribution/response capture

This document represents the operational workflow an assessor runs each supplier through. In a live program this would be tracked as a task board with statuses, assignees, and due dates per stage; here it is represented as a structured stage list for portfolio clarity.

## Workflow Stages

| Stage | Description | Typical Duration | Owner |
|---|---|---|---|
| **01 - Pre-Assessment Information** | Confirm vendor scope, tier, data sensitivity, and which of the 12 CCM domains apply based on service type | 1â€“2 days | TPRM Analyst |
| **02 - Review Supplier Record & Assign** | Review prior assessment history (if any) in the vendor record system; assign assessor and reviewer | 1 day | TPRM Program Manager |
| **03 - Business Kickoff** | Internal kickoff with the business/contract owner to confirm business context, criticality, and timeline expectations | 1 meeting | Business Owner + TPRM Analyst |
| **04 - Assessment Kickoff with Supplier** | External kickoff call with the vendor to walk through the questionnaire, explain evidence expectations, and set the response deadline | 1 meeting | TPRM Analyst |
| **05 - Generate Observations & Findings** | Independent review of vendor responses and evidence; findings drafted, classified (label + type), and scored | 5â€“10 business days | TPRM Analyst / Security Auditor |
| **06 - Remediation** | Findings shared with vendor; Corrective Action Plans issued per the treatment deadline matrix; progress tracked to closure | Per SLA (30â€“365 days by finding classification) | Vendor + TPRM Analyst |
| **07 - Closure** | Each finding independently re-verified; residual risk scored; executive summary issued; next assessment date scheduled | 5 business days | TPRM Analyst / CISO sign-off |

## Stage Detail: 05 - Generate Observations & Findings

This is the core analytical stage of the program and is where most of this portfolio's documentation lives. For each questionnaire response, the assessor:

1. Compares the vendor's answer against submitted evidence
2. Assigns a **Response Scenario**: `No`, `Yes - without evidence`, or `Yes - with partial evidence`
3. Classifies the finding: **Label** (`Critical Security finding` / `Standard finding`) and **Type** (`Missing Capability` / `Technical misconfiguration`)
4. Scores the finding severity: `Critical`, `High`, or `Moderate` (see `02-finding-classification-methodology/`)
5. Documents the specific missing requirements and the exact remediation ask

## Stage Detail: 06 - Remediation

Corrective Action Plans (CAPs) are issued with a due date calculated automatically from the finding's **Classification Ã— Type** combination (see the Treatment Deadline Matrix in `02`). Progress is tracked weekly; overdue CAPs are escalated per the escalation ladder in `07-remediation-tracking/remediation-plan.md`.

## Stage Detail: 07 - Closure

A finding is only closed once the assessor has **independently re-verified** the remediation evidence - CAP completion claimed by the vendor is not sufficient on its own. Closed findings are re-scored for residual risk in `08-closure-residual-risk/`.


