# 📊 Trader Performance vs Market Sentiment
### Primetrade.ai — Data Science Intern Assignment

---

## Objective
Analyze how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid. Uncover patterns that can inform smarter trading strategies.

---

## Datasets
| File | Description |
|---|---|
| `fear_greed_index.csv` | Daily Bitcoin sentiment score + label (2018–2024) |
| `historical_data.csv` | 211,224 trades by 32 traders on Hyperliquid (full year 2024) |

---

## Setup & How to Run

### Option 1 — Google Colab (Recommended)
1. Open [colab.research.google.com](https://colab.research.google.com)
2. Upload `Bitcoin_Sentiment_Trader_Analysis_v2.ipynb`
3. Upload both CSV files when prompted (see Cell 2 for upload instructions)
4. Click **Runtime → Run All**

### Option 2 — Local Jupyter
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Bitcoin_Sentiment_Trader_Analysis_v2.ipynb
```
Place both CSV files in the same folder as the notebook.

---

## Notebook Structure

| Section | Content |
|---|---|
| Part A | Data loading, documentation, cleaning, merging, key metrics |
| Part B1 | PnL, win rate & drawdown by sentiment |
| Part B2 | Trader behavior — frequency, long/short ratio, position size |
| Part B3 | Trader segmentation (3 segments) |
| Part B4 | 3 key insights with supporting charts |
| Part C | Segment-specific strategy recommendations |
| Bonus | Random Forest model + KMeans behavioral clustering |

---

## Key Findings

1. **BUY during Fear = 6x better returns** than buying during Extreme Greed ($63.93 vs $10.50 avg PnL)
2. **Infrequent traders earn 8x more per Greed-day trade** than frequent traders — selectivity beats volume
3. **Losing traders lose most during Greed** (-$202 avg) — following the crowd is costly
4. **Win rate never exceeds 50%** in any sentiment — success is asymmetric (big wins, many losses)
5. **Q1 and December are peak profit months** — August is the only net-negative month

---

## Strategy Recommendations

**Strategy 1 — "Buy Fear, Exit Greed"**
- Consistent Winners: scale up position size during Fear, take profits in Extreme Greed
- Losing Traders: avoid trading during Greed phases entirely

**Strategy 2 — "Selective > Frequent"**
- Frequent traders: reduce activity during Neutral and Greed; concentrate in Fear
- Infrequent traders: maintain selectivity; exploit Greed phases where their edge is 8x larger

---

## Output Charts
All charts saved as PNG files alongside the notebook:
- `B1_pnl_winrate_drawdown.png`
- `B2_behavior_sentiment.png`
- `B3_segmentation.png`
- `Insight1_buy_sell_pnl.png`
- `Insight2_monthly_pnl.png`
- `Insight3_winner_sentiment.png`
- `Bonus_model.png`
- `Bonus_clustering.png`
