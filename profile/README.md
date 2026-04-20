[Español](https://github.com/P2Pagos/.github/blob/main/profile/README.es.md) | [Português](https://github.com/P2Pagos/.github/blob/main/profile/README.pt.md) | [Русский](https://github.com/P2Pagos/.github/blob/main/profile/README.ru.md) | [Français](https://github.com/P2Pagos/.github/blob/main/profile/README.fr.md) | [Italiano](https://github.com/P2Pagos/.github/blob/main/profile/README.it.md)

> Translations may be outdated.  
> Las traducciones pueden estar desactualizadas.

# P2Pagos — Open-Source Multi-Rail Payment Infrastructure

Open-source, modular, and agnostic-by-design payment infrastructure for businesses and users that need practical multi-rail payment flows, self-custodial settlement, and more flexible cross-border money movement.

P2Pagos is built around **inbound rails**, **multi-rail offramp** and self-custodial settlement. It is designed to make payment architecture more practical across markets, rails, currencies, and jurisdictions, especially where traditional payment access is fragmented, limited, or overly dependent on a single provider.

P2Pagos uses [BTCPay Server](https://github.com/btcpayserver/btcpayserver) as the backend and an [Aqua Wallet](https://github.com/AquaWallet/aqua-wallet) fork as the default settlement wallet.

[BTCPay Server](https://github.com/btcpayserver/btcpayserver) was chosen because it is a battle-tested, widely adopted, and community-maintained API and GUI backend with some built-in rails. We also actively contribute to its [core and plugin ecosystem](https://github.com/search?q=involves%3Alearntheropes+%28org%3Abtcpayserver+OR+org%3Abtcpayserver-tether+OR+org%3Amempool%29&type=issues).

[Aqua Wallet](https://github.com/AquaWallet/aqua-wallet) was chosen because it already supports settlement in **btc on-chain, multiple stablecoins (USD and BRL for now)** by default, and can be integrated from BTCPay Server through the Shamrock protocol with a QR-based connection flow.

Where direct local cashout is not yet native, P2Pagos provides practical guidance around compatible external wallets, cards, and off-ramp tools to improve real usability in Latin America and other supported regions. For instance, across all currently planned settlement chains, we already consider wallets and services such as [Belo](https://belo.app), [Revolut](https://www.revolut.com), and [Offramp](https://offramp.xyz), including card and Google Pay / Apple Pay compatible paths, while more privacy-friendly card and Google Pay options may later be added through planned FixedFloat API work or collaboration with the issuer.

---

## Multi-Rail Payment Architecture Approach

P2Pagos is designed around a few practical choices:

- **Self-custodial by default**
- **Agnostic in practice** — the usable rail and settlement path matter more than ideology
- **Multi-rail by design** — different markets need different ways to pay and cash out
- **Modular** — inbound rails, offramps, flows, and services can be enabled or left out depending on the use case
- **Open source** — the public components remain MIT licensed, with long-term maintenance and development supported by revenue from the paid closed-source offering

If an inbound rail does not already settle into an asset supported by the Aqua wallet fork, P2Pagos aims to convert further into the supported asset that is cheapest and most functional for that case.

---

## Architecture

```mermaid
flowchart LR

subgraph walletWrap["/wallet (MIT)"]
  walletPlatform["Aqua fork (MIT) / (iOS & Android)"]
  seedMono["seed phrase"]
  seedMarket["seed phrase"]
  seedTeam["seed phrase / xpub"]
end

mono["/mono (MIT)"]
monoBtcpay["BTCPay Server (MIT)"]

subgraph docker["Docker"]
  marketplace["/marketplace (closed-source)"]
  marketBtcpay["BTCPay Server (MIT)"]
end

team["/team"]
otherWallet["/wallet (MIT)"]
builtMarket["built on"]
builtTeam["built on"]

dashboard["/dashboard"]

seedMono --> mono
seedMarket --> marketplace
seedTeam -.-> team
otherWallet --> marketplace

mono --> monoBtcpay
marketplace --> marketBtcpay
dashboard --> marketplace

marketplace -.-> builtMarket
builtMarket -.-> mono

team -.-> builtTeam
builtTeam -.-> mono

style team stroke-dasharray: 6 6
style builtMarket fill:transparent,stroke:transparent,color:#999
style builtTeam fill:transparent,stroke:transparent,color:#999
style walletPlatform fill:transparent,stroke:transparent,color:#999

click otherWallet "https://github.com/P2Pagos/wallet" "_blank"
click mono "https://github.com/P2Pagos/mono" "_blank"
```

---

## Inbound Multi-Rails

| Rail | Status | Currency | Payment Methods | Settlement | Fee | Verification |
|------|--------|----------|-----------------|------------|-----|--------------|
| BTC | Implemented | SATS | On-chain & Lightning | Bitcoin On-chain | None | None |
| USDT | Implemented | USD | Liquid & Polygon | USDT Liquid & Polygon | None | None |
| [Peach](https://github.com/P2Pagos/mono/tree/main/rails/peach) *(p2p-api-integration)* | testing | Global | Any | Bitcoin On-chain | High | None |
| [RoboSats](https://github.com/P2Pagos/mono/tree/main/rails/robosats) *(p2p-api-integration)* | testing | Global | Any | Bitcoin On-chain | High | None |
| Mostro *(p2p-api-integration)* | evaluating | Global | Any | Bitcoin On-chain | High | None |
| Guardarian *(cex-api-integration)* | planned | USD, EUR, GBP, CAD, AUD, JPY, TRY, PLN, SEK | Credit/Debit Cards & Google/Apple Pay | Bitcoin On-chain | Medium | Enhanced |
| Paygate *(cex-api-integration)* | planned | Global | Credit/Debit Cards | USDT Polygon | Medium | None |
| DePix *(cex-api-integration)* | planned | BRL | Pix | BRL on Liquid | Low | None |
| Kamipay *(cex-api-integration)* | planned | BRL | Pix | USDT Polygon | Low | None |
| MtPelerin *(cex-api-integration)* | planned | EUR & CHF | SEPA | Bitcoin On-chain OR USDT Polygon | Low | Standard |
| Bitzed *(cex-api-integration)* | planned | ZMW | Mobile | Bitcoin On-chain | Low | None |
| Matbea *(cex+p2p-api-integration)* | planned | RUB | Yandex Pay, Sberbank, Tinkoff, YooMoney, SBP P2P, Mobile phone | Bitcoin On-chain | Low | None |

---

## Multi-Rail Offramp

| Cashout | Status | Currency | Payment Methods | Verification |
|---------|--------|----------|-----------------|--------------|
| dLocal | early stage | LATAM / Africa / Asia & Middle East | bank transfer | standard |
| Ueno Bank | post [moonshot.md](moonshot.md) | PYG / USD | bank transfer / card-popup | standard |
| Freedomia Card | planned | USD limited settlements | card / Google Pay | none |

Referral code for one month free: [Freedomia](https://www.freedomia.io/a/p2pagos)

---

## Service Modules

| Service | Status | Scope | Purpose | Default |
|---------|--------|-------|---------|---------|
| [ip-detection](https://github.com/P2Pagos/mono/tree/main/services/ip-detection) | testing | global | IP geolocation and currency detection | enabled by default for currency detection based on Cloudflare country location; detailed notes will be covered in a separate blog post about a Proton VPN vulnerability ignored by the security team; ipinfo requires a free lifetime API key |
| [tor](https://github.com/P2Pagos/mono/tree/main/services/tor) | testing | global | Tor reverse proxy for onion and Tor-based integrations | enabled if consumed by an enabled rail |
| [cors](https://github.com/P2Pagos/mono/tree/main/services/cors) | testing | global | CORS reverse proxy for target APIs | enabled if consumed by an enabled rail |
| [market](https://github.com/P2Pagos/mono/tree/main/services/market) | testing | global | market aggregation and external offers | enabled if consumed by an enabled rail |
| kyc-kyb | defined | worldwide | KYC / KYB | optional, disabled by default |
| invoicing-reporting-py | in planning | Paraguay | invoicing and reporting | optional, disabled by default |

---

## Active and Planned Repositories

### [mono](https://github.com/P2Pagos/mono)

Single user orchestrator MIT repository.

It assembles inbound rails, settlement flows, and supporting services into one workspace. Active development is currently centered here.

### [wallet](https://github.com/P2Pagos/wallet)

A MIT fork of the Aqua Flutter Wallet for P2Pagos, with an embedded Nuxt app to manage /mono settings and connect to BTCPay via the Shamrock protocol.

### dashboard

Nuxt-based MIT app, intended to handle payment flows through an embedded interface in the /wallet Flutter app.

### marketplace

Closed-source repository for multi-user marketplace integrations of the /mono repo.

---

## Use Cases for Multi-Rail Payments

P2Pagos is aimed at cases where standard payment stacks are too limited, too fragile, or too dependent on a single provider.

Typical use cases include:

- cross-border businesses
- businesses that need multi-rail inbound payments
- merchants that want crypto settlement with broader payment reach
- users in emerging markets
- high-risk but lawful businesses
- builders that want modular, self-hostable payment infrastructure
- Bitcoiners and crypto enthusiasts

It is not meant to be presented as a universal fit for every merchant.

---

## Current Status

P2Pagos is still evolving.

Some components exist as working integrations, others are partial, experimental, or still being assembled into the main orchestrator. The repositories should be read as active infrastructure work, not as a finished product suite.

---

## Community & Contact

- [GitHub Discussions](https://github.com/orgs/P2Pagos/discussions)
- [Telegram Group](https://t.me/P2Pagos)
- [p2pagos@p2pay.to](mailto:p2pagos@p2pay.to) with optional PGP [A1786A2CF6C5B65FDB4519F17E425F745D4EE866](https://pgp.p2pay.to)

---

### Project inspired by [**BitPagos**](https://web.archive.org/web/20141225131358/https://www.bitpagos.com/es/) in 2014.
