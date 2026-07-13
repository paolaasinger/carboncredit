# Carbon Credit Market Analysis
A quantitative research project analyzing the EU Emissions Trading System (EU ETS) carbon market, its relationship with energy commodities, and its behavior around major geopolitical and policy events — from the 2022 Russia-Ukraine energy crisis to the 2026 Middle East war.

## Overview
This project combines finance research methodology with data science technique to answer a core question: what actually drives EU carbon (EUA) prices, and how should risk be managed around them?
Using daily futures data from FactSet (EUA carbon, TTF natural gas, and Rotterdam coal, 2021–2026), the analysis moves from exploratory correlation through formal statistical modeling to practical risk metrics.

## Methods
Correlation analysis: static and 60-day rolling correlation between carbon, gas, and coal returns
Multiple regression (OLS): isolating which fuel, if any, statistically predicts carbon price movement
GARCH(1,1) volatility modeling: testing for volatility clustering and persistence in carbon returns
Hedge ratio estimation: quantifying gas exposure needed to offset carbon risk
Event study: abnormal return analysis (with t-tests) around major events, including EU policy milestones (Fit for 55, CBAM, ETS Reform) and geopolitical shocks (Russia-Ukraine war, Middle East war)
Structural break testing: comparing pre/post volatility and mean returns around major shocks
Value at Risk (VaR) and Monte Carlo simulation: quantifying downside risk for a hypothetical carbon position

## Key Findings
Carbon prices show weak, regime-dependent correlation with fuel prices, behaving more like an independent policy-driven asset than a fuel derivative
Gas is a statistically significant but economically small driver of carbon returns (R² = 1.9%)
Carbon volatility is highly persistent (GARCH β ≈ 0.90), meaning risk stays elevated well after a shock
Carbon markets reacted more strongly to the Russia-Ukraine war (direct EU gas supply threat) than to the 2026 Middle East conflict (indirect, primarily oil/shipping disruption)
Fat-tailed return behavior means standard VaR may understate true tail risk

## Data
Carbon: ICE ECX EUA Continuous Futures (EUR/tonne)
Natural Gas: Dutch TTF Calendar Month Continuous Futures (EUR/MWh)
Coal: Rotterdam Coal Quarterly Near Term (USD/tonne)
Source: FactSet, daily settlement prices, July 2021 – July 2026

## Tools
Python (pandas, matplotlib, statsmodels, arch, scipy, numpy) in Jupyter Notebook
