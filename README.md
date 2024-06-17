# Pairs Trading Algorithm for Financial Markets

## Overview

This repository contains the implementation of a pairs trading algorithm for financial markets developed by Shashank Yadav. The strategy utilizes clustering techniques to identify pairs of stocks with correlated price movements, aiming to profit from temporary divergences in their prices.

## Strategy

The pairs trading strategy involves the following steps:

1. **Data Collection**: Historical stock price data is sourced from Yahoo Finance, covering a broad spectrum of the stock market, particularly the S&P 500 stocks. The data is preprocessed to handle missing values and standardized for uniformity and comparability across different stocks.

2. **Machine Learning Model for Pair Generation**: Clustering algorithms, specifically K-means and Hierarchical Clustering, are employed to group stocks with similar price movements. The optimal number of clusters is determined using the elbow method and silhouette scores. Stocks within the same cluster are considered potential trading pairs.

3. **Pairs Identification**: Correlation and cointegration tests are conducted to identify pairs of stocks suitable for trading strategies. A total of 12 pairs involving 16 unique tickers are identified based on statistical measures like correlation and cointegration.

4. **Z-Score Method for Trading Signals**: Buy and sell signals are generated based on the z-score of the price ratio between paired stocks. The z-score indicates extremes in the price ratio, guiding trading decisions.

5. **Plotting and Analysis**: The trading strategy is visualized by plotting price movements, buy/sell signals, and cumulative profit. Portfolio analysis is conducted to evaluate the performance of the strategy, including final returns and total return on investment.

## Results

The strategy successfully provided profitable returns in 9 out of 12 pairs, with a maximum return of 824.7% and a minimum return of 62.3%. However, it underperformed in 3 pairs, resulting in losses of 2.1%, 39.1%, and 33.1%.

## Recommendations

1. **Future Enhancements**: Incorporate additional financial metrics and market conditions, explore other clustering algorithms, and perform extended backtesting over different market cycles.
   
2. **Risk Management**: Implement position sizing techniques and stop-loss mechanisms to manage risk effectively and protect the portfolio from significant drawdowns.
   
3. **Market Adaptation**: Consider dynamic clustering techniques that adapt to changing market conditions to ensure the strategy remains relevant and effective.
