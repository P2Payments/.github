# P2Pagos

Infraestructura de pagos modular y de código abierto, construida en torno a la liquidación en Bitcoin y stablecoins, diseñada para permitir flujos de integración y pago más fluidos entre mercados y rieles. Utiliza [BTCPay Server](https://github.com/btcpayserver/btcpayserver) como backend, un fork de [Aqua Wallet](https://github.com/AquaWallet/aqua-wallet) para liquidación self-custodial, y está desarrollada principalmente con [Nuxt](https://github.com/nuxt/nuxt) y [Nitro](https://github.com/nitrojs/nitro).

P2Pagos combina múltiples rieles de entrada — fiat local, tarjetas, P2P y cripto — con liquidación on-chain en Bitcoin, USDT en Polygon u otras stablecoins en Liquid.

Está diseñada para usuarios y empresas que necesitan un acceso más simple a flujos de pago self-custodial y transfronterizos, incluso en mercados donde el acceso tradicional a pagos es limitado.

---

## Enfoque

P2Pagos está diseñada en torno a algunas decisiones prácticas:
- **Self-custodial por defecto**
- **Ag­nóstica en la práctica** — el riel utilizable y las liquidaciones para la mejor ruta de conversión importan más que la ideología
- **Multi-rail** — distintos mercados necesitan distintas formas de pagar
- **Modular** — los rieles y flujos pueden habilitarse o dejarse fuera según el caso de uso
- **Código abierto** — los componentes públicos permanecen bajo licencia MIT, con el mantenimiento y desarrollo a largo plazo respaldados por los ingresos de la oferta cerrada de pago

Si un riel no liquida ya en un activo soportado por el fork de Aqua Wallet, P2Pagos busca convertirlo adicionalmente al activo soportado que sea más barato y más funcional para ese caso.

---

## Integraciones de rieles

| Rail | Estado | Moneda | Métodos de pago | Liquidación | Comisión | Verificación |
|------|--------|--------|-----------------|-------------|----------|--------------|
| BTC | Implementado | SATS | On-chain y Lightning | Ninguna | Bitcoin On-chain | Ninguna | Ninguna |
| USDT | Implementado | USD | Liquid y Polygon | USDT Liquid y Polygon | Ninguna | Ninguna |
| Peach | en curso | Global | Cualquiera | Bitcoin On-chain | Alta | Ninguna |
| RoboSats | en curso | Global | Cualquiera | Bitcoin On-chain | Alta | Ninguna |
| Mostro | planificado | Global | Cualquiera | Bitcoin On-chain | Alta | Ninguna |
| Guardarian | planificado | USD, EUR, GBP, CAD, AUD, JPY, TRY, PLN, SEK | Tarjetas de crédito/débito y Google/Apple Pay | Bitcoin On-chain | Media | Reforzada |
| Paygate | planificado | Global | Tarjetas de crédito/débito | USDT Polygon | Media | Ninguna |
| DePix | planificado | BRL | Pix | BRL en Liquid | Baja | Ninguna |
| Kamipay | planificado | BRL | Pix | USDT Polygon | Baja | Ninguna |
| MtPelerin | planificado | EUR y CHF | SEPA | Bitcoin On-chain O USDT Polygon | Baja | Estándar |
| Bitzed | planificado | ZMW | Móvil | Bitcoin On-chain | Baja | Ninguna |
| Matbea | planificado | RUB | Yandex Pay, Sberbank, Tinkoff, YooMoney, SBP P2P, teléfono móvil | Bitcoin On-chain | Baja | Ninguna |

---

## Repositorios activos y planificados

### [mono](https://github.com/P2Pagos/mono)
Repositorio MIT de orquestador para un solo usuario. Reúne rieles, flujos y servicios de apoyo en un único workspace. El desarrollo activo está centrado actualmente aquí.

### [wallet](https://github.com/P2Pagos/wallet)
Un fork MIT de Aqua Flutter Wallet para P2Pagos, con una app Nuxt embebida para gestionar la configuración de /mono y conectarse a BTCPay mediante el protocolo Shamrock.

### dashboard
App MIT basada en Nuxt, pensada para gestionar flujos de pago mediante una interfaz embebida en la app Flutter /wallet.

### marketplace
Repositorio de código cerrado para integraciones de marketplace multiusuario del repositorio /mono.

---

## Casos de uso previstos

P2Pagos está orientada a casos en los que los stacks de pago estándar son demasiado limitados, demasiado frágiles o demasiado dependientes de un único proveedor.

Los casos de uso típicos incluyen:

- negocios transfronterizos
- comercios que quieren liquidación en cripto con mayor alcance de pago
- usuarios en mercados emergentes
- negocios de alto riesgo pero legales
- builders que quieren infraestructura de pagos modular y self-hostable
- bitcoiners y entusiastas de las criptomonedas

No está pensada para presentarse como una solución universal para cualquier comercio.

---

## Estado

P2Pagos sigue evolucionando. Algunos componentes existen como integraciones funcionales, otros son parciales, experimentales o todavía se están ensamblando dentro del orquestador principal.

Los repositorios deben leerse como trabajo activo de infraestructura, no como una suite de productos terminada.

---

## Comunidad y contacto

- [Debates en GitHub](https://github.com/orgs/P2Pagos/discussions)
- [Grupo de Telegram](https://t.me/P2Pagos)
- [p2pagos@p2pay.to](mailto:p2pagos@p2pay.to) con PGP opcional [A1786A2CF6C5B65FDB4519F17E425F745D4EE866](https://pgp.p2pay.to)
 
---

### Proyecto inspirado en [**BitPagos**](https://web.archive.org/web/20141225131358/https://www.bitpagos.com/es/)


