# Trader Performance vs Market Sentiment
**Primetrade.ai — Data Science/Analytics Internship Assignment**

Analysis of how Bitcoin market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid.

---

## Repository Structure

```
├── TraderPerformancevsSentiment.ipynb   # Main analysis notebook
├── fear_greed_index.csv              # Bitcoin Fear/Greed index dataset
├── historical_data.csv               # Hyperliquid trader data
├── fig1_performance_by_sentiment.png
├── fig2_behavior_by_sentiment.png
├── fig3_leverage_segment.png
├── fig4_frequency_segment.png
├── fig5_consistency_segment.png
├── fig6_long_bias.png
├── fig7_market_activity.png
├── fig8_cumulative_pnl.png
└── README.md
```

---

## Setup

**Requirements:** Python 3.8+

Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

---

## How to Run

### Option 1 — Google Colab (Recommended)
1. Upload `TraderPerformancevsSentiment.ipynb ` to [colab.research.google.com](https://colab.research.google.com)
2. Upload both CSV files (`fear_greed_index.csv`, `historical_data.csv`) to the Colab session storage (`/content/`)
3. Run all cells: `Runtime --> Run All`

### Option 2 — Jupyter Notebook (Local)
1. Clone the repo:
```bash
git clone <your-repo-url>
cd <repo-folder>
```
2. Update the file paths in the second cell of the notebook:
```python
feargreed_path      = 'fear_greed_index.csv'
historicaldata_path = 'historical_data.csv'
```
3. Launch and run:
```bash
jupyter notebook TraderPerformancevsSentiment.ipynb 
```

---

## Notebook Overview

| Section | Description |
|---|---|
| Part A | Data loading, cleaning, timestamp parsing, deduplication, feature engineering |
| Part B | Sentiment vs performance analysis, behavioral segmentation, statistical testing |
| Part C | Strategy recommendations with supporting summary tables |
| Write-Up | Inline markdown summary of methodology, insights, and strategies |
| Part D | Bonus: K-Means behavioral clustering + profitability prediction model |

---

## Key Findings

- Greed days produce more **consistent** profitability (median PnL USD77.7 vs USD36.8); Fear days produce more **extreme** outcomes
- PnL difference is statistically significant (Mann-Whitney U, p = 0.0198)
- Large-position traders earn **3x
-  more** on Fear days; small-position traders outperform on Greed days
- Traders are contrarian **dip-buyers** on Fear days (54% long) despite lower median returns

---

*Note: Analysis covers 32 unique traders. Findings should be validated on a larger dataset before deployment.*
