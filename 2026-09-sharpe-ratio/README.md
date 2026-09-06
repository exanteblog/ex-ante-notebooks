# Two Portfolios, One Score

The Sharpe ratio is built from the mean and standard deviation of returns.
Neither depends on the order the returns arrive in.

Data: S&P 500 daily returns, 2007 to 2009, 754 trading days, via yfinance.
Cached locally as sp500_2007_2009.csv.

Method: shuffle the daily returns 10,000 times and recompute the Sharpe ratio
and the maximum drawdown for each ordering.

Result: the Sharpe ratio is identical across all 10,000 shuffles, to within
floating point error. The maximum drawdown ranges from -26.5% to -72.2%. The
actual 2008 drawdown of -56.8% was worse than 86.8% of random orderings, which
is volatility clustering showing up in the data.

Run sharpe_ratio_order.ipynb top to bottom on a fresh kernel.