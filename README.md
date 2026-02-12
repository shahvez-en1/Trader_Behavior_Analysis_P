# Data Science Intern Project: Trader Behavior vs Market Sentiment

## Objective:
The goal of this project is to analyze how *market sentiment* (Fear/Greed) relates to *trader behavior* and *performance* on Hyperliquid. The objective is to uncover patterns that could inform smarter trading strategies and improve decision-making in the market.

## Project Structure:
The project consists of the following files:

- trader_behavior_analysis.ipynb: Jupyter notebook for data cleaning, feature engineering, analysis, model training, and evaluation.
- data/: Folder containing the datasets used for analysis (Bitcoin Market Sentiment and Historical Trader Data).
- charts/: Folder containing visualizations created during analysis.
- README.md: This file.

## Methodology:
### Step 1: Data Loading and Cleaning
- Loaded *Bitcoin Market Sentiment* and *Historical Trader Data* datasets.
- Checked for missing values and duplicates in the datasets.
- Converted *timestamps* to datetime format and aligned the data by *date*.

### Step 2: Feature Engineering and Key Metrics Calculation
- Calculated key metrics such as *PnL, **win rate, **average trade size, and **leverage distribution*.
- Applied *one-hot encoding* to the classification column (Fear/Greed).
  
### Step 3: Trader Behavior Analysis
- Compared trader performance on *Fear* vs *Greed* days, as well as *Extreme Fear* and *Extreme Greed* days.
- Analyzed *trade frequency, **leverage usage, **win rates, and **position sizes* across different sentiment conditions.

### Step 4: Predictive Modeling
- Used *Random Forest* model and *Logistic Regression* to predict trader performance based on market sentiment and trader behavior.
- Applied *RandomizedSearchCV* for *hyperparameter tuning* and *cross-validation* to improve model performance.

### Step 5: Actionable Insights and Strategy Recommendations
- *Insight 1: Traders tend to use **higher leverage* during *Greed* days, increasing both risk and potential reward.
- *Insight 2: **Win rate* is lower during *Fear* days, suggesting that traders are more cautious or losing in high volatility.

*Strategies*:
1. *During Greed days*: Increase leverage for high-frequency traders who consistently perform well.
2. *During Fear days: Reduce leverage and apply stricter **risk management* protocols (e.g., stop-loss) for high-risk traders.

## Insights:
1. *Leverage Usage: Traders tend to use **higher leverage* during *Greed* days, which increases both risk and potential reward.
2. *Performance on Fear Days: Traders are more cautious during **Fear* days, resulting in a lower *win rate*.
3. *Behavior Segmentation*: Traders using high leverage or trading frequently perform differently based on market sentiment.

## Model and Performance:
- *Random Forest Classifier* and *Logistic Regression* models were trained to predict trader performance using *market sentiment* and *trading behavior* features.
- The performance was evaluated using *accuracy* and *cross-validation*.

### Performance Metrics:
- *Accuracy (Random Forest)*: 83.02%
- *Accuracy (Logistic Regression)*: 58.7% (initial model)

### Hyperparameter Tuning:
- *RandomizedSearchCV* was used to find the best hyperparameters for the *Random Forest model*, resulting in improved accuracy.

## How to Run the Project:
1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
