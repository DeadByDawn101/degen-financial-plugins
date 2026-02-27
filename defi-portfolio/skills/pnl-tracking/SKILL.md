---
name: pnl-tracking
description: Calculate realized and unrealized PnL across all token positions for a wallet or set of wallets. Covers Solana SPL tokens, Raydium LP positions, and pump.fun positions. Use when asked "what's my PnL", "how much have I made", "show my gains/losses", "portfolio performance".
---

# PnL Tracker — Portfolio Performance

## Overview

Real numbers. No feelings. Full wallet PnL across all positions.

## PnL Report Structure

### PORTFOLIO OVERVIEW
```
Wallet: [address shortened]
Total Invested (all time): $[X]
Total Realized PnL: +/-$[X] ([+/-X%])
Total Unrealized PnL: +/-$[X]
Current Portfolio Value: $[X]

Win Rate: [X]% ([X] wins / [X] trades)
Best Trade: +$[X] on $[TICKER]
Worst Trade: -$[X] on $[TICKER]
```

### CURRENT OPEN POSITIONS
```
$TICKER | Amount | Avg Entry | Current | Unreal P&L | % Portfolio
```

### CLOSED POSITIONS (last 30 days)
```
$TICKER | Bought | Sold | P&L | Hold Time
```

### PERFORMANCE BY CATEGORY
- pump.fun plays: [X] trades | avg P&L: [+/-X%]
- Raydium/graduated: [X] trades | avg P&L: [+/-X%]
- Airdrop farming: [X] trades | avg P&L: [+/-X%]

## Constraints

- All historical prices estimated from on-chain TXs — may not reflect exact execution price
- LP position value includes impermanent loss calculation
- Note if Birdeye/Helius API key missing — historical data may be incomplete
