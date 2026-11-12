
# Emerging Market Premium Analysis | Python Portfolio Optimization

**Academic Research Project | Python | Financial Analytics | Portfolio Optimization**

## Project Overview

This project investigates whether selected emerging-market equity indices exhibit a higher risk premium than developed-market indices. Using Python, it compares the risk–return characteristics of minimum-variance portfolios (MVP) and maximum-Sharpe-ratio portfolios across two historical periods: 2019 and a COVID-19 market-disruption period (October 2019–June 2020).

The analysis is historical and exploratory; it is not an investment recommendation or evidence that an emerging-market premium exists in all periods.

## Research Questions

- How do expected returns, volatility and Sharpe ratios compare between the selected developed- and emerging-market portfolios?
- How do minimum-variance and maximum-Sharpe-ratio allocations differ?
- How do the results change when the analysis includes the early COVID-19 period?

## Data and Scope

| Market Group | Indices Used | Periods |
|---|---|---|
| Developed markets | EURO STOXX 50, Dow Jones Industrial Average, Nikkei 225 | 2019; October 2019–June 2020 |
| Emerging markets | MSCI BRIC large-, mid- and small-cap indices | 2019; October 2019–June 2020 |

**Scope note**: The emerging-market sample uses BRIC indices rather than a complete BRICS index; South Africa is not represented in those BRIC series. Historical data availability and index selection limit the generalizability of the findings.

## Methodology

1. Load historical index prices (Yahoo Finance through pandas_datareader for developed markets; local CSV datasets for emerging markets).
2. Calculate returns, covariance and volatility statistics.
3. Generate 2,500 randomly weighted portfolios for each market group and period.
4. Identify the sampled portfolio with the lowest volatility and the sampled portfolio with the highest Sharpe ratio.
5. Compare portfolio returns, volatility, Sharpe ratios and index weights; visualize the risk–return distributions.
The analysis uses historical risk-free-rate assumptions documented in the notebooks. The randomly sampled portfolios approximate the optimization objectives; they are not exact analytical optimizers. Results can vary between runs because the original notebooks do not set a random seed.

## Key Findings

- The selected developed-market portfolios experienced weaker expected returns and greater volatility in the COVID-period analysis.
- The emerging-market results were mixed rather than consistently showing a higher premium.
- In the COVID-period comparison, the emerging-market maximum-Sharpe portfolio showed higher estimated return and volatility, while the allocation patterns differed substantially between minimum-variance and maximum-Sharpe portfolios.
- Overall conclusion: The project did not consistently confirm an emerging-market premium across the selected indices and periods.
These are findings from the original historical analysis, not independently reproduced or updated estimates.

## Notebooks

| File | Analysis |
|---|---|
| [`Final_Developed.ipynb`](Final_Developed.ipynb) | Developed-market indices, 2019 |
| [`Final_Developed_Covid.ipynb`](Final_Developed_Covid.ipynb) | Developed-market indices, COVID-period comparison |
| [`Final_Emerging.ipynb`](Final_Emerging.ipynb) | Emerging-market indices, 2019 |
| [`Final_Emerging_Covid.ipynb`](Final_Emerging_Covid.ipynb) | Emerging-market indices, COVID-period comparison |

## Tools and Techniques

- **Programming:** Python, Jupyter Notebook
- **Libraries:** pandas, NumPy, SciPy, Matplotlib, pandas_datareader
- **Financial Analytics:** Financial time-series analysis, portfolio simulation, volatility analysis and Sharpe-ratio analysis
- **Analytical Methods:** Risk–return comparison, quantitative modeling and data visualization

## Reproducibility and Limitations

The original academic analysis has been updated for compatibility with Google Colab and more recent Python libraries.

### Data Dependencies

The emerging-market notebooks use two historical CSV datasets included in this repository:

- `BRICS_L_M_S.csv` — emerging-market analysis for 2019
- `BRICS_L_M_S_CORONA.csv` — COVID-period emerging-market analysis

The developed-market notebooks retrieve historical adjusted market prices from Yahoo Finance using the `yfinance` library.

### Testing and Compatibility

All four notebooks have been executed successfully in Google Colab following updates to data loading, date-index handling and Matplotlib chart exports.

### Limitations

- The analysis uses historical market data and assumptions documented in the notebooks.
- Historical prices retrieved from Yahoo Finance may differ from the original downloaded values.
- The portfolio simulations use random sampling without a fixed random seed, so results may vary between runs.
- The notebooks have not been independently validated against the original historical calculations.
- The project is academic research and should not be interpreted as investment advice.

### How to Explore the Project

1. Open the Jupyter notebooks directly on GitHub to review the code, visualizations and saved outputs.
2. To rerun the notebooks, open them in Google Colab or a compatible local Python environment.
3. For the emerging-market notebooks, keep the corresponding CSV datasets in the notebook's working directory.
4. For the developed-market notebooks, install `yfinance` and ensure internet access is available.
5. Review the historical assumptions before interpreting or comparing the results.

## Portfolio Relevance

This project demonstrates the application of Python to financial data analysis and quantitative research, including:

- Financial data processing and time-series analysis
- Quantitative modeling and portfolio simulation
- Risk–return analysis using volatility and Sharpe ratios
- Data visualization and interpretation of analytical results
- Communication of financial insights through reproducible research workflows

The project connects **financial analytics, quantitative modeling and Python-based data analysis**, supporting my broader interests in Business Intelligence, Data Analytics and Finance. 
