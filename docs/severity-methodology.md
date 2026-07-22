# Severity Methodology

SEALCOIN uses CVSS as a reference, then adjusts severity for Web3-specific impact, asset criticality, exploitability, and the affected environment.

## Severity Levels

| Severity | Typical CVSS Range | SEALCOIN Interpretation |
|---|---:|---|
| Informational | 0.0 | No direct security impact or best-practice observation |
| Low | 0.1 - 3.9 | Limited impact, constrained exploitability, or low-value asset |
| Medium | 4.0 - 6.9 | Practical impact requiring conditions or limited privilege |
| High | 7.0 - 8.9 | Significant compromise of users, funds, data, contracts, or infrastructure |
| Critical | 9.0 - 10.0 | Systemic compromise, fund loss, unauthorized mint/release, account takeover at scale, or privileged infrastructure compromise |

## Web3 Adjustments

SEALCOIN may increase severity when a vulnerability affects:

- User funds or token supply
- PoSy accounting, rewards, penalties, or pool integrity
- Bridge mint, burn, lock, release, replay, or message verification
- Admin, signer, deployer, treasury, upgrade, or emergency controls
- Wallet signing, transaction approval, or user consent boundaries
- Marketplace settlement, pricing, or ownership records
- Production credentials, CI/CD, release channels, or infrastructure

SEALCOIN may reduce severity when impact is limited to testnet, requires unrealistic assumptions, needs already-compromised accounts, or affects only documentation or non-sensitive metadata.

## Examples

| Area | Example | Likely Severity |
|---|---|---|
| PoSy | Unauthorized reward claim from another participant's pool position | High to Critical |
| PoSy | Incorrect pool occupancy display with no financial effect | Low |
| Bridge | Replayable message that releases tokens twice | Critical |
| Bridge | Missing event emission with no state or accounting impact | Informational to Low |
| Marketplace | User can modify another user's active order | High |
| Marketplace | Price display rounding issue with no settlement impact | Low |
| Wallet | Bypass of transaction confirmation before signing | Critical |
| Wallet | UI-only wallet address truncation confusion | Low to Medium |
| SEALCOIN Platform | Cross-tenant admin access | Critical |
| SEALCOIN Platform | Reflected XSS in a non-authenticated marketing page | Low |
| Public APIs | IDOR exposing sensitive user or organization data | High |
| Infrastructure | Valid production deploy key exposed in CI logs | Critical |

Severity is not final until SEALCOIN validates exploitability, affected assets, and business impact.
