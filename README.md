# vol-protected-ts-momentum

# Volatility-Protected Time-Series Momentum Strategy

This project implements a time-series momentum trading strategy on SPY with a volatility-based filter to reduce risk exposure during turbulent market periods.

## Methodology

- **Asset**: SPY (S&P 500 ETF)
- **Signal**: 60-day momentum (positive return = buy, else cash)
- **Volatility Filter**: 20-day rolling standard deviation. Trade only when volatility is below the 80th percentile.
- **Execution**: Daily returns adjusted by previous day's signal to avoid lookahead bias.

## Performance Metric

- Strategy returns are plotted cumulatively.
- Sharpe Ratio is calculated (annualized).

## Files

- `momentum_vol_strategy.ipynb`: Main notebook with full strategy implementation and explanation.

## Next Steps

- Port strategy to QuantConnect's LEAN framework.
- Add realistic execution models and walk-forward validation.
