Hyperliquid Trader Behavior vs Market Sentiment

Objective : The goal of this project is to analyze how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on Hyperliquid.
We aim to uncover patterns that can help design smarter, sentiment-aware trading strategies.

Datasets
Bitcoin Market Sentiment Dataset :
Fields: timestamp, classification (Fear/Greed)
Hyperliquid Trader Dataset :
Fields: account, execution price, size, side, timestamp, closed PnL, etc.

Methodology

1. Data Preparation

Cleaned missing values and removed duplicates
Converted timestamps to standard datetime format
Aligned both datasets at daily level
Merged trading data with sentiment data
2. Feature Engineering

Created key trading metrics:

Daily PnL per trader
Win rate (profitable trades ratio)
Number of trades per day
Average trade size
Long/Short ratio

Analysis & Findings

1. Performance vs Sentiment

Trader PnL shows higher variability during Greed periods
Indicates increased risk-taking and market volatility

2. Behavioral Changes

During Greed:

Higher trade frequency
More aggressive trading behavior

During Fear:

Reduced activity
More cautious decision-making

3. Trader Segmentation

Frequent vs Infrequent Traders

Frequent traders execute more trades
However, higher activity does not guarantee higher profitability
Suggests overtrading behavior, especially in Greed markets

Visualizations

PnL Distribution by Sentiment
Trade Frequency by Sentiment

Strategy Recommendations

Strategy 1 — Control Risk During Greed

Reduce trade frequency
Limit position sizes
Avoid emotional overtrading

Strategy 2 — Trade Selectively During Fear

Focus on high-quality setups
Take advantage of market inefficiencies
Maintain disciplined execution

Bonus: Predictive Modeling
Built a Random Forest model to predict trader profitability
Features used:

Trade frequency
Position size
Win rate

Model provides a baseline for behavior-based prediction

Repository Structure
hyperliquid-sentiment-analysis/
│
├── data/                         # Raw datasets
├── outputs/                      # Charts and visualizations
│   ├── pnl_distribution.png
│   ├── trade_frequency.png
│
├── notebook.ipynb               # Main analysis notebook
├── final_processed_data.csv     # Cleaned dataset
├── requirements.txt             # Dependencies
├── README.md                    # Project documentation

How to Run

Install dependencies:

pip install -r requirements.txt

Run the notebook:

jupyter notebook notebook.ipynb

Conclusion

This project demonstrates that market sentiment significantly influences trader behavior and outcomes.

By adapting strategies based on sentiment:

Risk can be reduced during volatile phases
Opportunities can be better captured during cautious market conditions

Future Improvements

Add leverage-based segmentation
Build advanced predictive models
Create a Streamlit dashboard for interactive analysis

👨‍💻 Author : Jeet Mishra
