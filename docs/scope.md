# Program Scope

## In scope

### SEALCOIN Platform

- Authentication and authorization flaws
- Privilege escalation
- Organization or tenant isolation bypass
- Wallet workflow vulnerabilities affecting user funds
- Marketplace order manipulation
- Device onboarding and certificate lifecycle vulnerabilities
- PoSy pool business-logic vulnerabilities
- API vulnerabilities with material security impact

### PoSy smart contracts

- Unauthorized token locking, withdrawal, reward claiming, or pool administration
- Incorrect accounting of pool capacity, occupancy, rewards, penalties, or participant balances
- Access-control bypass
- Economic logic flaws with direct security or financial impact
- Reentrancy, replay, signature verification, or validation flaws where applicable

### Bridge smart contracts

- Unauthorized minting, burning, locking, or release of tokens
- Message verification flaws
- Replay attacks
- Incorrect chain/domain validation
- Access-control bypass
- Critical economic or accounting flaws

### Websites and public infrastructure

- Vulnerabilities affecting official SEALCOIN or QAIT websites
- Account takeover paths
- Sensitive information disclosure
- Server-side vulnerabilities with credible impact

## Out of scope

The following are generally out of scope unless they demonstrate a concrete, exploitable impact on SEALCOIN-controlled assets:

- Vulnerabilities in third-party wallets, browsers, exchanges, bridges, explorers, RPC providers, or infrastructure not controlled by SEALCOIN
- Generic scanner output without analysis
- Missing security headers without practical impact
- Best-practice recommendations without exploitability
- Denial-of-service attacks relying on excessive traffic or resource exhaustion
- Social engineering, phishing, spam, or physical attacks
- Attacks requiring compromised user devices, malware, or malicious browser extensions
- Issues requiring unrealistic assumptions or privileged internal access
- Previously known or already reported vulnerabilities
- Publicly disclosed vulnerabilities before SEALCOIN has been notified privately

## Environments

Reports should clearly state whether they affect:

- Production
- Staging
- Testnet
- Mainnet smart contracts
- Website
- API
- Agent integration

Testing must not disrupt production systems or affect real users.
