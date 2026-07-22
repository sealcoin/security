# Reward Policy

SEALCOIN may grant discretionary rewards for original, reproducible vulnerabilities affecting in-scope assets. Rewards are expressed as USD-equivalent amounts and may be paid in QAIT tokens.

Rewards are not guaranteed. Final eligibility and amount are determined by SEALCOIN.

## Baseline Ranges

| Severity | Indicative USD-equivalent reward |
|---|---:|
| Informational | No reward or recognition only |
| Low | $50 - $150 |
| Medium | $150 - $500 |
| High | $500 - $2,000 |
| Critical | $2,000 - $10,000 |

## Eligibility

A report is generally eligible when it:

- Affects an in-scope asset
- Is submitted privately through GitHub Private Vulnerability Reporting
- Is original and not already known to SEALCOIN
- Contains enough detail to reproduce and assess impact
- Demonstrates a credible security impact
- Follows the responsible disclosure rules in [SECURITY.md](../SECURITY.md)

## Shared or Affiliated Infrastructure

Reports affecting only SEALSQ, WISeKey, WISeID, WISeSat, or other affiliated-company assets are not eligible for a SEALCOIN reward.

A shared-infrastructure issue may be considered only when it directly and materially affects an in-scope SEALCOIN asset. The existence of a corporate relationship does not automatically place an asset within the SEALCOIN bounty scope.

Forwarding a report to another group entity does not imply acceptance, validation, or reward eligibility under the SEALCOIN program.

## First Valid Report Rule

When multiple researchers report the same vulnerability, SEALCOIN normally rewards the first report that is complete enough to reproduce and validate the issue. Earlier incomplete reports may be treated as informational if a later report provides the first usable reproduction.

## Duplicates

Duplicate reports are normally not reward eligible. SEALCOIN may still acknowledge materially useful new information, such as a clearer root cause, broader impact, or a safer fix.

## Quality Bonus

SEALCOIN may increase a reward for unusually useful reports, including:

- Minimal, reliable reproduction steps
- Safe Proof of Concept that avoids harm
- Clear business, financial, or on-chain impact
- Root-cause analysis
- Practical remediation guidance
- High-quality transaction, log, endpoint, or contract evidence

## Severity Assessment

SEALCOIN uses CVSS as a reference, adapted for Web3 impact. Severity may be adjusted for exploitability, affected funds, privilege level, ecosystem impact, regulatory exposure, asset criticality, and whether the issue affects production, testnet, or documentation only.

See [Severity Methodology](severity-methodology.md).

## Reward Reductions

Rewards may be reduced or denied for:

- Out-of-scope assets
- Known issues or duplicates
- Theoretical reports without demonstrated impact
- Automated scanner output without validation
- Excessive, destructive, or unsafe testing
- Public disclosure before remediation or agreement
- Missing reproduction steps
- Reports that require unrealistic assumptions
- Legal, sanctions, tax, AML, MiCA, or other regulatory constraints

## Common Vulnerability Classes

