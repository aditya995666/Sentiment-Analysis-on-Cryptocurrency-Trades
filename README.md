Bitcoin Market Sentiment Project

📘 Project Overview

Objective:
The project aims to explore how market sentiment, particularly the Fear & Greed Index, influences trader behavior and performance in the cryptocurrency market. By analyzing historical trading data and sentiment indicators, the goal is to identify patterns that can inform smarter trading strategies.

Key Components

Datasets:

Fear & Greed Index: Provides daily sentiment scores ranging from Extreme Fear, Fear, Neutral, Greed, to Extreme Greed, indicating overall market emotions.

Hyperliquid Historical Trader Data: Contains detailed information on individual trades, including account, coins, size in USD, Closed PnL, FearGreedValue, and Profit.

Analysis Techniques

Data Preprocessing: Cleaning and merging datasets to align sentiment data with trading activity.

Exploratory Data Analysis (EDA): Visualizing relationships between sentiment scores and trading outcomes.

Statistical Analysis: Investigating correlations between market sentiment and trader performance metrics.

Methodology

Data Integration:
The Fear & Greed Index data is merged with the Hyperliquid trader data based on the date, ensuring each trade is associated with the corresponding market sentiment score.

Exploratory Data Analysis (EDA):
Various visualizations are created to understand the distribution of sentiment scores and their potential impact on trading behavior, including:

Histograms and box plots to examine the spread of sentiment scores.

Line charts to observe trends over time.

Performance Metrics Analysis:
Key performance indicators (KPIs) such as Closed PnL, trade size, and execution price are analyzed in relation to sentiment scores to identify significant patterns or anomalies.

Statistical Testing:
Hypothesis testing is conducted to determine if there are statistically significant differences in trader performance during periods of extreme fear or greed compared to neutral sentiment periods.

📈 Key Findings

Sentiment Correlation:
A positive correlation is observed between high Fear & Greed Index scores (indicating greed) and increased trade sizes, suggesting that traders are more willing to take larger positions during periods of optimism.

Performance Variability:
Trader performance, as measured by Closed PnL, shows greater volatility during extreme sentiment periods. This indicates that while potential gains may be higher, the risks are also amplified.

Risk Management Implications:
Incorporating sentiment indicators into risk management strategies is important. Traders may consider adjusting position sizes or implementing stop-loss orders during periods of extreme sentiment to mitigate potential losses.

📊 Visualizations

The notebook includes several visualizations to illustrate the findings:

Sentiment Distribution:
A histogram displaying the frequency of different sentiment scores over time.

Trade Size vs. Sentiment:
A scatter plot showing the relationship between trade size and sentiment scores.

Performance vs. Sentiment:
A line chart depicting how trader performance varies with sentiment over time.

🧠 Insights and Recommendations

Market Timing:
Traders may benefit from aligning their strategies with prevailing market sentiment. For instance, adopting a more conservative approach during periods of extreme fear could help preserve capital.

Sentiment-Based Alerts:
Implementing automated alerts based on sentiment thresholds can assist traders in making timely decisions, such as entering or exiting positions.

Further Research:
Future studies could explore the impact of sentiment on Bitcoin and other cryptocurrencies, incorporating additional factors like social media sentiment or macroeconomic indicators.
