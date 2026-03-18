# Demo — How Mycelium Protocol Works
[中文版本](demo-zh.md)

> From zero to a live Web3 wallet and merchant loyalty loop — in under 2 minutes, on your phone.

---

## User Journey: Paying at a Local Coffee Shop

### Step 1 — Create an AirAccount (no seed phrase)
A new user opens the app and registers with their phone's built-in Passkey (Face ID / fingerprint).
No password. No 12-word seed phrase. The account is a smart contract wallet (ERC-4337).

```
User: [Scans face] → AirAccount created → Wallet address assigned
Time: ~20 seconds
```

### Step 2 — Merchant scans / user scans QR
At the coffee shop, the user taps "Pay" and scans the merchant's QR code (or the merchant scans the user's code).
SuperPaymaster sponsors the gas fee — the user pays **zero ETH gas**.

```
User: Scan QR → Confirm ฿85 → Transaction sent
Gas: Sponsored by SuperPaymaster (10% protocol fee on merchant)
Chain: Ethereum L2 (Optimism / Base)
Time: ~3 seconds
```

### Step 3 — Points minted automatically
The Mycelium Protocol mints community points (mPNTs) to the user's AirAccount.
Points can be redeemed at any merchant in the coalition network — no lock-in, no expiry.

```
User: Receives 85 mPNTs → Balance visible in app
Merchant: Sees settled transaction → Points liability logged
```

### Step 4 — Redeem or share points
The user can redeem points at any partner merchant, gift them to a friend, or stake them for governance rights.
No centralized platform controls the points. No LINE, no Grab, no middleman.

---

## Infrastructure Components

### AirAccount
Smart contract wallet with zero-friction onboarding.

| Feature | Detail |
|---|---|
| Auth method | Passkey (Face ID / fingerprint) |
| Recovery | Social recovery via trusted contacts |
| Standard | ERC-4337 account abstraction |
| Gas | Sponsored via SuperPaymaster |
| Repo | [github.com/aastarcommunity/AirAccount](https://github.com/aastarcommunity/AirAccount) |

### SuperPaymaster
Decentralized gas sponsorship — merchants pay, users don't.

| Feature | Detail |
|---|---|
| Model | Merchant pre-deposits gas budget |
| Fee | 10% of gas cost to protocol treasury |
| Permissionless | Anyone can become a paymaster node |
| Repo | [github.com/aastarcommunity/SuperPaymaster](https://github.com/aastarcommunity/SuperPaymaster) |

### SDSS (Rain Computing)
Decentralized computing and storage network powering off-chain AI and data layers.

[github.com/aastarcommunity/SDSS](https://github.com/aastarcommunity/SDSS)

### CometENS
ENS-compatible name resolution for the Mycelium ecosystem.

[github.com/aastarcommunity/CometENS](https://github.com/aastarcommunity/CometENS)

### HexagonWarrior
Desktop application for community builders and node operators.

[github.com/AAStarCommunity/HexagonWarrior-Tauri](https://github.com/AAStarCommunity/HexagonWarrior-Tauri)

---

## Framework

### COS72
DAO and community tooling framework — the backbone for launching communities on Mycelium Protocol.

[github.com/MushroomDAO/COS72](https://github.com/MushroomDAO/COS72)

### Arcadia — Play2B2E Loyalty
Gamified on-chain loyalty system. Merchants issue points; users earn by engaging; points are tradeable across the network.

- [Arcadia GitHub](https://github.com/CMUBA/ArcadiaV2)
- [Arcadia Live Site](https://arcadia.cmuba.org/)

### Doris Protocol
Creator economy protocol — content value circulation and attribution.

[github.com/MushroomDAO/Doris](https://github.com/MushroomDAO/Doris)

---

## Applications

### Zu.Coffee
Community experiment born at Zuzalu — demonstrating the micro-circulation model at a real café.

- [Zu.Coffee GitHub](https://github.com/MushroomDAO/zu.coffee)
- [Zu.Coffee Website](https://zu.coffee/)

### Chiang Mai Connect
Local information discovery protocol for the Chiang Mai community — events, merchants, collaboration.

[github.com/CMUBA/ChiangMaiConnect](https://github.com/CMUBA/ChiangMaiConnect)

---

## Try It Now

| Resource | Link |
|---|---|
| AAStar Community (infra builders) | [aastar.io](https://aastar.io) |
| MushroomDAO GitHub | [github.com/MushroomDAO](https://github.com/mushroomdao) |
| Community | [Telegram](https://t.me/aastarcommunity) · [Twitter](https://x.com/aastarcommunity) |
| Governance Forum | gov.mushroom.box *(coming Phase 2)* |
