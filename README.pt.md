# P2Payments

Infraestrutura de pagamentos modular e open-source, construída em torno da liquidação em Bitcoin e stablecoins, projetada para permitir fluxos de integração e pagamento mais fluidos entre mercados e rails. Utiliza [BTCPay Server](https://github.com/btcpayserver/btcpayserver) como backend, um fork de [Aqua Wallet](https://github.com/AquaWallet/aqua-wallet) para liquidação self-custodial, e é desenvolvida principalmente com [Nuxt](https://github.com/nuxt/nuxt) e [Nitro](https://github.com/nitrojs/nitro).

A P2Payments combina múltiplos rails de entrada — fiat local, cartões, P2P e cripto — com liquidação on-chain em Bitcoin, USDT na Polygon ou outras stablecoins na Liquid.

Ela foi projetada para usuários e empresas que precisam de acesso mais simples a fluxos de pagamento self-custodial e cross-border, inclusive em mercados onde o acesso tradicional a pagamentos é limitado.

---

## Abordagem

A P2Payments foi projetada em torno de algumas escolhas práticas:
- **Self-custodial por padrão**
- **Agnóstica na prática** — o rail utilizável e as liquidações para o melhor caminho de conversão importam mais do que a ideologia
- **Multi-rail** — mercados diferentes precisam de formas diferentes de pagamento
- **Modular** — rails e fluxos podem ser habilitados ou deixados de fora dependendo do caso de uso
- **Open source** — os componentes públicos permanecem sob licença MIT

Se um rail ainda não liquidar em um ativo suportado pelo fork da Aqua Wallet, a P2Payments busca converter adicionalmente para o ativo suportado que seja mais barato e mais funcional para aquele caso.

---

## Integrações de rails

| Rail | Status | Moeda | Métodos de pagamento | Liquidação | Taxa | Verificação |
|------|--------|--------|----------------------|------------|------|--------------|
| BTC | Implementado | SATS | On-chain e Lightning | Nenhuma | Bitcoin On-chain | Nenhuma | Nenhuma |
| USDT | Implementado | USD | Liquid e Polygon | USDT Liquid e Polygon | Nenhuma | Nenhuma |
| Peach | em andamento | Global | Qualquer | Bitcoin On-chain | Alta | Nenhuma |
| RoboSats | em andamento | Global | Qualquer | Bitcoin On-chain | Alta | Nenhuma |
| Mostro | planejado | Global | Qualquer | Bitcoin On-chain | Alta | Nenhuma |
| Guardarian | planejado | USD, EUR, GBP, CAD, AUD, JPY, TRY, PLN, SEK | Cartões de crédito/débito e Google/Apple Pay | Bitcoin On-chain | Média | Reforçada |
| Paygate | planejado | Global | Cartões de crédito/débito | USDT Polygon | Média | Nenhuma |
| DePix | planejado | BRL | Pix | BRL na Liquid | Baixa | Nenhuma |
| Kamipay | planejado | BRL | Pix | USDT Polygon | Baixa | Nenhuma |
| MtPelerin | planejado | EUR e CHF | SEPA | Bitcoin On-chain OU USDT Polygon | Baixa | Padrão |
| Bitzed | planejado | ZMW | Móvel | Bitcoin On-chain | Baixa | Nenhuma |
| Matbea | planejado | RUB | Yandex Pay, Sberbank, Tinkoff, YooMoney, SBP P2P, telefone móvel | Bitcoin On-chain | Baixa | Nenhuma |

---

## Repositórios ativos e planejados

### [mono](https://github.com/P2Payments/mono)
Repositório MIT de orquestrador para usuário único. Ele reúne rails, fluxos e serviços de apoio em um único workspace. O desenvolvimento ativo está atualmente concentrado aqui.

### [wallet](https://github.com/P2Payments/wallet)
Um fork MIT da Aqua Flutter Wallet para P2Payments, com um app Nuxt embutido para gerenciar as configurações do /mono e conectar-se ao BTCPay via protocolo Shamrock.

### dashboard
App MIT baseada em Nuxt, destinada a lidar com fluxos de pagamento por meio de uma interface embutida no app Flutter /wallet.

### marketplace
Repositório de código fechado para integrações de marketplace multiusuário do repositório /mono.

---

## Casos de uso pretendidos

A P2Payments é voltada para casos em que stacks de pagamento padrão são limitados demais, frágeis demais ou dependentes demais de um único provedor.

Os casos de uso típicos incluem:

- negócios cross-border
- merchants que querem liquidação em cripto com maior alcance de pagamento
- usuários em mercados emergentes
- negócios de alto risco, mas legais
- builders que querem infraestrutura de pagamentos modular e self-hostable
- bitcoiners e entusiastas de cripto

Ela não deve ser apresentada como uma solução universal para qualquer merchant.

---

## Status

A P2Payments ainda está evoluindo. Alguns componentes existem como integrações funcionais, outros são parciais, experimentais ou ainda estão sendo montados dentro do orquestrador principal.

Os repositórios devem ser lidos como trabalho ativo de infraestrutura, não como uma suíte de produtos finalizada.

---

## Comunidade

- [GitHub Discussions](https://github.com/orgs/P2Payments/discussions)
- [Telegram](https://t.me/P2PaymentsCom)