| Vulnerability Type | Typical Severity | Reward Eligibility | Notes |
|---|---|---|---|
| Authentication bypass | Critical | Eligible | Critical when it enables account takeover or privileged access |
| Privilege escalation | High to Critical | Eligible | Includes role, organization, admin, and tenant boundary bypass |
| Broken access control | Medium to Critical | Eligible | Severity depends on data, action, and affected asset |
| Cross-tenant data access | High to Critical | Eligible | Strong impact on SEALCOIN Platform and Public APIs |
| Business logic flaw | Medium to Critical | Eligible | Must show concrete impact, not only unexpected behavior |
| Marketplace order manipulation | High to Critical | Eligible | Includes unauthorized order changes, settlement abuse, or price manipulation |
| Wallet workflow bypass | High to Critical | Eligible | Includes unauthorized transaction approval or signing flow compromise |
| Sensitive information disclosure | Medium to Critical | Eligible | Depends on sensitivity, scale, and exploitability |
| Hardcoded secrets | Medium to Critical | Eligible | Eligible when secrets are valid or materially useful |
| Exposed private keys | Critical | Eligible | Includes deployer, admin, treasury, signer, or Bridge keys |
| Directory listing | Informational to Medium | Conditional | Eligible only with sensitive files or exploitable exposure |
| Debug endpoint exposure | Medium to High | Eligible | Higher when it leaks secrets or enables state changes |
| Server-side request forgery | Medium to Critical | Eligible | Higher with cloud metadata, internal admin, or credential access |
| Remote code execution | Critical | Eligible | Must be demonstrated safely |
| SQL/NoSQL injection | High to Critical | Eligible | Depends on data access and write capability |
| Command injection | Critical | Eligible | Avoid destructive commands in PoC |
| Cross-site scripting | Low to High | Conditional | Eligible when it affects real users, sessions, wallets, or privileged actions |
| CSRF | Low to High | Conditional | Eligible when it performs sensitive state-changing actions |
| Open redirect | Informational to Low | Usually no | Eligible only as part of account takeover, OAuth abuse, or credible exploit chain |
| CORS misconfiguration | Low to High | Conditional | Eligible when it exposes authenticated sensitive data or actions |
| Rate limiting issue | Informational to Medium | Conditional | Eligible only with abuse impact, account takeover support, or resource risk |
| Clickjacking | Informational to Low | Usually no | Eligible only for sensitive actions with realistic user impact |
| Missing DMARC | Informational | Usually no | May be considered if tied to verified takeover or account impact |
| Missing CAA | Informational | Usually no | Best-practice issue unless exploitability is demonstrated |
| Missing security headers | Informational to Low | Usually no | Requires practical exploit path |
| Subdomain takeover | Medium to High | Eligible | Must prove control without impacting users |
| Broken link hijacking | Low to Medium | Conditional | Eligible when linked from trusted SEALCOIN properties and exploitable |
| Dependency confusion | High to Critical | Eligible | Must avoid publishing malicious packages or causing execution |
| CI/CD secret exposure | High to Critical | Eligible | Includes tokens, signing credentials, deploy keys, or release channels |
| Supply-chain update compromise | High to Critical | Eligible | Includes SEALCOIN Agent or contract tooling update paths |
| Smart contract reentrancy | High to Critical | Eligible | Critical with fund loss, unauthorized withdrawal, or pool compromise |
| Smart contract access control flaw | High to Critical | Eligible | Includes unauthorized admin, mint, burn, pause, upgrade, or withdrawal |
| Smart contract accounting error | Medium to Critical | Eligible | Includes balances, rewards, penalties, and capacity calculations |
| Signature verification flaw | High to Critical | Eligible | Includes replay, malleability, domain separation, and signer validation |
| Flash loan exploit | High to Critical | Eligible | Must show credible economic impact |
| Oracle manipulation | High to Critical | Eligible | Depends on liquidity, controls, and affected value |
| Bridge verifier bypass | Critical | Eligible | Includes forged messages, validator bypass, or proof validation errors |
| Bridge replay attack | Critical | Eligible | Includes cross-chain, cross-domain, or repeated message execution |
| Unauthorized mint/burn/release | Critical | Eligible | Highest priority for Bridge and token contracts |
| Governance or admin takeover | Critical | Eligible | Includes upgrade, treasury, signer, or emergency control takeover |
| Denial of service | Low to High | Conditional | Volumetric DoS is out of scope; logic-level permanent or low-cost DoS may qualify |

## QAIT Payment Calculation

Where a reward is granted in QAIT, the number of QAIT tokens may be calculated using a reasonable market reference at the time of reward decision or payment processing, as determined by SEALCOIN.

SEALCOIN may refuse, delay, or adjust payment where required by law, regulation, sanctions screening, AML obligations, tax requirements, MiCA considerations, or internal compliance rules.
