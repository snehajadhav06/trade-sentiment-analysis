# Trader Behavior vs. Bitcoin Market Sentiment

Analysis of the relationship between trader performance (Hyperliquid historical trade data)
and Bitcoin market sentiment (Fear & Greed Index), built as part of a data science assignment.

## Contents
- `trader_sentiment_analysis.ipynb` — full notebook: data cleaning, merging, EDA, sentiment
  vs. performance analysis, and hidden pattern discovery
- `output/` — exported summary tables (PnL by sentiment, win rate by sentiment, trade size
  by sentiment, account-level profiles, correlation matrix)

## Key Findings
- Trader performance follows a U-shaped pattern across sentiment — Extreme Greed and Fear
  both outperform Neutral sentiment, rather than a simple "greed is good" trend
- Average trade size was largest during Fear ($7,816) and smallest during Extreme Greed
  ($3,112) — traders sized up on dips rather than chasing euphoria
- ~66% of accounts were net more profitable on Greed-side days, ~34% on Fear-side days,
  suggesting distinct contrarian vs. momentum trading styles across the population
- Sentiment score alone is a weak linear predictor of daily PnL (correlation ≈ -0.08),
  since the real relationship is category-based (U-shaped) rather than linear

## Data Sources
- Hyperliquid historical trade data (account, coin, size, side, PnL, fees, timestamps)
- Bitcoin Fear & Greed Index (daily sentiment classification)

Raw data files are excluded from this repo (see `.gitignore`) due to file size — the full
analysis and results are available in the notebook and `output/` folder.
