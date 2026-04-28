# Trader Performance vs Market Sentiment — 

## Objective
Analyze how Bitcoin market sentiment (Fear/Greed Index) relates to 
trader behavior and performance on Hyperliquid.

---

## Datasets Used
- Bitcoin Fear/Greed Index (daily classification: Fear, Greed, Neutral, Extreme Fear)
- Hyperliquid Historical Trader Data (PnL, trade count, leverage, long/short ratio, etc.)

---

## Methodology
1. Loaded and cleaned both datasets — checked for nulls, duplicates, standardized dates
2. Merged datasets on date to align sentiment with daily trader activity
3. Computed key metrics: daily PnL, win rate, trade count, long/short ratio, average trade size (USD)
4. Grouped all metrics by sentiment category and compared distributions
5. Derived actionable strategy recommendations from observed patterns

---

## Key Findings

### 1. Fear Days Drive More Trading Activity — Not Less
Counterintuitively, traders are MORE active during Fear days.
Daily trade count is higher on Fear days compared to Greed days.
This suggests panic-driven, impulsive behavior rather than strategic positioning.

### 2. PnL is Actually Better on Fear Days
Daily PnL ranks: Fear > Neutral > Greed
Win rate ranks: Neutral > Fear > Greed
This means traders make more money on Fear days despite (or because of)
higher activity — but Neutral days produce the most consistent winners.

### 3. Extreme Fear = Strong Long Bias + Large Position Sizes
During Extreme Fear, the long/short ratio is significantly skewed —
for example, buy-side volume of ~599 vs sell-side of ~399.
Trade size in USD is also largest on Fear days.
On Greed days, buy/sell volumes are far more balanced.

### 4. Greed Days = Impulsive Buy-Sell Cycles
On Greed days, most positions are opened and closed quickly —
traders are not holding positions long enough to capture meaningful upside.
This results in lower PnL despite market optimism.

---

## Strategy Recommendations

**Rule 1: Lean into Fear, but size responsibly**
Fear days historically produce better PnL and larger price moves.
Traders should consider entering positions during Fear — but avoid
over-leveraging just because sentiment is low. The edge is in patience,
not panic-buying.

**Rule 2: On Greed days, reduce trade frequency and hold longer**
The data shows Greed days have lower PnL and impulsive short-term trading.
A simple rule: on Greed days, cut trade count by ~30-40% and set
a minimum hold time before closing a position. Avoid reactive selling.

---

## Files in this Repo
- `market_sentiment_analysis.ipynb` — Full analysis notebook (Colab)
- `README.md` — This file

---
