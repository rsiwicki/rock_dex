# rock_dex project

This project is a _data-in-context_ note book that conflates code and discussion exploring basic properties of Bitcoin and methods for trading strategies.

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

1. pandas
2. numpy
3. time
4. cufflinks - enhancements to plotly
5. plotly.offline - graphing libraries
