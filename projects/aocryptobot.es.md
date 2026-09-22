# AOCryptobot

- **Dates:** 2020 → 2023
- **Status:** Archivado, open source
- **Stack:** Go, DDD, Binance API
- **Code:** [gitlab.com/aoterocom/AOCryptobot](https://gitlab.com/aoterocom/AOCryptobot)

![AOCryptobot](../img/cryptobot2.png)

Un bot de trading que nació en dos días durante el rally cripto de enero de 2021, como market maker que sacaba beneficio de las oscilaciones del precio, y que acabó siendo algo mucho más grande.

- Estrategias parametrizadas sobre indicadores conocidos como RSI, MACD y Stochastic RSI, usados como señales de entrada y salida.
- Un analizador de backtest que busca, para cada estrategia y mercado, los parámetros que mejor funcionaron en los últimos días.
- Varias estrategias y mercados a la vez, eligiendo la estrategia con la mejor relación entre beneficio y desviación estándar.
- Binance y paper trading.

Llegó a un beneficio medio semanal de alrededor del 2,5%.

![Backtest](../img/cryptobot4.png)
