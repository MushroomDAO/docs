# Tokenomics — GToken & PNTs
[中文版本](tokenomics-zh.md)

> GToken is not an investment. It is a protocol participation credential — your key to shaping the digital public goods commons.

A tribute to Bitcoin: GToken has a fixed total supply of 21 million, forever.
GToken is the community governance token with two core rights: community governance rights, and community protocol participation and usage rights.
GToken holders are recognized as protocol members — with corresponding governance rights and access to community protocol products and advanced features.
PNTs is the community utility token, serving as the base payment unit for all protocol products, following the OpenPNTs protocol.

---

## Token Issuance Goals

- **Establish community ownership:** By distributing GToken, the protocol's ownership and future direction are placed in the hands of users and community contributors.
- **Achieve self-sustainability:** Establish a community treasury managed by token holders to fund future development, operations, and community incentives — escaping dependence on the founding team.
- **Protect protocol autonomy and immutability:** Through decentralized governance, ensure the protocol's core features cannot be easily changed by any single entity, making it a truly open and fair digital public infrastructure.

---

## Token Overview

| Token | Type | Total Supply | Purpose |
|---|---|---|---|
| **GToken** | Governance | 21,000,000 (fixed, Bitcoin-inspired) | Protocol governance, role registration, community access |
| **PNTs** | Utility | 1,000,000,000 initial + 2% annual inflation | In-protocol transactions, loyalty points, service payments |
| **xPNTs** (e.g. aPNTs) | Community Utility | Each community deploys its own | Community-specific service payments (e.g., Gas sponsorship) |

---

## GToken — Governance Token

### Distribution (80% DAO / 20% Commercial Company)

| Category | % | GT Amount | Unlock |
|---|---|---|---|
| **Commercial Company** (HyperCapital /唯一商业公司) | 20% | 4,200,000 | 4-year linear, no cliff |
| **Community Treasury** (governance-controlled) | 38% | 7,980,000 | Governance proposals |
| → OpenNest new protocol incubation | (20%) | 4,200,000 | Milestone-based release |
| → 3-year contributor reward pool | (12%) | 2,520,000 | Monthly stream |
| → Operations reserve | (6%) | 1,260,000 | Governance decision |
| **Infrastructure mining** (DVT · AI nodes · IPFS) | 14% | 2,940,000 | Earned by contribution, no lock |
| **Core builders** (AAStar + AuraAI + team) | 12% | 2,520,000 | 4-year linear, 6-month cliff |
| **Cold start free exchange** (Howey-compliant) | 3% | 630,000 | Immediate, no lock |
| **Guardian airdrop** (invitation system) | 3% | 630,000 | Level-based, 6-month unlock |
| **Academic partners** (CMUBA + CMUBRC) | 5% | 1,050,000 | 4-year linear |
| **Advisors** | 3% | 630,000 | 4-year linear, 1-year cliff |
| **Ecosystem / partnerships reserve** | 2% | 420,000 | Governance decision |
| **Total** | **100%** | **21,000,000** | |

### Design Rationale

**80% DAO / 20% Commercial:** The commercial company (唯一商业公司 / loyalty alliance) holds 20% with 4-year vesting. Commercial (20%) + core builders (12%) = 32% — permanently below the 50% governance threshold, preventing centralized capture.

**Infrastructure mining (14%):** Nodes running DVT validators, community AI compute, and IPFS gateways earn GToken proportional to their verified contribution. This is not a promise — it's a meritocratic reward tracked on-chain.

**Cold start free exchange (3%):** Distributed via permissionless on-chain contract. Anyone can acquire by participating in early protocol actions. Passes the Howey Test — free distribution, no investment of money, no profit expectation.

**Guardian airdrop (3%):** Four-level invitation tree. No addresses collected. Privacy preserved. Anti-sybil via social proof.

### Burn Mechanism

Every protocol join and exit burns a configurable amount of GToken. The burn rate is set by community multisig and written into the contract. Combined with the 21M hard cap, this creates natural scarcity without inflation games.

