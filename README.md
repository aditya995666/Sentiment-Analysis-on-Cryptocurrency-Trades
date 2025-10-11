# Slide 1: Title Slide
# Bitcoin Market Analysis and Price Prediction

# Slide 2: Introduction
# Project Goal:

To analyze the Bitcoin market by combining historical trading data with market sentiment data (Fear & Greed Index) to uncover insights into trading behavior and build a predictive model.

# Objectives:

Data Integration: Merge and clean historical trade data with daily market sentiment data.

Exploratory Data Analysis (EDA): Visualize and analyze the combined dataset to identify relationships between market sentiment, trade size, direction, and profitability.

Predictive Modeling: Develop a model to predict trading outcomes based on the available features.

# Slide 3: Data Loading and Initial Exploration
Data Sources:

historical_data.xls: A transactional dataset containing detailed information about individual trades, including execution price, size, side, and profit and loss (PnL).

fear_greed_index.xls: A time-series dataset providing a daily sentiment score for the market, classified into categories like "Extreme Fear," "Fear," "Neutral," "Greed," and "Extreme Greed."

Initial Findings:

The trade dataset (trade_df) contains 211,224 rows and 16 columns.

The sentiment dataset (sentiment_df) contains 2,644 rows and 4 columns.

# Slide 4: Data Preprocessing and Cleaning
Steps Taken:

Column Renaming: Renamed columns in the sentiment data for better readability (e.g., value to FearGreedValue).

Date Conversion: Converted the Timestamp IST and SentimentDate columns to a consistent date format to enable merging.

Data Merging: Performed a left merge on the two datasets using the date as the key to create a unified DataFrame.

Handling Missing Values: A small number of rows (6) with missing sentiment data after the merge were identified and removed to ensure data quality.

Duplicate Check: Confirmed that there were no duplicate rows in the final dataset.

# Slide 5: Exploratory Data Analysis (EDA) - Sentiment Distribution
Distribution of Market Sentiment:

The analysis of the 'classification' column reveals the frequency of different market sentiments:

Fear: 61,837 instances

Greed: 50,303 instances

Extreme Greed: 39,992 instances

Neutral: 37,686 instances

Extreme Fear: 21,400 instances

Insight: The market has spent more time in a state of "Fear" than any other sentiment, suggesting a predominantly cautious or bearish outlook during the observed period.

(A histogram showing the distribution of sentiment classifications would be included here.)

# Slide 6: EDA - Correlation Analysis
Correlation Heatmap:

A heatmap of the correlation matrix for the numerical features was generated.

Key Observations:

There is a moderate positive correlation between Size Tokens and Size USD, which is expected as the token size directly impacts the USD value of the trade.

No other strong linear correlations were immediately apparent between the features, suggesting that more complex, non-linear relationships may exist.

(A heatmap visualization would be displayed on this slide.)

# Slide 7: EDA - Profitability Analysis by Sentiment
Average Closed PnL per Market Sentiment:

Extreme Greed: Highest average profit, suggesting that trades made during periods of extreme market optimism tend to be the most profitable.

Fear: Second highest average profit, indicating that buying during fearful market conditions ("buying the dip") can also be a profitable strategy.

Neutral & Extreme Fear: Showed the lowest average profits.

Conclusion: Market sentiment appears to have a significant impact on trading profitability.

(A bar chart illustrating the average "Closed PnL" for each sentiment would be included here.)

# Slide 8: EDA - Trade Size Analysis by Sentiment
Average Trade Size (USD) per Market Sentiment:

Fear: The largest average trade sizes were observed during periods of "Fear." This could indicate that larger investors or "whales" are more active when the market is fearful.

Extreme Greed: The smallest average trade sizes occurred during "Extreme Greed," possibly due to smaller retail investors entering the market at its peak.

Insight: Trade sizes vary significantly with market sentiment, with larger trades being more common in fearful markets.

(A bar chart showing the average "Size USD" per sentiment would be presented here.)

# Slide 9: EDA - Distribution of PnL and Trade Size
Distribution of Closed PnL and Size USD:

Closed PnL: The distribution of "Closed PnL" is heavily skewed, with a large number of trades resulting in small gains or losses and a few outliers with very large profits or losses.

Size USD: Similarly, the distribution of trade size in USD is also skewed, with most trades being of a smaller value.

Implication: The market is characterized by many small trades and a few very large ones, which can have a disproportionate impact on overall market trends.

(Two histograms, one for "Closed PnL" and one for "Size USD," would be shown on this slide.)

# Slide 10: EDA - Profitability by Trade Direction and Coin
Profitability by Trade Direction:

The analysis shows the count of profitable vs. non-profitable trades for both "Buy" and "Sell" directions.

This visualization helps in understanding whether buying or selling has been more profitable on average.

Profit Ratio per Coin:

A bar chart of the top 100 coins by their profit ratio was created.

This allows for the identification of the most consistently profitable cryptocurrencies in the dataset.

(Two charts: a count plot for "Profit" by "Direction" and a bar chart for "Profit ratio per Coin" would be included.)

# Slide 11: Model Building and Prediction
Model Selection:

A Linear Regression model was chosen to predict trading outcomes. Note: The notebook implies the use of a classification model to predict 'Profit' (True/False) or a regression model for 'Closed PnL'. This slide assumes a classification task for simplicity.

Features and Target:

Features (X): Execution Price, Size Tokens, Size USD, Start Position, FearGreedValue, etc.

Target (y): Profit (a boolean indicating whether a trade was profitable).

Results:

The model was trained and evaluated, with a comparison of 'Actual' vs. 'Predicted' values indicating its performance.

The model was saved using pickle for future use, named best-model.pkl.

# Slide 12: Conclusion and Future Work
Key Takeaways:

Market sentiment (Fear & Greed Index) is a valuable indicator for understanding trading behavior, profitability, and average trade size.

"Extreme Greed" and "Fear" periods present distinct opportunities for profitability.
