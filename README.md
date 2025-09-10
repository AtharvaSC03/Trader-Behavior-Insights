
# 📊 Trader Behavior Insights under Bitcoin Market Sentiment

**Author:** Atharva Chavan (Junior Data Scientist Candidate)

---

## 🚀 Project Overview

This project analyzes **historical trading data from Hyperliquid** alongside the **Bitcoin Fear & Greed Index** to understand how **market emotions influence trader behavior and performance**.

The goal is to uncover actionable patterns and insights that can support the development of **smarter, sentiment-aware trading strategies** in the crypto market.

---

## 🛠 Methodology

### 🔹 Data Loading & Preprocessing

* Loaded `historical_data.csv` (trader data) and `fear_greed_index.csv` (sentiment data).
* Converted timestamps into proper datetime objects.
* Created date-only keys for joining the datasets.
* Renamed and simplified column names for clarity.
* Merged trader and sentiment data on the **date column**.
* Identified and removed **outliers** in `closed_pnl` and `size_usd` using the **1.5 × IQR rule** to improve robustness.

### 🔹 Exploratory Data Analysis (EDA)

* Visualized **distribution of sentiment** categories (Fear, Greed, Extreme Fear, Extreme Greed).
* Compared **PnL distributions** under different sentiments (with and without outlier removal).
* Calculated **win rates** across sentiment categories.
* Examined **trade size behavior** (`size_usd`) under different sentiments.
* Evaluated **symbol performance** segmented by sentiment.
* Explored correlations between **PnL, execution price, trade size, and fees**.
* Analyzed **trade direction (Buy/Sell, Long/Short)** across sentiment states.

---

## 📈 Key Findings

* 🟢 **Extreme Greed** sentiment was associated with the **highest average PnL and win rate**, suggesting optimism-driven profitability.
* 📊 **Trade sizes** tended to be larger during Fear and Greed states (even after outlier removal).
* 💡 Certain **cryptocurrencies responded differently** to sentiment shifts, highlighting the importance of sentiment-specific asset selection.
* 🔗 Correlations between PnL and features like trade size, price, or fee were **weak**, suggesting sentiment itself (and external factors) plays a stronger role.
* 📉 **Trade direction** patterns shifted with sentiment (e.g., more **Open Long** during Extreme Greed, more **Open Short** during Extreme Fear).

---

## 💡 Implications for Smarter Trading

* **📊 Sentiment-Aware Timing:** Increase trading activity during **Extreme Greed** phases, historically associated with higher profitability.
* **⚖️ Adaptive Risk Management:** Dynamically adjust **trade size and leverage** depending on prevailing sentiment.
* **🎯 Sentiment-Specific Asset Focus:** Prioritize assets that have historically shown better performance under the current sentiment regime.
* **🔍 Further Research:** Incorporate **trade duration, trader-level strategies, and external events** into models for improved predictions.

---

## 🖥 Getting Started

1. Clone this repository:

   ```bash
   git clone https://github.com/AtharvaSC03/Trader-Behavior-Insights.git
   cd Trader-Behavior-Insights
   ```
2. Place the datasets (`historical_data.csv`, `fear_greed_index.csv`) in the root folder.
3. Run the Jupyter Notebook or Google Colab notebook:

   ```bash
   jupyter notebook
   ```
4. Open `Trader_Behavior_Insights.ipynb` and execute all cells.

---

## 📚 Libraries Used

* **pandas** → data manipulation
* **numpy** → numerical operations
* **matplotlib** & **seaborn** → data visualization

---

## 🔮 Future Work

* Implement **machine learning models** (e.g., logistic regression, XGBoost) to predict trade outcomes based on sentiment and trade features.
* Build **real-time dashboards** (Streamlit/Plotly) to monitor sentiment and trader performance.
* Extend analysis to include **macro events & news sentiment** for deeper insights.

---

## ✨ Conclusion

This project provides a **foundational analysis** of how **market sentiment impacts trader behavior**.

The insights gained here can serve as a stepping stone toward **advanced, sentiment-aware trading systems** in the Web3 space.

---

Would you like me to also **add badges (e.g., Python, Jupyter, MIT License, GitHub stars)** at the top of your README to make it look even more polished and professional for recruiters?
