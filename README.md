This project implements an algorithmic statistical arbitrage strategy in Python to identify and trade 
cointegrated stock pairs. Traditional pairs trading models rely on static ordinary least squares (OLS) 
regression to calculate a constant hedge ratio, which fails when market regimes shift over time. 
To address this parameter drift, this framework uses a Kalman Filter to continuously estimate 
hedge ratios (β) in real time without lookahead bias, adapting to changing correlations between assets.

After screening tech equities using the Engle-Granger cointegration test, residual spread errors 
are normalized into rolling Z-scores to generate mean-reversion trading signals. Through parameter 
optimization across lookback windows and entry/exit thresholds, the model significantly enhanced its 
risk adjusted performance, raising the backtested Sharpe ratio from 0.57 to 0.91 while reducing maximum 
drawdown to -9.6%.
