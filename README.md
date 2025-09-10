📊 Trader Behavior Insights under Bitcoin Market Sentiment
Author: Atharva Chavan (Junior Data Scientist Candidate)

#Project Goal
This project analyzes historical trading data from Hyperliquid alongside Bitcoin market sentiment (Fear vs. Greed Index) to understand how market emotions influence trader behavior and performance. The goal is to identify actionable patterns that could lead to smarter trading strategies.

#Methodology
Data Loading & Preprocessing:

#Loaded historical trading data (historical_data.csv) and sentiment data (fear_greed_index.csv).
Converted timestamp columns to datetime objects for consistent handling.
Created a date-only column for merging the datasets.
Simplified column names for clarity.
Merged the trader and sentiment dataframes on the date.
Identified and removed outliers in closed_pnl and size_usd using the 1.5 * IQR rule to ensure a more robust analysis of typical trader behavior.
Exploratory Data Analysis (EDA):

#Visualized the distribution of market sentiment to understand the frequency of different emotional states.
Analyzed the distribution of trader PnL (Profit and Loss) under different sentiments, both before and after outlier removal.
Calculated and visualized the win rate across different sentiment categories.
Examined the distribution of trade sizes (size_usd) by sentiment.
Investigated symbol performance across different sentiment categories, focusing on top-performing symbols.
Explored the correlation between closed_pnl, execution_price, size_usd, and fee.
Analyzed the distribution of trade directions (side, Direction) within each sentiment category after outlier removal.
Key Findings:

#Market sentiment is frequently in states of "Fear" or "Greed."
"Extreme Greed" sentiment was associated with the highest average PnL and win rate, even after outlier removal, suggesting potential profitability in optimistic markets.
Average trade size varies with sentiment, with "Fear" and "Greed" generally having larger average sizes before outlier removal. After outlier removal, "Extreme Fear" and "Fear" still showed slightly larger average sizes.
Specific cryptocurrencies exhibit varying performance depending on the market sentiment.
Correlations between PnL and individual trade features like size, price, and fee are relatively weak, indicating that sentiment and potentially other factors play a significant role in trade outcomes.
Analysis of trade direction after outlier removal revealed differences in trading activity across sentiments (e.g., prevalence of "Open Long" in Extreme Greed vs. "Open Short" in Extreme Fear).
Implications for Smarter Trading Strategies
The findings suggest that incorporating Bitcoin market sentiment into trading strategies could be beneficial:

###Sentiment-Aware Timing: Consider adjusting trading activity based on the prevailing sentiment, potentially being more aggressive during periods of "Extreme Greed" which historically showed higher average profitability and win rates in this dataset.
###Adaptive Risk Management & Trade Sizing: The observation of smaller, more frequent winning trades during "Extreme Greed" could inform dynamic trade sizing strategies.
###Sentiment-Specific Symbol Selection: Focus on trading assets that have historically performed well in the current market sentiment.
###Further Research: Explore additional factors like trade duration, specific trading strategies employed by profitable traders, and external market events to build more comprehensive trading models.
#Getting Started
To replicate this analysis, clone the repository and ensure you have the necessary data files (historical_data.csv and fear_greed_index.csv) in the appropriate directory. The code can be run in a Jupyter Notebook or Google Colab environment.

##Libraries Used
pandas
numpy
matplotlib
seaborn

Implement machine learning models to predict trade outcomes based on sentiment and other features.
This project provides a foundational analysis of how market sentiment influences trader behavior. The insights gained can serve as a starting point for developing more sophisticated and sentiment-aware trading approaches.
