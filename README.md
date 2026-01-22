# trader-behavior-insights
# Trader Behavior Insights – Fear vs Greed Sentiment Analysis (Bitcoin)

## 📌 Project Overview
This project analyzes how **Bitcoin market sentiment** (Fear vs Greed) impacts **trader behavior and performance** using historical trade-level data.  
The goal is to uncover behavior patterns across sentiment regimes and provide actionable insights that can be used for designing smarter trading strategies.

---

## 🎯 Objective
- Understand the relationship between **market sentiment** and **trader performance**
- Compare profitability, volume, and activity during **Fear vs Greed**
- Identify patterns in trading behavior (risk-taking, trade frequency, volume trends)
- Provide strategy recommendations for each sentiment regime

---

## 📂 Datasets Used
1. **Bitcoin Market Sentiment Dataset**
   - Columns: `date`, `classification`
   - Label types: Fear, Greed

2. **Hyperliquid Historical Trader Dataset**
   - Columns: `account`, `coin`, `execution_price`, `size_tokens`, `size_usd`, `side`, `timestamp_ist`, `closed_pnl`, `fee`, etc.

---

## ⚙️ Tools & Technologies
- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**
- Jupyter Notebook / Google Colab

---

## 🔍 Methodology
### 1) Data Cleaning & Preprocessing
- Standardized column names
- Converted time columns into valid datetime format
- Extracted correct trade date from `timestamp_ist`
- Handled missing values and invalid records

### 2) Feature Engineering
Created daily-level trader metrics:
- `total_pnl`
- `avg_pnl`
- `total_volume_usd`
- `avg_trade_usd`
- `trades_count`
- `total_fee`

### 3) Merge with Sentiment Dataset
- Merged datasets on daily `date` to analyze sentiment impact
- Final merged dataset contained:
  - **158 matching days**
  - Greed: **115 days**
  - Fear: **43 days**

### 4) Comparative Analysis
Fear vs Greed analysis performed using:
- Summary statistics tables
- Box plots for PnL & volume
- Trade behavior breakdown by sentiment regime

---

## 📊 Key Insights (High-level)
- **Greed days** show higher trading participation and volume
- **Fear days** show reduced activity with higher uncertainty in outcomes
- Profitability patterns shift across regimes indicating sentiment impacts trader decision-making

---

## ✅ Strategy Recommendations
### 📌 During Greed
- Follow momentum-based setups carefully
- Apply strict stop-loss / risk caps
- Avoid overconfidence & overtrading

### 📌 During Fear
- Use conservative position sizing
- Prefer mean-reversion or higher probability setups
- Preserve capital (high volatility periods)

---

## 📌 Results Included
- Fear vs Greed comparison table
- Boxplots of daily total PnL and volume
- Behavioral breakdown based on sentiment

---

## ▶️ How to Run
1. Clone the repo
```bash
git clone https://github.com/<your-username>/trader-behavior-insights.git
cd trader-behavior-insights
