---
layout: post
title: "Security Price Volatility Indexer"
date: 2014-08-06 10:47:49 -0500
---
A program that reads in market data of prices of securities, stores them and does a simple calculation of the change in price over an amount of time given a fixed starting date. You can set intervals of time such as a day, week, month, etc when calculations will be made. The output will be a list of securities ordered by those with the highest change in price over the given time period.

The thought is an assisted way to get a list of securities whose rate of change in price is greater than average and can be provided to an individual who can decide whether to invest or not. A more advanced take on it is having the program figure out price trends that are more "smoothly" changing than others—versus those that are more "spiky", with the intention that a smoother curve implies a trend which a human could then reason about after researching the security. With the goal of trying to separate erratic securities from more reliable ones.
