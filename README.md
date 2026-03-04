# SMC BOS Strategy

A Pine Script backtesting framework for testing a trading model.

## Strategy Concept

The strategy combines multiple structural components used in discretionary SMC trading:

1. Higher Timeframe Bias
   - 4H EMA determines directional bias

2. Trend Alignment
   - 1H EMA confirms trend direction

3. Liquidity Sweep
   - Detects sweep of previous swing highs/lows on HTF

4. Confluence Model
   One of the following must occur:
   - Order Block touch
   - Fair Value Gap fill
   - Equilibrium (midpoint of swing)

5. Entry Confirmation
   - Lower timeframe Break of Structure (BOS)

## Entry Model

Long Entry:
- HTF bias bullish
- Trend aligned
- Liquidity sweep occurs
- At least one confluence zone
- LTF BOS confirmation

Short Entry:
- HTF bias bearish
- Trend aligned
- Liquidity sweep occurs
- At least one confluence zone
- LTF BOS confirmation

## Risk Model

- Stop Loss: Order block edge or last swing
- Take Profit: Risk multiple (default 2R)

## Purpose

This repository is used for:
- PineScript strategy experimentation
- Structural trading research
- Testing variations of SMC models
