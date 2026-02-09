Open-source multi-rail Bitcoin payment infrastructure where merchants accept fiat and crypto while always receiving final settlement in bitcoin.

P2Pay is a modular, self-custodial payment architecture built on top of BTCPay Server and peer-to-peer rails.  
It is designed for censorship-resistant, high-risk and cross-border use cases.

---

## Core Principles

- **Settlement-first architecture** (bitcoin as final layer)
- **Multi-rail routing** (fiat, cards, P2P, crypto)
- **Self-custodial by default**
- **Vendor-neutral**
- **KYC-free where legally possible**
- **Designed for failure scenarios, not marketing demos**

---

## Features

- BTCPay Server integration (Greenfield API)
- Bitcoin on-chain payments
- Lightning Network support
- USDt on TRON
- Fiat-to-BTC flows via P2P rails
- Modular rail integrations (Peach, RoboSats, others)
- Single-user booking, invoicing and ecommerce flows
- API-first architecture
- Designed for embeddable deployments

---

## Target Users

- **Bitcoin-native builders** who want fiat reach without touching fiat custody  
- **High-risk legal businesses** (adult, legal cannabis, grey-zone fintech)  
- **Unbanked or sanctioned regions** lacking access to Stripe-like gateways  
- **Emerging markets** (LATAM, Africa, cross-border freelancers)  
- **Infrastructure teams** building settlement-first payment systems  

---

## Payment Rails (Architecture Overview)

### Bitcoin
- On-chain
- Lightning Network  
- No protocol-level limits  

### USDt
- TRON (via BTCPay plugin)

### Fiat (via P2P)
- Local rails aggregated through P2P platforms  
- Merchant-defined fee (typically 5–7%)  
- Per-transaction limits depend on rail  

### Cards (experimental / under evaluation)
- Redirect-based card → BTC settlement  
- KYC-free thresholds where supported  
- Architecture designed to isolate chargeback risk  

---

## Status

- Booking-first development strategy  
- Market liquidity aggregation live  
- P2P rail integrations modular and extensible  
- Credit/debit card rails under evaluation  
- Marketplace (multi-tenant) architecture planned  

---

# Active Repositories

---

## [p2pay-market](https://github.com/p2payto/p2pay-market)
Multi-rail Bitcoin P2P offer comparator and spread index.

Live deployment:  
https://market.p2pay.to

![language](https://img.shields.io/github/languages/top/p2payto/p2pay-market)
![Stars](https://img.shields.io/github/stars/p2payto/p2pay-market?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2pay-market?style=social)

---

## [p2pay-booking](https://github.com/p2payto/p2pay-booking)
Multi-rail booking system with final settlement in bitcoin.

Live deployment:  
https://booking.p2pay.to

![language](https://img.shields.io/github/languages/top/p2payto/p2pay-booking)
![Stars](https://img.shields.io/github/stars/p2payto/p2pay-booking?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2pay-booking?style=social)

---

## [robosats-nitro](https://github.com/p2payto/robosats-nitro)
Nitro server integration layer for RoboSats rail.

![language](https://img.shields.io/github/languages/top/p2payto/robosats-nitro)
![Stars](https://img.shields.io/github/stars/p2payto/robosats-nitro?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/robosats-nitro?style=social)

---

## [robosats-nuxt](https://github.com/p2payto/robosats-nuxt)
Nuxt integration layer for RoboSats authentication and client-side flows.

![language](https://img.shields.io/github/languages/top/p2payto/robosats-nuxt)
![Stars](https://img.shields.io/github/stars/p2payto/robosats-nuxt?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/robosats-nuxt?style=social)

---

## [p2p-plugin](https://github.com/p2payto/p2p-plugin)
BTCPay Server plugin enabling P2P rail integrations (Peach-based).

![language](https://img.shields.io/github/languages/top/p2payto/p2p-plugin)
![Stars](https://img.shields.io/github/stars/p2payto/p2p-plugin?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2p-plugin?style=social)

---

## Commercial advisory

This is a non-profit open-source project under active development.

For teams looking for production-ready, commercial payment architecture solutions today,
Blockchange provides independent multi-rail payment advisory:
https://www.blockchange.expert/en/#book

---

## To get support

[Wiki](https://github.com/p2payto/help/wiki)  
[Discussions](https://github.com/orgs/p2payto/discussions)


