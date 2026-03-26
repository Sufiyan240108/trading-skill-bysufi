# ATLAS — AI Trading & Analysis System

A Claude skill that turns Claude into a full-stack trading intelligence agent. Analyzes stocks, markets, news, sentiment, fundamentals, and technicals to give you clear, actionable buy/sell/hold decisions with position sizing.

## Modules (18 total)

| # | Module | What it does |
|---|---|---|
| 1 | Deep Stock Analysis | Full fundamental + technical + sentiment breakdown |
| 2 | Quick Verdict | Buy / sell / hold in 60 seconds |
| 3 | Earnings Analysis | Pre or post-earnings deep dive |
| 4 | Competitor Comparison | Pick the winner across N stocks |
| 5 | Market Pulse | Indices, sectors, biggest movers today |
| 6 | News & Sentiment Scan | What the market is talking about |
| 7 | Sector Rotation Analysis | Where is the money moving |
| 8 | Macro Risk Radar | Fed, CPI, geopolitics — what matters now |
| 9 | Portfolio Audit | Review holdings, flag problems |
| 10 | Position Sizing Engine | How much to buy, risk-adjusted |
| 11 | Portfolio Builder | Build a portfolio from scratch |
| 12 | Rebalance Advisor | When and how to rebalance |
| 13 | Stock Screener | Find stocks matching your criteria |
| 14 | Watchlist Builder | Build a tracking list with trigger logic |
| 15 | Momentum Scanner | Breakout and reversal candidates |
| 16 | Trade Setup Builder | Entry, exit, stop-loss for a trade |
| 17 | Risk/Reward Calculator | Is this trade worth taking |
| 18 | Backtest a Thesis | Does this strategy have historical support |

## Installation

1. Download the repo as a ZIP
2. Rename `trading-agent.zip` → `trading-agent.skill`
3. Upload to Claude via the Skills section

Or clone and re-zip the `trading-agent/` folder yourself.

## What's inside

```
trading-agent/
├── SKILL.md                          # Main skill — all 18 modules
└── references/
    ├── technical-analysis.md         # TA indicators, patterns, candlesticks
    ├── fundamental-analysis.md       # Valuation ratios, sector benchmarks
    ├── risk-management.md            # Position sizing, Kelly Criterion, risk rules
    └── market-psychology.md          # Sentiment indicators, market cycles, behavioral traps
```

## Notes

- Pulls live data via web search on every query — not relying on stale training data
- Indian market support built in (NSE/BSE tickers, Nifty/Sensex, ₹ sizing)
- Not licensed financial advice. Verify before trading.
