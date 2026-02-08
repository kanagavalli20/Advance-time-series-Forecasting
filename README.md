Advanced Time Series Forecasting using Prophet with External Regressors
Project Overview

This project implements an advanced time series forecasting pipeline using Facebook Prophet enhanced with multiple external regressors. The objective is to improve forecast accuracy by incorporating real-world exogenous variables and to benchmark the optimized Prophet model against a traditional SARIMA baseline.

The project focuses on production-quality implementation, proper time-series validation, and interpretability of model components such as trend, seasonality, and regressor effects.

Dataset Description

Daily time series data spanning more than 4 years

Strong weekly and yearly seasonality

Clear long-term upward trend

Synthetic but realistic data generation

External Regressors Used

Marketing Spend

Temperature

Promotion Indicator

These regressors simulate real business drivers influencing demand.

Methodology
1. Data Generation

A realistic daily time series is programmatically generated with:

Trend component

Weekly and yearly seasonal patterns

Noise

Exogenous variables affecting the target series

2. Train–Test Strategy

Time-aware split (80% training, 20% testing)

No random shuffling to avoid data leakage

3. Baseline Model

SARIMA model implemented using statsmodels

Captures short-term seasonality and autocorrelation

Used as a benchmark for comparison

4. Prophet Model

Prophet with weekly and yearly seasonality

External regressors explicitly added

Tuned hyperparameters:

changepoint_prior_scale

seasonality_prior_scale

additive seasonality mode

5. Evaluation Metrics

Models are evaluated using:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

Mean Absolute Percentage Error (MAPE)

Results Summary

Prophet with external regressors consistently outperforms SARIMA

Improved accuracy across all evaluation metrics

External regressors help explain variations that SARIMA cannot capture

Prophet effectively models trend changes and seasonal effects

External Regressor Impact

Marketing spend shows strong positive influence on forecasts

Promotion periods introduce sharp demand spikes captured well by Prophet

Temperature improves seasonal alignment of predictions

Key Insights

Including realistic external regressors significantly enhances forecast performance by allowing the model to attribute variations to real-world drivers rather than forcing the trend component to absorb unexplained patterns.

Technologies Used

Python

Prophet

statsmodels

scikit-learn

NumPy

Pandas

How to Run

Install required libraries

Run the provided Python file

The script will:

Generate data

Train SARIMA and Prophet models

Compare performance metrics

Output regressor influence analysis

Conclusion

This project demonstrates that Prophet with well-chosen external regressors provides superior forecasting performance compared to classical SARIMA models, especially in complex, multi-seasonal time series with real-world influencing factors.
