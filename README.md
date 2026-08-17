# quantitative-investment-analysis
Quantitative analysis of stock returns using regression, backtesting, risk analysis, and Monte Carlo simulation

# Quantitative Investment Analysis

A quantitative research project exploring whether historical market data can provide useful information for evaluating investment risk, predicting short-term returns, and understanding possible future outcomes.

## Research Question

**Can historical returns, volatility, moving-average behavior, and trading volume provide useful information for evaluating and predicting stock returns?**

This project compares **Apple (AAPL)** with the **S&P 500 ETF (SPY)** and evaluates both historical performance and model-based evidence.

## Project Objectives

The project applies concepts from statistics, quantitative finance, and programming to:

* Analyze historical stock-market data
* Calculate and compare investment returns and risk
* Engineer quantitative financial features
* Build multiple linear regression models
* Evaluate models using unseen test data
* Backtest a simple model-driven investment strategy
* Examine the risk of overfitting
* Simulate possible future prices using Monte Carlo simulation
* Compare model predictions with uncertainty-based simulations
* Develop an evidence-based investment conclusion

## Data

Historical daily market data is obtained from Yahoo Finance using the Python `yfinance` library.

The primary securities analyzed are:

* **AAPL — Apple Inc.**
* **SPY — SPDR S&P 500 ETF Trust**

The analysis uses daily closing prices and trading volume.

## Feature Engineering

The project creates several quantitative features from the historical data:

| Feature              | Purpose                                                     |
| -------------------- | ----------------------------------------------------------- |
| Daily Return         | Measures the daily percentage change in price               |
| 5-Day Moving Average | Measures the short-term price trend                         |
| MA Distance          | Measures how far price is above or below its moving average |
| 20-Day Volatility    | Measures recent variability in returns                      |
| Volume               | Measures trading activity                                   |
| Tomorrow's Return    | Target variable used by the regression model                |

## Exploratory Data Analysis

The exploratory analysis compares AAPL and SPY using:

* Normalized investment growth
* Daily return distributions
* Rolling volatility
* Maximum daily gains and losses
* Average historical returns
* Annualized return and volatility estimates

## Regression Model

A multiple linear regression model is used to investigate whether historical market features contain information about the following day's return.

The model uses:

**Predictors**

* Daily Return
* MA Distance
* Volatility
* Volume

**Target**

* Tomorrow's Return

## Train/Test Evaluation

The dataset is divided chronologically into:

* **80% training data**
* **20% testing data**

The model is trained only on the earlier observations and evaluated on later, unseen observations.

Performance is evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R²

This helps determine whether relationships found in historical data generalize to new market observations.

## Backtesting

A simple investment strategy is tested using the model's predictions.

The strategy invests when the model predicts a positive next-day return and remains out of the market otherwise.

Its historical performance is compared with a buy-and-hold benchmark.

The purpose of the backtest is not to prove that the strategy will work in the future, but to evaluate how it would have performed on historical data that was not used to fit the model.

## Monte Carlo Simulation

The project also uses Monte Carlo simulation to examine uncertainty rather than attempting to predict one exact future price.

Thousands of possible 30-day price paths are generated using historical return and volatility estimates.

The simulation is used to estimate:

* Mean simulated final price
* Median simulated final price
* Probability of finishing above the current price
* 5th percentile outcome
* 95th percentile outcome

## Results

**To be completed after the analysis is finished.**

This section will summarize the results for AAPL and SPY, including regression performance, backtesting results, risk measures, and Monte Carlo outcomes.

## Key Findings

**To be completed after evaluating the results.**

The conclusions will be based on the evidence produced by the analysis rather than assuming beforehand that either investment or model will perform better.

## Limitations

This project is an educational quantitative analysis and has several important limitations:

* Historical performance does not guarantee future performance.
* Financial-market relationships can change over time.
* Daily stock returns contain substantial randomness and are difficult to predict.
* Regression results depend on the features and historical period selected.
* Monte Carlo simulations depend on assumptions derived from historical data.
* The basic backtest does not fully account for transaction costs, taxes, slippage, or market impact.
* Statistical relationships do not necessarily imply causation.
* Results should not be interpreted as investment advice.

## Technologies

* Python
* pandas
* NumPy
* scikit-learn
* Matplotlib
* yfinance
* R
* Google Colab
* GitHub

## Project Status

🚧 **In Progress**

The quantitative analysis and model evaluation are currently being developed.

---

*This project was created for educational purposes to apply concepts in statistics, programming, quantitative finance, regression, backtesting, and simulation. It is not financial advice.*
