![Crypto logo](/img/cryptobot2.png)

### This is ![](/img/gologo.png)

* * *

##### Two days, one bot. Cryptobot started being a development that crossed my mind eventually and was done in a couple of days, I mean, literally...

*   Made with **Golang**
*   Binance and/or paper trading support
*   Custom Market Maker strategy config parameters
*   Backtest analyzer algorithm and parameter calculator

![Crypto logo](/img/cryptobot3.png)

### Why this project

* * *

This project that was initially designed to get profit of the Jan 2021 ‘crypto-boom’, with cryptocurrencies rising up, to be able to take profit not only of the rise (holding asset) but with a market-maker play (takes profit of the market oscillations, buying and selling constantly waiting for that waving behaviour)

Now this became in something pretty big, with the introduction of **custom parametrized strategies** in lastest PR’s. This means that you can create a strategy based in the best **well-known market and trading indicators**, as RSI, MACD, Stochastic RSI… Using a maximum of 2 parameters, that use to be associated indicator curve steep

The bot is, in addition, capable of run with **simultaneous strategies and markets, calculating the best parameters for each strategy**, and been able to select one of them, if conditions are addressed (for example, in my tests I’m declaring tradeable any strategy with backtest profit of 1.5% on the last 5 days, I play always with the strategy that have better benefit / std deviation ratio)

![Crypto logo](/img/cryptobot4.png)

### Checkout from Gitlab

* * *

The project **is under GNU-GPL license** so you can check out the full code on github at the following repo:

##### [https://gitlab.com/aoterocom/AOCryptobot](https://gitlab.com/aoterocom/AOCryptobot)
