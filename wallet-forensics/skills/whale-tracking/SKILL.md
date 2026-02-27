---
name: whale-tracking
description: Track and analyze large wallet holders in a token. Given a CA, identifies top wallets by holdings, classifies each as whale/sniper/bot/dev, shows their entry prices, current P&L, and likelihood of selling. Use when asked "who are the whales", "top holders", "will they dump", "who holds X token".
---

# Whale Tracker

## Overview

Know who holds before you buy. This skill maps the top holder landscape.

## Whale Report Structure

### TOP 20 HOLDERS MAP
```
Rank | Address      | Holdings  | % Supply | Est. Entry | Unreal P&L | Type
1    | 4drR...KPBT  | 50M       | 5.0%     | $0.000001  | +$4,200    | 🐋 WHALE
2    | 9Y4K...chJ   | 35M       | 3.5%     | $0.000003  | +$1,100    | 🤖 BOT
...
```

### HOLDER CLASSIFICATION
For each significant holder:
- 🐋 **WHALE** — large position, likely strategic
- 🤖 **BOT** — automated patterns, sniper signature
- 👨‍💻 **DEV** — linked to deployer wallet
- 💎 **DIAMOND HANDS** — hasn't moved in >7 days
- 🔄 **FLIPPER** — history of quick sells
- 👻 **FRESH WALLET** — new wallet, unknown intent

### CONCENTRATION RISK
```
Top 1 wallet:  [X]% of supply — [LOW/MEDIUM/HIGH] risk
Top 5 wallets: [X]% of supply
Top 10 wallets: [X]% of supply
Exchanges held: [X]% (estimate based on known addresses)
```

### SELL PRESSURE ESTIMATE
Based on entry prices vs. current price:
- Wallets in profit (potential sellers): [X]% of supply
- Wallets underwater (likely holding): [X]% of supply
- Average unrealized gain of top 10: [X]%

### VERDICT
**LOW SELL RISK** — holders mostly in modest profit, distributed
**MEDIUM SELL RISK** — some large profit whales, watch closely
**HIGH SELL RISK** — top holders sitting on huge gains, dump risk real
