# Foundation-of-DataScience (Spring 2026) - Notes & Code

## Purpose
Keep clean, reproducible notes, labs, and assignments from the course in one place.

## Topics (high-level)
Bayesian inference, regression (simple/multiple), prediction & overfitting, MCMC, GLMs (logistic/binomial, Poisson), ordered outcomes, hierarchical models, networks, Gaussian processes, missing data, clustering, variational inference.

## Stack
- Python 3.11
- Jupyter (JupyterHub / notebooks)
- NumPy
- SciPy
- Pandas
- PyMC
- ArviZ
- Matplotlib
- Seaborn

## Structure

## Project Highlight: Macro News Sentiment and S&P 500 Direction

One of the main course projects in this repository studies whether daily macro news sentiment is associated with the probability that the next trading day's S&P 500 return is positive.

### Project Overview

- Built a causal-analysis workflow using daily macro news sentiment and S&P 500 return data
- Framed the problem with treatment, outcome, and control variables rather than using a simple correlation-only setup
- Modeled the binary market-direction outcome with Bayesian logistic regression

### What the Project Covered

- Collected and filtered macro-related news sentiment data from the Alpha Vantage NEWS_SENTIMENT API
- Aggregated article-level sentiment into a daily sentiment measure
- Merged the sentiment dataset with daily S&P 500 return data
- Compared baseline, control-only, and full Bayesian logistic regression models
- Ran sensitivity analysis across 1- to 30-trading-day prediction horizons

### My Contribution

- Worked on data preprocessing and final modeling-dataset construction
- Cleaned the S&P 500 return data and merged it with the daily macro news sentiment dataset
- Created the final modeling variables, including `treatment_sentiment`, `same_day_return`, `next_return`, and `next_up`
- Conducted the sensitivity analysis across different trading-day horizons and added a follow-up check for a possible delayed sentiment effect

### Key Findings

- Same-day market return was a much stronger predictor of next-day direction than daily macro sentiment
- Adding sentiment did not meaningfully improve the next-day model beyond the control-only specification
- The clearest exploratory signal appeared at a longer horizon, suggesting that sentiment may matter more with a lag than in immediate next-day prediction

### Why This Project Matters

This project was a good example of combining data cleaning, causal framing, Bayesian modeling, and result interpretation in a finance-related setting. It also helped me think more carefully about the difference between predictive patterns, delayed effects, and causal claims in noisy market data.
