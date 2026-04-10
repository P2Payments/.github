[Español](https://github.com/P2Payments/.github/blob/main/profile/README.es.md) | [Português](https://github.com/P2Payments/.github/blob/main/profile/README.pt.md) | [Русский](https://github.com/P2Payments/.github/blob/main/profile/README.ru.md) | [Français](https://github.com/P2Payments/.github/blob/main/profile/README.fr.md) | [Italiano](https://github.com/P2Payments/.github/blob/main/profile/README.it.md)

# P2Payments

Open-source, modular payment infrastructure built around Bitcoin- and stablecoin-based settlement, designed to enable more frictionless integration and payment flows across markets and rails. It uses [BTCPay Server](https://github.com/btcpayserver/btcpayserver) as the backend, an [Aqua Wallet](https://github.com/AquaWallet/aqua-wallet) fork for self-custodial settlement, and is primarily built with [Nuxt](https://github.com/nuxt/nuxt) and [Nitro](https://github.com/nitrojs/nitro).

P2Payments combines multiple entry rails — local fiat, cards, P2P, and crypto — with on-chain settlement in Bitcoin, USDT on Polygon, or other stablecoins on Liquid.

It is designed for users and businesses that need simpler access to self-custodial, cross-border payment flows, including in markets where traditional payment access is limited.

---

## Approach

P2Payments is designed around a few practical choices:
- **Self-custodial by default**
- **Agnostic in practice** — the usable rail and settlements for best conversion path matter more than ideology
- **Multi-rail** — different markets need different ways to pay
- **Modular** — rails and flows can be enabled or left out depending on the use case
- **Open source** — the public components remain MIT licensed

If a rail does not already settle into an asset supported by the Aqua wallet fork, P2Payments aims to convert further into the supported asset that is cheapest and most functional for that case.

---

## Rail Integrations

| Rail | Status | Currency | Payment Methods | Settlement | Fee | Verification |  
|------|--------|--------|--------|--------|--------|--------|
| BTC | Implemented | SATS | On-chain & Lightning | None | Bitcoin On-chain | None | None |
| USDT | Implemented | USD | Liquid & Polygon | USDT Liquid & Polygon | None | None |  
| Peach | ongoing | Global | Any | Bitcoin On-chain | High | None | 
| RoboSats | ongoing | Global | Any | Bitcoin On-chain  | High | None | 
| Mostro | planned | Global | Any | Bitcoin On-chain | High | None |
| Guardarian | planned | USD, EUR, GBP, CAD, AUD, JPY, TRY, PLN, SEK | Credit/Debit Cards & Google/Apple Pay | Bitcoin On-chain | Medium | Enhanced |
| Paygate | planned | Global | Credit/Debit Cards | USDT Polygon | Medium | None | 
| DePix | planned | BRL | Pix | BRL on Liquid | Law | None | 
| Kamipay | planned | BRL | Pix | USDT Polygon | Law | None | 
| MtPelerin | planned | EUR & CHF | SEPA | Bitcoin On-chain OR USDT Polygon | Low | Standard | 
| Bitzed | planned | ZMW | Mobile | Bitcoin On-chain | Low | None | 
| Matbea | planned | RUB | Yandex Pay, Sberbank, Tinkoff, YooMoney, SBP P2P, Mobile phone | Bitcoin On-chain | Low | None | 

---

## Active and Planned Repositories

### [mono](https://github.com/P2Payments/mono)
Single user orchestrator MIT repository. It assembles rails, flows, and supporting services in one workspace. Active development is currently centered here.

### [wallet](https://github.com/P2Payments/wallet)
A MIT fork of the Aqua Flutter Wallet for P2Payments, with an embedded Nuxt app to manage /mono settings and connect to BTCPay via the Shamrock protocol.

### dashboard
Nuxt-based MIT app, intended to handle payment flows through an embedded interface in the /wallet Flutter app.

### marketplace
Closed-source repository for multi-user marketplace integrations of the /mono repo.

---

## Intended Use Cases

P2Payments is aimed at cases where standard payment stacks are too limited, too fragile, or too dependent on a single provider.

Typical use cases include:

- cross-border businesses
- merchants that want crypto settlement with broader payment reach
- users in emerging markets
- high-risk but lawful businesses
- builders who want modular, self-hostable payment infrastructure
- Bitcoiners and crypto enthusiasts

It is not meant to be presented as a universal fit for every merchant.

---

## Status

P2Payments is still evolving. Some components exist as working integrations, others are partial, experimental, or still being assembled into the main orchestrator.

The repositories should be read as active infrastructure work, not as a finished product suite.

---

## Community

- [GitHub Discussions](https://github.com/orgs/P2Payments/discussions)
- [Telegram Group](https://t.me/P2PaymentsCom)

---

## Advisory

Commercial architecture advisory, integration design, and implementation support are available separately via [Blockchange](https://blockchange.expert).