```
User joins protocol → X GT burned
User exits protocol → Y GT burned
Burn rates configurable by community multisig (proposal + vote)
```

---

## GToken Rights

GToken has **zero financial return by design**. It grants:

### 1. Governance Rights (Core)

| Right | Details |
|---|---|
| **Proposal** | Hold/delegate ≥1% of supply to submit a MIP (Mycelium Improvement Proposal) |
| **Vote** | 1 GT = 1 vote. Quadratic voting available for select decisions |
| **Delegation** | Delegate votes to active community representatives |
| **Protocol config** | Vote on fee changes, chain support, treasury disbursements |

**Governance process:**
1. **Temperature Check** — Governance forum, ~10,000 GT informal vote
2. **Consensus Check** — Forum, ~30,000 GT required
3. **On-chain Proposal** — ≥210,000 GT to submit; 7-day voting; 4% quorum (840,000 GT); >50% to pass
4. **Timelock** — 2-day delay before execution (safety window)

### 2. Protocol Access Rights

| Right | Details |
|---|---|
| **Mint SBT** | Hold GToken to mint your cross-community Reputation SBT |
| **Register community** | Deploy community on Mycelium, run your own Paymaster |
| **Run SuperPaymaster** | Operate gas sponsorship nodes for your community |
| **Task Plaza** | Create and complete bounties |
| **Protocol launch** | Launch your own sub-protocol within the ecosystem |
| **Ecosystem priority** | Early access to OpenNest-incubated projects |

> **Disclaimer:** Priority access to OpenNest projects is not an investment recommendation. Each project is independent. Risks are borne individually. MushroomDAO bears no responsibility for third-party project performance.

---

## PNTs — Utility Token

PNTs is the protocol-level utility token and the foundational loyalty points layer.

| Parameter | Value |
|---|---|
| Initial supply | 1,000,000,000 |
| Annual inflation | 2% (adjustable by governance annually) |
| Use | In-protocol service payments · loyalty points · DEX liquidity |

### Distribution

| Category | % | Amount |
|---|---|---|
| Community treasury | 95% | 950,000,000 |
| Uniswap liquidity pool initialization | 2% | 20,000,000 |
| Genesis launch incentives | 3% | 30,000,000 |

Governance controls inflation rate and treasury release. Main uses: compute network mining rewards, DEX liquidity pools, OpenNest project incentives.

### PNTs as the Loyalty Points Layer

PNTs underpins the commercial loyalty coalition model (analogous to airline miles):
- Single issuer (protocol) → merchants are redemption agents
- Cross-merchant redemption is B2B settlement, not consumer payment
- Users experience invisible Web3: scan QR → earn/redeem points → no gas, no seed phrase

---

## xPNTs — Community Utility Tokens

Any community can deploy their own xPNTs instance via the `xPNTsFactory` contract.

**Example: aPNTs (AAStar community)**
- Backed by SuperPaymaster gas sponsorship capacity
- Price: $0.018–$0.030 / aPNTs (admin-adjustable within range)
- No tiers, no caps, permissionless
- Operators stake aPNTs to provide gasless transactions to users

---

## GToken Sale (Cold Launch)

**Starting price:** $0.15 / GT
**Price increase:** +12% per phase (triggered by revenue milestone, not token quantity)
**Payment:** USDC, USDT, WETH (Chainlink price feeds for non-stablecoin)
**Sales pool:** 680,000 GT pre-allocated (covers all 4 phases + 5% buffer)

See [Cold Launch](cold-launch-en.md) for the full tier structure and transparency commitment.

---

## Community Governance

See [DAO](dao-en.md) for the full governance structure.

GToken is the mechanism by which the Mycelium Protocol transforms from infrastructure into a **sovereign, self-driven decentralized commons** — owned by those who build and use it.

---

*License: GNU GPL v3*
*GToken contract (Sepolia): `0x9ceDeC089921652D050819ca5BE53765fc05aa9E`*
*Airdrop target date: July 4, 2027*
