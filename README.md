# LocalBoost

A collaborative analytics prototype for exploring small-business sales data. The Flask application accepts a CSV upload, runs forecasting and investor-analysis modules, and prepares plots and scores for a results view. The [React/Vite interface](https://github.com/dhruv-ar/LocalBoost-Frontend) is in a separate repository.

## Analysis flow

1. Upload a sales CSV through the Flask entry point in `app.py`.
2. Run `Forecasting.model.sales_analysis` with a 30-step forecast horizon.
3. Run `InvestorAnalysis.investor_analysis.run_investor_analysis` for scores and supporting plots.
4. Pass the analysis outputs to the results view.

## Repository map

- `app.py` - Flask upload and results routes
- `Forecasting/` - sales and revenue forecasting
- `InvestorAnalysis/` - investor-oriented metrics and plots
- `data_processing.py` - data preparation utilities
- `static/plots/` - generated visualization assets
- `requirements.txt` - Python dependencies

## Stack

Python, Flask, pandas, NumPy, scikit-learn, statsmodels, Matplotlib, and Plotly.

## Status

This repository is a team prototype, not a deployed production service. The Flask entry point references HTML templates that are not present in this repository, so the checked-in code is best read as the analysis and routing prototype rather than a one-command runnable application. It also uses development-mode settings and would need input validation and production hardening before deployment.

## Related repository

[LocalBoost frontend](https://github.com/dhruv-ar/LocalBoost-Frontend)
