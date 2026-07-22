# Triage Guide

This internal guide keeps GitHub Private Vulnerability Reporting handling consistent for the SEALCOIN Security Research Program.

## Intake

1. Acknowledge the report within 2 business days.
2. Apply `status/new` and the most specific `category/*` label.
3. Confirm the report is private and contains reproduction details.
4. Ask for missing information once, clearly and specifically.

## Validation

Check whether the report is in scope, reproducible, original, and security-impacting. Do not run unsafe PoCs against production without owner approval.

Use `status/triaging` while validation is active. If valid, move to `status/accepted`; if not, use `status/duplicate`, `status/known`, or `status/out-of-scope`.

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
| High | P1 | Owner assignment within 2 business days |
| Medium | P2 | Schedule remediation in normal security backlog |
| Low | P3 | Fix opportunistically or document acceptance |
| Informational | P4 | Acknowledge or close |

## Labels

Use one or more category labels, one severity label after validation, and one status label. Add reward labels only after acceptance.

Recommended labels: `category/platform`, `category/api`, `category/agent`, `category/posy`, `category/bridge`, `category/website`, `category/infrastructure`, `severity/critical`, `severity/high`, `severity/medium`, `severity/low`, `severity/informational`, `status/new`, `status/triaging`, `status/accepted`, `status/duplicate`, `status/known`, `status/out-of-scope`, `status/fixed`, `status/rewarded`, `reward/pending`, `reward/paid`.

## Communication

Keep messages short and specific:

- Confirm receipt
- State what is being validated
- Ask for missing reproduction details
- Share severity and eligibility decisions when ready
- Provide remediation status at least every 30 days
- Agree on disclosure timing before public release

## Reward Decision

Base rewards on severity, asset criticality, exploitability, report quality, duplicate status, and safe conduct. Record the decision, rationale, USD-equivalent amount, QAIT payment handling, and any legal or compliance blocker.

Do not request payment details in public issues.
