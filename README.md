WealthTech Investment Recommendation Modeller

Project Overview

This project develops a machine learning-based investment recommendation system that generates Buy, Hold, and Sell signals for Apple (AAPL) stock using historical market data and technical indicators.

The system follows a full quantitative trading pipeline including data collection, behavioral analysis, feature engineering, machine learning model training, and strategy backtesting.

The goal is to explore how machine learning models can assist in generating trading signals and evaluating their effectiveness compared to a market benchmark.

---

Project Pipeline

The project is structured as a multi-stage workflow:

1. Data Collection and Cleaning
   
   - Historical stock data for Apple (AAPL) is collected and cleaned.

2. Behavioral Market Analysis
   
   - Market behavior patterns are analyzed to understand price movements and volatility.

3. Feature Engineering
   
   - Technical indicators are created, including:
   - Moving Averages
   - Moving Average Crossovers
   - Rolling Mean
   - Rolling Volatility
   - Momentum
   - Price Change
   - Volume

4. Machine Learning Model Training
   
   - A classification model using XGBoost is trained to predict trading signals (Buy, Hold, Sell).

5. Model Evaluation
   
   - Model performance is evaluated using:
   - Accuracy
   - Classification Report
   - Confusion Matrix

6. Strategy Backtesting
   
   - The predicted signals are applied to simulate a trading strategy and compared with a buy-and-hold market benchmark.

---

Model Details

Algorithm used:

- XGBoost Classifier

Key model parameters:

- Number of estimators: 600
- Max depth: 4
- Learning rate: 0.05
- Subsample: 0.8
- Column sample by tree: 0.8

---

Results

Model Accuracy: ~82%

Trading Performance:

- Strategy Return: -2.97%
- Market Return: 44.55%
- Sharpe Ratio: -0.019
- Maximum Drawdown: -8.9%

Although the model achieved good classification accuracy, the trading strategy did not outperform the market benchmark. This highlights an important challenge in financial machine learning: high prediction accuracy does not always translate into profitable trading strategies.

---

Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Jupyter Notebook

---

Project Structure

WEALTHTECH_INVESTMENT_RECOMMENDATION_MODELLER/

data/
    aapl_day1_cleaned.csv
    aapl_day3_features.csv
    day_7.csv
    day_9_backtesting_results.csv

notebooks/
    data_collection.ipynb
    day_6_behavioral_analysis.ipynb
    day_7_feature_engineering.ipynb
    day_8_model_training.ipynb
    day_9_backtesting.ipynb
    day_10_final_analysis.ipynb

README.md

---

Key Insights

- Moving average indicators and volatility features were the most influential predictors.
- The model successfully identified stable market conditions but struggled with rare Buy and Sell signals.
- Backtesting results emphasize the importance of evaluating trading strategies using financial performance metrics, not just prediction accuracy.

---

Future Improvements

Potential improvements for future work include:

- Additional feature engineering using more technical indicators
- Hyperparameter optimization
- Alternative machine learning models
- Reinforcement learning approaches for trading strategies
- Risk management and portfolio optimization techniques

---

Conclusion

This project demonstrates a complete machine learning workflow for financial market prediction and algorithmic trading research. It highlights both the potential and limitations of using machine learning techniques for investment decision support.
