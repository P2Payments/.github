Fiat payment processor with many local fiat payment methods with the merchant always receiving bitcoin.

## Status
I'm working on the Peach API integration, but I'm stack waiting that a new endpoint is added to publish a buy offer for a fixed amount.  
Fiat integration with Robosat. To be considered if feasible  
Fiat integration with Mostro. To be considered if feasible  
Fiat integration with hodl Hodl. Can't be implemented since it requires the account creation manually the last time that I checked  
Of the 3 planned services (invoicing, ecommerce, booking) I'm still working on booking as the first one because it is probably the most time consuming to implement.  

## Features
- Self custodial solution with btcpay server integration.  
- Supports on-chain and Lighning Network payments.
- Supports USDt on TRON
- Supports fiat with the merchant always receiving bitcoins.  
- Invoicing: single user stand-alone service
- Ecommerce: single user stand-alone service
- Booking: single user stand-alone service
- Cloud: multiple users cloud app with all the previous services included.

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



