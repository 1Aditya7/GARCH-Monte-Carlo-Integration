# GARCH Model Integration with Monte Carlo Simulation for Intraday Trading Strategy Analysis

This project implements an intraday trading strategy combining volatility prediction using GARCH models with intraday technical indicators. The strategy aims to optimize trading decisions based on predicted volatility and intraday signals, evaluated through Monte Carlo simulations.

## Project Overview

The project is structured into several key components:

1. **Data Preparation:**
   - Two datasets are used:
     - `simulated_daily_data.csv`: Contains daily stock data.
     - `simulated_5min_data.csv`: Contains 5-minute intraday stock data.

2. **Volatility Prediction:**
   - **GARCH Modeling:** Predicts daily volatility using GARCH(1,3) models.
   - Rolling window approach to forecast variance based on daily log returns.

3. **Signal Generation:**
   - **Daily Signal:** Determines buy/sell signals based on predicted volatility premiums.
   - **Intraday Signal:** Uses technical indicators (RSI, Bollinger Bands) on 5-minute data for intraday signals.

4. **Strategy Implementation:**
   - Combines daily and intraday signals to determine trading actions.
   - Calculates strategy returns based on combined signals.

5. **Monte Carlo Simulations:**
   - **Simulation Function:** Implements Monte Carlo simulations to assess strategy performance under different scenarios.
   - Evaluates risk metrics such as Value at Risk (VaR) and Conditional VaR (CVaR) from simulations.

6. **Model Comparison:**
   - Compares GARCH and GJR-GARCH models for volatility estimation.
   - Analyzes news impact curves to understand volatility responses to shocks.

## Files and Usage

- **Python Scripts:**
  - `intraday_trading_strategy.py`: Main script implementing the entire strategy including Monte Carlo simulations.
  - Dependencies: `matplotlib`, `pandas`, `numpy`, `arch`, `pandas_ta`.

- **Datasets:**
  - `simulated_daily_data.csv`: Daily stock data used for volatility prediction.
  - `simulated_5min_data.csv`: 5-minute intraday stock data used for intraday signals.

- **Outputs:**
  - Plots:
    - Strategy returns over time.
    - Monte Carlo simulations of strategy returns.
    - News impact curves for GARCH models.

## Running the Code

1. **Environment Setup:**
   - Ensure Python 3.x and required libraries (`matplotlib`, `pandas`, `numpy`, `arch`, `pandas_ta`) are installed.

2. **Execution:**
   - Run `intraday_trading_strategy.py` in a Python environment.
   - Adjust parameters (e.g., model parameters, dataset paths) as needed.

## Results

- **Strategy Returns Plot:** Visualizes cumulative returns of the implemented intraday trading strategy.

- **Monte Carlo Simulations:** Provides simulations of potential strategy outcomes under different scenarios, evaluating risk metrics such as VaR and CVaR.

- **Volatility Modeling:** Compares GARCH and GJR-GARCH models for volatility forecasting, illustrating news impact curves.

## Conclusion

This project demonstrates the application of GARCH models, intraday technical indicators, and Monte Carlo simulations in building an effective intraday trading strategy. By combining volatility predictions with intraday signals and assessing performance through simulations, the strategy aims to optimize trading decisions and manage risk effectively.
