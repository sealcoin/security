# Program Scope

This scope defines assets eligible for responsible disclosure review under the SEALCOIN Security Research Program.

## Asset Table

| Asset | Description | In Scope | Reward Eligible | Comments |
|---|---|---:|---:|---|
| SEALCOIN Platform | `https://platform.sealcoin.ai/` | Yes | Yes | Includes authentication, authorization, tenant isolation, business logic, wallet workflows, and sensitive data exposure |
| SEALCOIN Platform API | `https://api.platform.sealcoin.ai` | Yes | Yes | Includes API authentication, authorization, access control, rate-limit bypass with practical impact, and data exposure |
| Bridge web application | `https://bridge.platform.sealcoin.ai/` | Yes | Yes | Includes bridge user flows, transaction preparation, wallet connection, and user consent boundaries |
| SEALCOIN website | `https://sealcoin.ai/` | Yes | Usually | Reward eligibility requires practical security impact |
| QAIT website | `https://www.qait.ch/` | Yes | Usually | Reward eligibility requires practical security impact |
| Spacedrop website | `https://spacedrop.sealcoin.ai/` | Yes | Usually | Reward eligibility requires practical security impact |
| SEALCOIN Agent | Not publicly available | No | No | Agent issues are eligible only after SEALCOIN publishes an explicit Agent build, integration, or update channel in this scope |
| QAIT HTS token | `0x0000000000000000000000000000000000992f8e` | Yes | Yes | Hedera Token Service token |
| QAITHTSConnector | `0x00000000000000000000000000000000009c1fcc` | Yes | Yes | Includes token connector logic, access control, and cross-chain accounting impact |
| QAITOFT on BSC | `0x4d41A5d412f4Ef44A35b9f53b06DB65edE249493` | Yes | Yes | Includes mint, burn, lock, release, replay, chain validation, and verifier logic |
| QAITOFT on Base | `0x0c9147701Ea8B0EFDdbe6a0E3950d922227Dd19b` | Yes | Yes | Includes mint, burn, lock, release, replay, chain validation, and verifier logic |
| QAITOFT on Ethereum | `0x2C9A0895A18c6ba7404E86bC5aEc0518f859181A` | Yes | Yes | Includes mint, burn, lock, release, replay, chain validation, and verifier logic |
| PoSy smart contract | `0x27d9b4c0ff7d39a07cd45d91a526605f6eb8a5a0` | Yes | Yes | Includes accounting, rewards, locking, withdrawals, pool administration, signatures, and access control |
| QAITVesting | `0x502bad06e848b239f2cb4be1649acc694d4c46d1` | Yes | Yes | Includes vesting accounting, release logic, authorization, and admin controls |
| SEALCOIN-operated infrastructure | Cloud, deployment, CI/CD, DNS, storage, and edge services directly operated by SEALCOIN | Yes | Yes | Only systems owned or administered by SEALCOIN are in scope |
| Third-party dependencies | Wallets, exchanges, explorers, RPC providers, SaaS tools, browsers, and infrastructure not controlled by SEALCOIN | No | No | Report these to the relevant owner unless they create direct risk to an in-scope SEALCOIN asset |
| Public documentation | This repository and `https://github.com/sealcoin/public-documentation` | Yes | Usually no | Documentation issues are welcome but normally not reward eligible |

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
- Platform API authorization flaws exposing sensitive data or privileged actions
- Unauthorized wallet, marketplace, device, or PoSy actions
- PoSy accounting errors affecting rewards, penalties, pool capacity, or balances
- Bridge replay, verifier bypass, domain validation, or unauthorized mint/release flaws
- Vesting release, accounting, or access-control flaws
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

Reports should state whether the issue affects production, staging, testnet, mainnet smart contracts, websites, APIs, or another explicitly listed asset.

Testing must not disrupt production systems, alter real user data, or affect assets outside this scope.
