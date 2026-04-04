# P2PayTo

Open-source, modular payment infrastructure built around Bitcoin-based settlement.

P2PayTo combines multiple entry rails — fiat, cards, P2P, and crypto — with settlement toward assets supported by the Aqua wallet fork: BTC on-chain, L-BTC, and stablecoins on Liquid.

---

## Approach

P2PayTo is designed around a few practical choices:

- **Settlement-first** — the final asset matters more than the entry rail
- **Multi-rail** — different markets need different ways to pay
- **Agnostic in practice** — the usable rail and the best conversion path matter more than ideology
- **Self-custodial by default**
- **Modular** — rails and flows can be enabled or left out depending on the use case
- **Open source** — the public components remain MIT licensed

If a rail does not already settle into an asset supported by the Aqua wallet fork, P2PayTo aims to convert further into the supported asset that is cheapest and most functional for that case.

---

## Rail Integrations

| Rail | Status |
|------|--------|
| BTC on-chain | Implemented |
| Lightning | Implemented |
| USDT onnLiquid Network | Implemented |
| Peach | Implemented |
| RoboSats| Implemented |

---

## Active and Planned Repositories

### [mono](https://github.com/p2payto/mono)
Main orchestrator repository. It assembles rails, flows, and supporting services in one workspace. Active development is currently centered here.

### [wallet](https://github.com/p2payto/wallet)
Mobile wallet based on Aqua. Used for signing and self-custodial settlement flows within the broader P2PayTo architecture.

### [app](https://github.com/p2payto/app)
Nuxt-based wallet mini app. Intended to extend payment flows through an embedded interface.

### marketplace
Closed-source repository for multi-user marketplace integrations.

---

## Intended Use Cases

P2PayTo is aimed at cases where standard payment stacks are too limited, too fragile, or too dependent on a single provider.

Typical use cases include:

- cross-border businesses
- merchants that want crypto settlement with broader payment reach
- users in emerging markets
- high-risk but lawful businesses
- builders who want modular, self-hostable payment infrastructure

It is not meant to be presented as a universal fit for every merchant.

---

## Status

P2PayTo is still evolving. Some components exist as working integrations, others are partial, experimental, or still being assembled into the main orchestrator.

The repositories should be read as active infrastructure work, not as a finished product suite.

---

## Community

- [GitHub Discussions](https://github.com/orgs/p2payto/discussions)
- [Telegram](https://t.me/P2PayTo)

---

## Advisory

Commercial architecture advisory, integration design, and implementation support are available separately via [Blockchange](https://blockchange.expert).
