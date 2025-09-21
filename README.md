# banks-var
# Model Note — 1‑Day VaR Backtest (Banks)

**Purpose.** Evaluate 1‑day Value‑at‑Risk (VaR) coverage for bank stocks using **parametric** and **historical** VaR at 95% and 99% confidence.

**Data.** Daily close → returns; rolling window = 250 trading days (≈ 1Y).

**Backtests.**
- Exceptions counted where realized return < VaR.
- **Kupiec (UC) test** p-values reported for each ticker/level.

**Assumptions & Limits.**
- Normality for parametric VaR; historical VaR sensitive to window choice.
- Non‑stationarity; no liquidity/transaction cost modeling.
- No ES backtest; VaR horizon fixed at 1 day.

**Monitoring Ideas.**
- Rolling exception rate vs target (5%/1%).
- Regime flags using rolling volatility or GARCH.

The var_results.csv contains the result and the plots folder contains the plot for each bank with 95 and 99% confidence
