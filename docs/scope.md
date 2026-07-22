# Program Scope

This scope defines assets eligible for responsible disclosure review under the SEALCOIN Security Research Program.

## Asset Table

| Asset | Description | In Scope | Reward Eligible | Comments |
|---|---|---:|---:|---|
| SEALCOIN Platform | User, organization, marketplace, wallet, device, and PoSy workflows operated by SEALCOIN | Yes | Yes | Includes authentication, authorization, tenant isolation, business logic, and sensitive data exposure |
| Public APIs | Internet-accessible APIs published or operated by SEALCOIN | Yes | Yes | Includes API auth, access control, rate-limit bypass with practical impact, and data exposure |
| SEALCOIN Agent | Agent software, integrations, or update channels explicitly published by SEALCOIN | Yes | Yes | Local-only issues require realistic impact beyond the researcher's own device |
| PoSy smart contracts | SEALCOIN PoSy contracts on supported testnet or mainnet deployments | Yes | Yes | Includes accounting, rewards, locking, withdrawals, pool administration, signatures, and access control |
| Bridge smart contracts | Bridge contracts and message verification components controlled by SEALCOIN | Yes | Yes | Includes mint, burn, lock, release, replay, chain validation, and verifier logic |
| SEALCOIN-operated infrastructure | Cloud, deployment, CI/CD, DNS, storage, and edge services directly operated by SEALCOIN | Yes | Yes | Only systems owned or administered by SEALCOIN are in scope |
| Public SEALCOIN websites | Official SEALCOIN or QAIT websites and web applications | Yes | Usually | Reward eligibility requires practical security impact |
| Third-party dependencies | Wallets, exchanges, explorers, RPC providers, SaaS tools, browsers, and infrastructure not controlled by SEALCOIN | No | No | Report these to the relevant owner unless they create direct risk to an in-scope SEALCOIN asset |
| Public documentation | This repository and public documentation | Yes | Usually no | Documentation issues are welcome but normally not reward eligible |

## Shared and Affiliated Infrastructure

| Asset or infrastructure | In Scope | Reward Eligible | Notes |
|---|---:|---:|---|
| DNS and subdomains under `sealcoin.ai` | Yes | Case by case | Eligible when the issue creates a practical security impact on a SEALCOIN asset |
| `qait.ch` and its official subdomains | Yes | Case by case | Subject to ownership and operational control |
| Shared email, SSO, certificate, Cloudflare, or corporate IT infrastructure | Case by case | Case by case | Only when the report directly compromises a SEALCOIN-controlled asset, user, credential, or operation |
| `sealsq.com` | No | No | Belongs to another group entity and is outside the SEALCOIN program |
| `wisekey.com` | No | No | Belongs to another group entity and is outside the SEALCOIN program |
| `wiseid.com` | No | No | Outside scope unless explicitly listed later |
| `wisesat.space` | No | No | Outside scope unless explicitly listed later |
| Other affiliated-company assets | No | No | May be forwarded internally to the appropriate owner |

Reports affecting assets of affiliated companies may be forwarded internally to the appropriate security or IT owner, but they are not eligible under the SEALCOIN Security Research Program unless they demonstrate a direct and material compromise of an explicitly in-scope SEALCOIN asset.

## In-Scope Examples

- Authentication bypass or account takeover in the SEALCOIN Platform
- Cross-tenant access to organization data
- Unauthorized wallet, marketplace, device, or PoSy actions
- Public API authorization flaws exposing sensitive data or privileged actions
- SEALCOIN Agent update, signing, or trust-boundary vulnerabilities
- PoSy accounting errors affecting rewards, penalties, pool capacity, or balances
- Bridge replay, verifier bypass, domain validation, or unauthorized mint/release flaws
- Exposed production secrets for SEALCOIN-operated systems
- Subdomain takeover of an official SEALCOIN-controlled domain

## Out of Scope

The following are out of scope unless they demonstrate concrete impact on an in-scope SEALCOIN-controlled asset:

- Third-party wallets, browsers, exchanges, explorers, RPC providers, bridges, or infrastructure
- Generic scanner output without validation
- Missing headers or cookie flags without practical exploitability
- Missing DMARC, CAA, SPF, or DNS hardening without takeover, spoofing, or account impact
- Clickjacking on pages with no sensitive action
- Self-XSS, logout CSRF, or issues requiring victim self-compromise
- Denial-of-service attacks relying on excessive traffic, volumetric load, or resource exhaustion
- Rate limiting observations without bypass or material security impact
- Social engineering, phishing, spam, coercion, or physical attacks
- Malware, persistence, destructive testing, or tests that affect other users
- Vulnerabilities requiring compromised user devices, malicious extensions, or privileged internal access
- Best-practice recommendations without exploitability
- Previously known, already reported, or publicly disclosed issues

## Environments

Reports should state whether the issue affects production, staging, testnet, mainnet smart contracts, websites, APIs, or SEALCOIN Agent integrations.

Testing must not disrupt production systems, alter real user data, or affect assets outside this scope.
