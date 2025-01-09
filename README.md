# Forecasting Macroeconomic Variables

This project provides a framework for forecasting key macroeconomic indicators (GDP growth, inflation, and unemployment rate) for Lithuania using statistical time series models. It incorporates advanced forecasting techniques, error analysis, and robustness checks to deliver accurate predictions and evaluate model performance.

## Key Features

- **Dynamic Time Series Analysis**:
  - Models include AR(1), MA(1), ARMA(1,1), and VAR(1).
  - In-sample period: 1998–2015; holdout period: 2016–2022.
  - Generates one-step, two-step, and three-step forecasts.

- **Visualization**:
  - Historical trends and scatterplots for GDP, inflation, and unemployment.
  - Forecasts overlaid with actual holdout data for clear comparison.

- **Error Analysis**:
  - Computes multiple error metrics: MSE, RMSE, MAE, MSPE, RMSPE, and MAPE.
  - Identifies the best models for each variable based on performance metrics.

- **Robustness Testing**:
  - Repeats forecasting with adjusted in-sample and holdout periods to validate model performance.
  - Includes Diebold-Mariano tests to statistically compare forecasting accuracy.

- **Enhanced Inflation Forecast**:
  - Incorporates additional macroeconomic variables: interest rates, money supply growth, crude oil prices, and exchange rates.
  - Develops a Vector Autoregression (VAR) model to predict inflation for 2023.

---

## Project Structure

### 1. **Data Processing and Visualization**
- **Objective**: Understand historical trends and relationships between variables.
- **Visualization**: Line plots for historical data and scatterplots for variable relationships.
- **Key Insight**: Relationships such as GDP and unemployment align with Okun's Law, while GDP and inflation show weaker correlations.

### 2. **Modeling and Forecasting**
- **Models**:
  - **AR(1)**: Captures short-term autoregressive patterns.
  - **MA(1)**: Focuses on moving average effects.
  - **ARMA(1,1)**: Combines AR and MA components.
  - **VAR(1)**: Multivariate model capturing interdependencies between GDP, inflation, and unemployment.
- **Forecasting**:
  - Generates multi-step forecasts (1-step, 2-step, 3-step).
  - Overlays forecasts with actual holdout data for validation.

### 3. **Error Analysis**
- **Objective**: Evaluate model performance through error metrics.
- **Metrics**:
  - Absolute Metrics: MSE, RMSE, MAE.
  - Percentage Metrics: MSPE, RMSPE, MAPE.
- **Findings**:
  - **GDP**: MA(1) outperforms other models.
  - **Inflation**: MA(1) is the most accurate, closely followed by ARMA(1,1).
  - **Unemployment**: VAR(1) demonstrates superior performance.

### 4. **Robustness Testing**
- **Approach**:
  - Adjust in-sample and holdout periods (e.g., 1999–2016 for in-sample, 2017–2021 for holdout).
  - Validate consistency of model performance across different data splits.
- **Diebold-Mariano Test**:
  - Statistically compares the forecasting accuracy of top-performing models.

### 5. **Enhanced Inflation Forecast for 2023**
- **Additional Variables**:
  - Interest Rates, Money Supply Growth, Crude Oil Prices, and Exchange Rates.
- **Approach**:
  - Identify statistically significant predictors of inflation.
  - Use significant variables in a VAR(1) model to forecast inflation.
- **Result**:
  - Predicted inflation for 2023: **9.55%**.

---

## Key Insights

- **MA(1)** is the best model for forecasting GDP and inflation based on absolute error metrics.
- **VAR(1)** excels in predicting unemployment due to its ability to model interdependencies.
- Incorporating macroeconomic predictors like interest rates and crude oil prices improves inflation forecasts.
