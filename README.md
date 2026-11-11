Emerging Market Premium Analysis | Python Portfolio Optimization
Academic research project · Python · Financial Analytics · Portfolio Optimization
Project overview
This project investigates whether selected emerging-market equity indices exhibit a higher risk premium than developed-market indices. Using Python, it compares the risk–return characteristics of minimum-variance portfolios (MVP) and maximum-Sharpe-ratio portfolios across two historical periods: 2019 and a COVID-19 market-disruption period (October 2019–June 2020).

The analysis is historical and exploratory; it is not an investment recommendation or evidence that an emerging-market premium exists in all periods.
Research questions
- How do expected returns, volatility and Sharpe ratios compare between the selected developed- and emerging-market portfolios?
- How do minimum-variance and maximum-Sharpe-ratio allocations differ?
- How do the results change when the analysis includes the early COVID-19 period?
Data and scope
Market group	Indices used	Periods
Developed markets	EURO STOXX 50, Dow Jones Industrial Average, Nikkei 225	2019; October 2019–June 2020
Emerging markets	MSCI BRIC large-, mid- and small-cap indices	2019; October 2019–June 2020


Scope note: The emerging-market sample uses BRIC indices rather than a complete BRICS index; South Africa is not represented in those BRIC series. Historical data availability and index selection limit the generalizability of the findings.
Methodology
1. Load historical index prices (Yahoo Finance through pandas_datareader for developed markets; local CSV datasets for emerging markets).
2. Calculate returns, covariance and volatility statistics.
3. Generate 2,500 randomly weighted portfolios for each market group and period.
4. Identify the sampled portfolio with the lowest volatility and the sampled portfolio with the highest Sharpe ratio.
5. Compare portfolio returns, volatility, Sharpe ratios and index weights; visualize the risk–return distributions.
The analysis uses historical risk-free-rate assumptions documented in the notebooks. The randomly sampled portfolios approximate the optimization objectives; they are not exact analytical optimizers. Results can vary between runs because the original notebooks do not set a random seed.
Key findings
- The selected developed-market portfolios experienced weaker expected returns and greater volatility in the COVID-period analysis.
- The emerging-market results were mixed rather than consistently showing a higher premium.
- In the COVID-period comparison, the emerging-market maximum-Sharpe portfolio showed higher estimated return and volatility, while the allocation patterns differed substantially between minimum-variance and maximum-Sharpe portfolios.
- Overall conclusion: The project did not consistently confirm an emerging-market premium across the selected indices and periods.
These are findings from the original historical analysis, not independently reproduced or updated estimates.
Notebooks
File	Analysis
[`Final_Developed.ipynb`](Final_Developed.ipynb)	Developed-market indices, 2019
[`Final_Developed_Covid.ipynb`](Final_Developed_Covid.ipynb)	Developed-market indices, COVID-period comparison
[`Final_Emerging.ipynb`](Final_Emerging.ipynb)	Emerging-market indices, 2019
[`Final_Emerging_Covid.ipynb`](Final_Emerging_Covid.ipynb)	Emerging-market indices, COVID-period comparison


Tools and techniques
Python, Jupyter Notebook, pandas, NumPy, SciPy, Matplotlib, pandas_datareader, financial time-series analysis, portfolio simulation, volatility and Sharpe-ratio analysis.
Reproducibility and limitations
The repository is an archive of the original academic analysis, not yet a fully reproducible software package.
- Final_Emerging.ipynb requires BRICS_L_M_S.csv, and Final_Emerging_Covid.ipynb requires BRICS_L_M_S_CORONA.csv. These files are not currently included in the repository. They must be obtained from the original authorized data source before those notebooks can run.
- The developed-market notebooks use the historical pandas_datareader Yahoo Finance interface, which may not work reliably with current versions/services.
- The original analysis uses historical data, risk-free-rate assumptions and annualization choices. It has not been rerun or validated against current market data.
- The notebooks contain saved outputs for reviewing the original analysis even when live data retrieval is unavailable.
To explore the work, open the notebooks directly on GitHub. To rerun it, first resolve the data dependencies and verify library compatibility and the historical calculations.
Portfolio relevance
This project demonstrates Python-based financial data analysis, quantitative modeling, visualization, interpretation of risk–return trade-offs and communication of analytical findings.
