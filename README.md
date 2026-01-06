# Dual Momentum Strategy

A systematic equity momentum strategy combining absolute (time-series) and relative (cross-sectional) momentum signals for enhanced risk-adjusted returns with downside protection.

## Project Overview:

Type: Quantitative Trading Strategy

Time Period: 2018-2025 (8 years)

Implementation: Python, Google Colab

## Key Results:

CAGR: 15.65% vs 13.70% (S&P 500)

Sharpe Ratio: 0.81 vs 0.74 (+9.5% improvement)

Alpha: +1.95% annually

Max Drawdown: -32.51% vs -33.72% (better protection)

## Strategy Description:

### Core Methodology:

#### Dual Momentum Approach:


Absolute Momentum (12-month): Filters stocks with positive trailing 12-month returns (trend identification)

Relative Momentum (6-month): Ranks eligible stocks by 6-month performance

Portfolio Construction: Hold top 20 stocks, equal-weighted (5% each)

Risk Management: Move to cash (SHY) when <30% of universe shows positive absolute momentum

Rebalancing: Monthly

Transaction Costs: 0.2% of turnover (realistic institutional rate)

## Academic Foundation:


Jegadeesh & Titman (1993) - Cross-sectional momentum

Moskowitz et al. (2012) - Time-series momentum

Antonacci (2014) - Dual momentum framework


## Technical Implementation:


### Universe:


120 large-cap stocks across 10 sectors

Diversified across Technology, Finance, Healthcare, Consumer, Energy, etc.

Benchmark: S&P 500 (SPY)

Cash Proxy: 1-3 Year Treasuries (SHY)


## Code Structure:

├── 0. Library Imports

├── 1. Configuration & Parameters

├── 2. Data Collection (yfinance)

├── 3. Momentum Signal Calculation

├── 4. Portfolio Construction & Backtesting

├── 5. Performance Metrics Analysis

└── 6. Visualization & Results


## Key Features:


Walk-forward backtesting (no look-ahead bias)

Turnover-based transaction costs (73% average monthly turnover)

Regime detection (Risk-ON: 87% | Risk-OFF: 13%)

Proper type handling and error prevention

Comprehensive performance metrics


## Performance Analysis:


| Metric          | Strategy | S&P 500 | Difference |
|-----------------|----------|---------|------------|
| Total Return    | 215.97%  | 176.13% | +39.84%    |
| CAGR            | 15.65%   | 13.70%  | +1.95%     |
| Volatility      | 19.81%   | 19.22%  | +0.59%     |
| Sharpe Ratio    | 0.81     | 0.74    | +0.07      |
| Max Drawdown    | -32.51%  | -33.72% | +1.21%     |
| Calmar Ratio    | 0.48     | 0.41    | +0.08      |



## Transaction Costs:

Total Costs: $18,728 over 8 years

Average per Rebalance: $280

Cost as % of Returns: 8.67% (realistic for active strategy)

Average Turnover: 73.3% monthly (consistent with academic literature)


## Prerequisites:

pythonpip install yfinance pandas numpy matplotlib seaborn

#### Running the Notebook:

Open Dual_Momentum_Strategy.ipynb in Google Colab or Jupyter

Run all cells sequentially

Runtime: 2-3 minutes for full execution


## Data:

Source: Yahoo Finance (yfinance)

Period: 2018-01-01 to 2025-12-31

Frequency: Daily prices, monthly rebalancing


## Visualizations:

The notebook generates 4 key charts:

Equity Curve: Strategy vs benchmark cumulative performance

Drawdown Comparison: Peak-to-trough analysis

Rolling Sharpe Ratio: Time-varying risk-adjusted performance

Monthly Returns Heatmap: Calendar view of returns


## Limitations:

Survivorship Bias: Universe based on 2025 constituents, likely overstating returns 

Single Asset Class: Equities only (no bonds, commodities, currencies)

Simplified Transaction Costs: Fixed 0.2% rate, doesn't account for market impact

Parameter Stability: Fixed lookback periods (not adaptive)

## Academic Context:

This project implements dual momentum as a practical application of academic research:

Demonstrates understanding of momentum anomaly

Shows ability to translate research into implementable strategies

Includes realistic execution costs and risk management

Theory-driven parameters (not curve-fitted)

Positioning: This is a secondary project demonstrating breadth of quantitative skills. For more complex work involving Markov-switching models and multi-asset optimization, see Portfolio Optimization Project.

## Files:

Dual_Momentum_Strategy.ipynb - Main notebook with full implementation

README.md - This file

## Author: Aymen Hafsaoui

linkedin.com/in/aymen-hafsaoui-2ba52431a | aymn.hafsaoui@gmail.com
 
## License:

This project is open source and available for educational purposes.

## Acknowledgments:

Academic research: Jegadeesh, Titman, Moskowitz, Antonacci

Data source: Yahoo Finance via yfinance

Implementation environment: Google Colab


Note: This strategy is for educational and research purposes only. Past performance does not guarantee future results. Not financial advice.PartagerArtéfactsTout téléchargerDual momentum with transaction costsPY 
