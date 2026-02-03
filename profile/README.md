Fiat payment processor with many local fiat payment methods with the merchant always receiving bitcoin.

## Features
- Self custodial solution with btcpay server integration.  
- Supports on-chain and Lighning Network payments.
- Supports USDt on TRON
- Supports fiat with the merchant always receiving bitcoins.  
- Invoicing for single user
- Ecommerce for single user
- Booking for single user

## Target
- Bitcoin enthusiasts: you believe in Bitcoin sound money but at the same time you know that Bitcoin is not widely used as you wish. This tool allows you to reach the traditional market without touching fiat money.  
- High risk businesses: you are involved in legal high risk business such as adult or legal cannabis and you can't find a traditional payment gateway supporting your business.  
- Unbanked and sanctioned: you are unbanked, or you live in a country that has not easy access to popular payment processors like Stripe, because your country is unsupported or even sanctioned.  
- Emerging markets: you want to expand your virtual service business to emerging markets like LATAM and Africa and you lack of a reliable payment gateway.

## Payment methods. Fees. Limits.
- Bitcoin: onchain and lightning network,
  - No fee.
  - No amount limit.  
- USDt: on Tron if you have the plugin on btcpay.
    - No fee.
    - No amount limit
- Fiat: All the currencies and local payment methods supported by [Peach Bitcoin](https://peachbitcoin.com) as listed [here](https://api.peachbitcoin.com/v1/info). Tens of local payment methods in Europe, LATAM, Africa with more to come, US excluded. Other p2p platforms integration will be evaluated.
-   - The fee is set by the merchant and paid by the buyer. To find a match it should be between 5 and 10%.
    - 1000 CHF (or equivalent in other currency) amount limit for each payment.
 
## Status
- Local payment methods integration with Peach Bitcoin. Btcpay server plugin under active development.  
- Local payment methods integration with Robosat almost ready but required a bond from the buyer, but it can be enebaled by my merchants only for recurring clients, where the marchant can put the bond on behalf of hte buyer knowing he/she will pay.  
- Local payment methods integration with Mostro. To be considered if feasible.  
- Credit and debit cards integration being evaluated with centralized kyc-free providers.  
- Of the 3 planned services (invoicing, ecommerce, booking) I'm still working on booking as the first one because it is probably the most time consuming to implement.  
      
## Main repos

### [p2pay-booking](https://github.com/p2payserver/p2pay-booking)
Under active development

![language](https://img.shields.io/github/languages/top/p2payto/p2pay-booking)
![Stars](https://img.shields.io/github/stars/p2payto/p2pay-booking?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2pay-booking?style=social)

### [p2pay-cloud](https://github.com/p2payserver/p2pay-cloud)
Development started and currently paused

![language](https://img.shields.io/github/languages/top/p2payto/p2pay-cloud)
![Stars](https://img.shields.io/github/stars/p2payto/p2pay-cloud?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2pay-cloud?style=social)

### [btcpay-plugin](https://github.com/p2payto/p2p-plugin)
Under active development

![language](https://img.shields.io/github/languages/top/p2payto/p2p-plugin)
![Stars](https://img.shields.io/github/stars/p2payto/p2p-plugin?style=social)
![Forks](https://img.shields.io/github/forks/p2payto/p2p-plugin?style=social)


## Commercial advisory

This is a non-profit open-source project under active development.

For teams looking for production-ready, commercial payment architecture solutions today,
Blockchange provides independent multi-rail payment advisory:
https://www.blockchange.com.py/en/#book



