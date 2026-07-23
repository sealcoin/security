# Triage Guide

This internal guide keeps GitHub Private Vulnerability Reporting handling consistent for the SEALCOIN Security Research Program.

## Intake

1. Aim to acknowledge complete reports within 2 business days.
2. Confirm the report is private and contains reproduction details.
3. Ask for missing information once, clearly and specifically.

## Validation

Check whether the report is in scope, reproducible, original, and security-impacting. Do not run unsafe PoCs against production without owner approval.

Assign severity only after exploitability and impact have been validated. SEALCOIN may internally classify reports as Informational, Low, Moderate, High, or Critical. Informational is an internal classification only; GitHub Security Advisories use Low, Moderate, High, and Critical.

Use the native GitHub workflow:

| Lifecycle State | Meaning |
|---|---|
| Open private vulnerability report | Received and awaiting initial review |
| Needs information | Maintainers request specific missing details in comments |
| Accepted as Draft Security Advisory | Validated vulnerability under remediation |
| Closed | Duplicate, known issue, out of scope, insufficient detail, or not reproducible |
| Published | Remediation and coordinated disclosure completed, where applicable |

## Shared or Affiliated Infrastructure

When a report concerns shared corporate infrastructure or an affiliated-company domain:

1. Identify the legal and technical owner.
2. Determine whether an explicitly in-scope SEALCOIN asset is directly affected.
3. Assign the report internally to the relevant SEALCOIN, IT, SEALSQ, or WISeKey owner.
4. Do not promise a reward before ownership, impact, and program eligibility are confirmed.
5. Preserve the original submission timestamp in case the issue is later accepted by the appropriate program or entity.

## Duplicates

The first complete, reproducible report is normally the eligible report. Link later duplicates to the original private report when possible and thank the researcher without sharing another researcher's details.

## Priority

| Severity | Internal Priority | Target Handling |
|---|---|---|
| Critical | P0 | Immediate owner assignment and mitigation plan |
| High | P1 | Prioritize owner assignment as soon as practical |
| Moderate | P2 | Schedule remediation in normal security backlog |
| Low | P3 | Fix opportunistically or document acceptance |
| Informational | P4 | Acknowledge or close |

## Communication

Keep messages short and specific:

- Confirm receipt
- State what is being validated
- Ask for missing reproduction details
- Share severity and eligibility decisions when ready
- Provide remediation status when there is meaningful progress, or periodically for accepted reports under active remediation
- Agree on disclosure timing before public release

## Reward Decision

Base rewards on severity, asset criticality, exploitability, report quality, duplicate status, and safe conduct. Record the decision, rationale, USD-equivalent amount, QAIT payment handling, and any legal or compliance blocker internally or in the private advisory discussion.

Do not request payment details in public issues.
