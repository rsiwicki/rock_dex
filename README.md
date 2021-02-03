# rock_dex project

This project is a _data-in-context_ note book that conflates code and discussion exploring basic properties of Bitcoin and methods for trading strategies.

It is referred to in this blog post: https://robert-siwicki.medium.com/bitcoin-as-a-store-of-value-and-experiments-with-algorithmic-trading-strategies-dd9794b1b0db

# Introduction

## Overview

Bitcoin (BTC) is proposed to provided a modern era store of value and be a potential successor to Gold (GLD) in this respect (Ammous, 2018). Ammous (2018) illustrates that one of the key determinate factors of both BTC and GLD in confering this property is that they both demonstrate a high stock-to-flow ratio.

Stock-to-flow refers to the property by which the current global stock or holding of an asset compares to the potential incomming flow of that asset. For example, the global stock of GLD compared to the potential new production of GLD is very high - i.e. its a rare metal on Earth and the effort of extraction of new GLD only accounts for some 2% of the stock. This is compared to the potential stock-to-flow of fiat currency whereby government issued paper (no longer backed by anything like a gold standard) can be printed / minted readily (with little effort) thus large quantities of new flow can devalue currently held stock, leading to inflationary periods and the consequent socio-economic results. The economic model of BTC is purported to resemble that of GLD as BTC miners are effectively expending a larger amount of resource and effort in minting new Bitcions. In addition the total global supply of BTC is capped to 22 million; this should result in a deflationary currency.

This study will make heavy use of the methods of Hilpisch (2020), who writes as a specialist in the domain of data-driven finance. So as such it is both a learning excercise of personal interest in the crypto currency markets though also a vehicle by which the author can learn and test the methods of Hilpisch.

## Problem Statements

In this study this notebook will:

1. Investigate the potential correlation between BTC and GLD returns in timeseries, assuming a positive correlation indicates some representation whereby BTC is also considered a store of value. The assumption here is that when investors opt for gold as a store of value they could also opt for BTC.
2. Machine learning will be applied to determine if the trades into BTC or GLD can be recommended over just holding a long position (it is suspected that the recent activities driving the price of BTC higher could result in an extremely simple, hold only strategy)


## Metrics

The metrics for this project are relatively simple, given the strong connection to the financial domain and are either the price of the assets (GLD, BTC), the returns or relevant statistical metrics such as correlation.

## Data

Data for crypto currency prices where obtained for free from https://www.cryptodatadownload.com and data is from the crypto currency exchange Binance.

Data for gold prices was obtained from Yahoo Finance https://uk.finance.yahoo.com.

## Libraries Used

pandas
numpy
time
cufflinks - enhancements to plotly
plotly.offline - graphing libraries

## Findings

There appears to be a possible increase of correlation of gold and BTC prices over time series. Whilst still weak the trend should be observed over time in a further study to see if it increases as expected.

In the case of testing algorithms where confronted with previously unseen data, no algorithmic machine learning strategy works better than a simple hold strategy.

## Conclusion

Part 1 of this study, investigating how BTC could potentially relate to GLD as a store of value demonstrates that there is a possibility that there is an increasing correlation over time between BTC price and GLD price movements. To further improve this study, time is required to further assess the relationship in our existing simplified model; though, the addition and study of additional financial metrics that impact the GLD price, though applied to BTC could be considered - e.g. inflation metrics.

Part 2 of this study deeply assessed the methods Hilpisch (2020) demonstrates in order to start identifying a potential machine learning based strategy for increasing hypothetical future returns of trading BTC, through only technical analysis and not fundamental analysis. The simple hold strategy was pitted against a second reference strategy of Fast and Slow Simple Moving Averages (SMA). Further to this Support Vector Machine and Logistic Regression strategies were added with simplified engineered features of return lags and whether a position should be short or long. The machine learning strategies all appeared to be weak once tested with a train / test split of the data and compared to a simple hold strategy.

Though our findings that simply holding BTC generates effective returns and in reality with costs accrued per trade is certainly more efficient is perhaps itself a very fitting answer as to how best to trade BTC in the current environment, essentially buy and hold.

It is likely that the unusual nature of BTCs recent ascent could be confounding the training and testing of our algorithms: i.e. that the real driver for BTC prices is something more fundamental than technical analysis; such as the store-of-value effect studied in part 1.
Future improvement could include attempting the same strategies on hourly data instead of daily, perhaps here there are technical analysis relationships that are more subtle and intra day trading could benefit from a machine learning approach.

## References

Ammous, S (2018). The Bitcoin Standard: The Decentralized Alternative to Central Banking. Wiley.

Binance (2021). Crypto Currency Data: Bitcoin USD. From https://www.cryptodatadownload.com.

Hilpisch, Y (2020). Python for Finance: Mastering Data Driven Finance. O'Reilly.

Yahoo (2021). Gold Prices Daily. From https://uk.finance.yahoo.com.

