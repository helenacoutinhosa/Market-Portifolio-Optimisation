# Brazilian Market Portfolio Optimization

This project analyzes a selection of major Brazilian publicly traded companies and constructs an efficient frontier to evaluate optimal portfolio allocations based on risk and return. The objective is to demonstrate how portfolio theory can be applied to an emerging market using real financial data.

### Key Features
- Retrieves historical price data from Yahoo Finance
- Calculates daily and annualized returns
- Computes covariance and correlation structure of assets
- Runs Monte Carlo portfolio simulations to generate thousands of possible portfolio combinations
- Identifies:
  - Maximum Sharpe Ratio Portfolio (highest risk-adjusted return)
  - Minimum Volatility Portfolio (lowest overall risk)
- Plots the Efficient Frontier using `ggplot2`

---

### 📊 Assets Included
| Ticker      | Company Name                      | Sector                  |
|------------|-----------------------------------|-------------------------|
| ITUB4.SA   | Itaú Unibanco                     | Banking & Finance       |
| VALE3.SA   | Vale S.A.                          | Mining & Commodities    |
| PETR4.SA   | Petrobras                           | Energy & Oil            |
| BBDC4.SA   | Bradesco S.A.                      | Banking & Finance       |
| WEGE3.SA   | WEG S.A.                            | Industrial Technology   |

---

### Files in This Repository
| File | Description |
|------|-------------|
| `brazil_portfolio_optimization.Rmd` | R Notebook script for data loading, portfolio simulation, and efficient frontier visualization |
| `monte_carlo_portfolios.csv` (created when running) | Contains all generated simulated portfolios |
| `efficient_frontier.png` (created when running) | Saved visualization of the efficient frontier |

---

### Methodology
This project uses:
- **Daily log returns** for return consistency
- **Annualization factor of 252 trading days**
- **Random weight generation** with normalization for portfolio simulations
- **Sharpe Ratio** as performance metric:

\[
\text{Sharpe Ratio} = \frac{\text{Expected Return}}{\text{Portfolio Volatility}}
\]

---

### Requirements
Install the following R packages before running:

```r
install.packages(c("quantmod", "tidyverse", "PerformanceAnalytics", "xts", "ggplot2"))
