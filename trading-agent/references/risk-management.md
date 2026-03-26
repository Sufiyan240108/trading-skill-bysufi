# Risk Management Reference

## The Core Rules (Non-Negotiable)

1. **Never risk more than 2% of total capital on a single trade** (standard). 1% for conservative. 3% max for aggressive.
2. **Never let a position become >20% of portfolio** (unless very high conviction, very short term)
3. **Always define the stop loss BEFORE entering a trade**
4. **Never average down into a losing position without a clear thesis reason**
5. **Cut losses fast. Let winners run.** The math demands it.

---

## Position Sizing Models

### Fixed Percentage Risk Model (Recommended default)
```
Risk amount = Total Capital × Risk % per trade
Position Size = Risk Amount ÷ (Entry Price - Stop Loss Price)
```

**Example:**
- Capital: ₹5,00,000
- Risk per trade: 2% → Risk amount = ₹10,000
- Entry: ₹500, Stop Loss: ₹475 → Risk per share = ₹25
- Position size = ₹10,000 ÷ ₹25 = 400 shares
- Total position value = 400 × ₹500 = ₹2,00,000 (40% of capital — check concentration)

### Kelly Criterion
```
f* = (p × b - q) / b
f* = fraction of capital to bet
p = probability of winning
b = ratio of win to loss
q = 1 - p = probability of losing
```

**Half-Kelly** is standard — use f*/2 for real trading. Kelly full is theoretically optimal but practically too aggressive and drawdowns are brutal.

**Example:**
- Win rate: 55% (p = 0.55), Win/Loss ratio: 2:1 (b = 2)
- f* = (0.55 × 2 - 0.45) / 2 = (1.10 - 0.45) / 2 = 0.325
- Half-Kelly = 16.25% of capital per trade

### Volatility-Adjusted Sizing (ATR-based)
```
ATR = Average True Range (14-period, daily)
Position Size = (Capital × Risk %) ÷ (ATR × Multiplier)
```
Multiplier = 1.5–2.0 typical. Higher volatility stock → smaller position.

---

## Stop Loss Types

### Hard Stop
Fixed price. Simple. If price hits X, you're out. No questions.
- Best for: discretionary traders, swing trades
- Risk: gap downs can blow through your stop

### Trailing Stop
Moves up with price (for long positions). Locks in profits.
- **ATR-based trail**: Stop = Current Price - (2 × ATR). Adjusts with volatility
- **% trail**: Stop = Current Price × (1 - X%). Simpler but less sophisticated
- Best for: trend-following, positional trades where you want to ride the winner

### Technical Stop
Set below key support level (not just arbitrary %).
- "Stop is $480 because that's below the 200MA and the last major swing low at $483"
- More logical than arbitrary % stops

### Time Stop
If trade doesn't work within X days, exit regardless.
- Useful for: setups that depend on a catalyst. If catalyst passes and stock doesn't move, exit.

---

## Portfolio-Level Risk

### Correlation Risk
Don't think you're diversified if you hold 10 tech stocks. They all go down together.
- True diversification = low correlation across holdings
- Sectors: max 2–3 stocks per sector in a 10-stock portfolio
- Factor exposure: check if portfolio is all "growth" or all "value" — that's factor concentration

### Beta
- Beta > 1 = moves more than the market. High beta portfolio amplifies both gains and losses
- Beta < 1 = defensive, moves less
- In bull markets: prefer high beta. In bear markets: prefer low beta or hedge

### Max Drawdown Budgeting
- Know your maximum acceptable portfolio loss before you start (your "ruin threshold")
- Typical for active traders: 20% max drawdown before going to cash
- If portfolio is down 15%, reduce position sizes. If down 20%, re-evaluate everything.

### Concentration Limits
| Position | Max % of Portfolio |
|---|---|
| Single stock | 20% |
| Single sector | 35% |
| Single country/market | 70% (if focused) |
| Cash floor (always keep) | 10% minimum |

---

## The Math of Losses (Why Risk Management Matters More Than Gains)

| Loss % | Gain needed to recover |
|---|---|
| 10% | 11.1% |
| 20% | 25% |
| 30% | 42.9% |
| 40% | 66.7% |
| 50% | 100% |
| 60% | 150% |

**Implication:** Losing 50% requires a 100% gain just to break even. This is why protecting capital is Priority #1.

---

## Expected Value Framework

For any trade to be worth taking:
```
EV = (Win Rate × Avg Win) - (Loss Rate × Avg Loss) > 0
```

Minimum viable trade:
- **1:2 R/R** at 40% win rate: EV = (0.4 × 2) - (0.6 × 1) = 0.8 - 0.6 = +0.2 ✓
- **1:1 R/R** at 40% win rate: EV = (0.4 × 1) - (0.6 × 1) = -0.2 ✗ (losing trade)
- **1:3 R/R** at 35% win rate: EV = (0.35 × 3) - (0.65 × 1) = 1.05 - 0.65 = +0.4 ✓

**Minimum standard:** Only take trades with at least 1:2 R/R. Even with a 40% win rate, you come out ahead.

---

## Hedging Basics

### Portfolio Hedge
- **Inverse ETFs** (e.g., SH for S&P 500 short) — simple, no derivatives needed
- **Put options on index** — buy puts on Nifty/SPY to protect portfolio
- **Increase cash** — simplest hedge. Selling reduces exposure.

### Individual Stock Hedge
- **Protective put** — buy put on a stock you own. Costs premium, caps downside.
- **Stop loss** — the poor man's hedge. Free but doesn't protect against gaps.

### When to Hedge
- When VIX spikes above 25 (fear elevated)
- Before major macro events (Fed meeting, CPI print, elections)
- When portfolio P&L is at a high and you're nervous about a reversal
- When you can't watch the market for extended periods

---

## Behavioral Risk Traps

| Trap | What It Looks Like | Antidote |
|---|---|---|
| Revenge trading | Lost money, trade bigger to make it back fast | Mandatory 24hr break after a big loss |
| FOMO | Chasing a stock already up 20% | "If I missed it, I missed it. Next setup." |
| Anchoring | "It was $100, now $60, it's cheap" | Price is not value. Analyze afresh. |
| Overconfidence | Big winning streak → sizing up dangerously | Stick to the plan. Streaks end. |
| Loss aversion | Holding losers too long hoping to break even | The stock doesn't know what you paid. Cut it. |
| Confirmation bias | Only reading bullish news on a stock you own | Actively seek the bearish case |
| Averaging down emotionally | "It went down, I'll buy more to lower cost" | Only average into strength or with a clear thesis |
