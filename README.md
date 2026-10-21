# NBA MVP Prediction

## Project Overview

This project investigates whether information available before the start of an NBA regular season can predict the league's Most Valuable Player Award (MVP).

Using historical NBA player statistics, team performance, MVP voting results, and available preseason expectations, the project will develop a machine learning model to estimate MVP probabilities for the 2026–27 season.

The project will combine Python-based data analysis and modeling, a Monte Carlo simulation, SQL-based data management, and Power BI visualization.

## Research Question

**Can information available before the NBA season begins accurately predict who will win MVP at the end of the season?**

## Objectives

* Collect and consolidate historical NBA MVP voting results and player statistics.
* Build player-season and team-season datasets using information available before each target season.
* Engineer features that capture player performance history, age, team strength, and preseason expectations.
* Train and evaluate predictive models using chronological historical backtesting.
* Simulate 10,000 possible MVP voting outcomes to estimate candidate probabilities and uncertainty.
* Build an interactive Power BI dashboard to communicate predictions, historical performance, and model limitations.

## Data Sources

Planned sources include:

* [Basketball-Reference](https://www.basketball-reference.com/awards/) — historical MVP voting and award results.
* [NBA.com/stats](https://www.nba.com/stats) — player and team statistics.
* [NBA API Python package](https://github.com/swar/nba_api) — programmatic access to available NBA statistics.
* Archived preseason projections and odds, where reliable historical records are available.

Source coverage, licensing, and data quality will be assessed during data collection.

## Methodology

1. **Data collection:** Gather historical MVP voting, player statistics, team results, and available preseason expectations.
2. **Data preparation:** Standardize seasons, player identifiers, team identifiers, and statistical definitions.
3. **Feature engineering:** Create features using only information available before the target season's opening night.
4. **Model development:** Compare baseline approaches with suitable machine learning models.
5. **Historical backtesting:** Evaluate predictions chronologically, training only on information from prior seasons.
6. **Monte Carlo simulation:** Run 10,000 simulations of candidate performance, eligibility, and MVP voting outcomes.
7. **Visualization:** Present forecasts, historical backtesting, and model evaluation in Power BI.

## Preventing Data Leakage

A central design requirement is that every historical prediction must use only information available before that season began.

Statistics, standings, award results, and other information from the target season will be used as outcomes for evaluation, not as preseason model inputs.

Historical MVP eligibility rules will be represented according to the season being evaluated. The NBA's 65-game award eligibility requirement will not be applied retroactively to seasons when it was not in effect.

## Technology Stack

* **Python:** Data preparation, exploratory analysis, feature engineering, modeling, and simulation.
* **Pandas / NumPy:** Data manipulation and numerical computation.
* **Scikit-learn:** Model training and evaluation.
* **PostgreSQL / SQL:** Structured storage and querying of historical data and predictions.
* **Power BI:** Interactive dashboard and reporting.
* **Git / GitHub:** Version control and project documentation.

Additional libraries will be selected as the project develops.

## Repository Structure

```text
nba-mvp-prediction/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
├── sql/
├── reports/
│   └── figures/
├── .gitignore
└── README.md
```

## Evaluation

Model performance will be assessed using chronological backtesting and appropriate classification and probability metrics. Evaluation will consider whether the model identifies the eventual winner, ranks serious candidates highly, and produces reasonably calibrated probabilities.

Results will be compared against simple baselines. Limitations caused by incomplete historical preseason information and the relatively small number of MVP winners will be documented.

## Project Status

**Status:** Initial setup and data collection planning.

Historical data collection, data validation, feature engineering, model development, and dashboard creation are planned next.

## Disclaimer

This project is for educational and analytical purposes. Predictions represent estimates with uncertainty, not guarantees of future NBA award outcomes.
