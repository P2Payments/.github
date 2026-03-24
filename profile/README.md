# P2Pay

Open-source, modular Bitcoin payment infrastructure. Accept fiat and crypto across multiple rails. Settle in bitcoin or in the stablecoin that works best for your market.

> **P2Pay is chain-agnostic.** We don't pick chains for ideology — we pick them for what actually works. The settlement layer is Bitcoin or a Bitcoin-native stablecoin, depending on what the market needs and what the best available integration supports. Today that means BTC on-chain, Lightning, and Liquid — because Liquid gives us Bitcoin-native stablecoins (USDt, BRLz, EURx, and more) without altcoin exposure. That may evolve. The principle won't.

---

## Core Principles

- **Settlement-first** — bitcoin or a Bitcoin-native stablecoin is the final layer
- **Chain-agnostic** — best rail wins, always
- **Multi-rail** — fiat, cards, P2P, and crypto as entry rails
- **Self-custodial by default**
- **Vendor-neutral**
- **KYC-free where legally possible**
- **Built for failure scenarios, not demo environments**
- **MIT licensed. Forever open.**

---

## Rail Integrations

| Rail | Status | Notes |
|------|--------|-------|
| BTC on-chain | ✅ Live | Via BTCPay Server |
| Lightning | ✅ Live | Via BTCPay Server · Boltz swaps |
| Liquid Network | ✅ Live | USDt, BRLz, EURx, L-BTC · Aqua wallet · SamRock Protocol for BTCPay linking |
| Peach P2P | ✅ Live | KYC-free BTC rail |
| RoboSats P2P | ✅ Live | Lightning-native P2P exchange |
| Credit / debit card | 🔄 In progress | Up to $800 KYC-free via Guardarian |
| Russian local payment methods | 🔄 In progress | 4 methods · up to $1,000 |
| ueno / uPay / uPOS | 📋 Planned | Local rails via Moonshot grant |

---

## Active Repositories

### [mono](https://github.com/p2payto/mono)
Main repository. Core application logic, rail integrations, payment flows, dashboard, and mini-app surfaces. Active development happens here.

### [wallet](https://github.com/p2payto/wallet)
Mobile wallet forked from Aqua. Merchant-controlled signing and self-custodial flows. Liquid-native by default. Part of the P2Pay architecture, not a standalone product.

### [miniapp](https://github.com/p2payto/miniapp)
Upcoming Nuxt mini app embedded in the wallet. Extends P2Pay payment flows through a wallet-native interface.

---

## Who This Is For

P2Pay exists for cases where traditional payment stacks break down:

- merchants that need fiat reach without fiat custody
- cross-border businesses with unreliable banking access
- high-risk but fully legal industries
- users in emerging markets
- builders who want modular Bitcoin-native payment infrastructure

If payment platforms work fine for you, P2Pay is not for you. If they don't, this is yours.

---

## Community

- [GitHub Discussions](https://github.com/orgs/p2payto/discussions)
- [Telegram](https://t.me/P2PayTo)

---

## Commercial Advisory

Commercial architecture advisory, integration design, and implementation support available separately via [Blockchange](https://blockchange.expert).

For teams looking for production-ready, commercial payment architecture solutions today,
Blockchange provides independent multi-rail payment advisory:
https://www.blockchange.expert/en/#book



