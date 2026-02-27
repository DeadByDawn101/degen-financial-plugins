---
name: wallet-forensics
description: Deep on-chain investigation of any Solana or EVM wallet. Given a wallet address, builds a complete profile: SOL/token balance, transaction history, PnL across all tokens, connected wallets, sniper behavior, and risk classification. Use when user asks to "look up a wallet", "check a whale", "is this a sniper", "who is this wallet", "trace these funds".
---

# Wallet Forensics

## Overview

On-chain intelligence for any wallet. Trace funds, classify behavior, identify connected wallets, calculate all-time PnL.

## Data Sources

- **Helius**: Full TX history, token transfers, NFT activity
- **Solscan**: Account overview, token holdings, recent TXs
- **DexScreener**: Match wallet TXs to known pairs
- **Birdeye**: Portfolio value, PnL by token

## Forensics Report Structure

### 1. WALLET OVERVIEW
```
Address: [wallet] (shortened: [first6]...[last4])
Balance: [X.XXX] SOL ($[USD])
Token Holdings: [count] tokens | $[total_value]
First TX: [date] | Last TX: [date]
Total TXs: [count]
Wallet Age: [X days/months]
```

### 2. BEHAVIOR CLASSIFICATION
Classify wallet as one or more:
- 🎯 **SNIPER** — buys within first 3 blocks of launch
- 🐋 **WHALE** — holds >1% of any token supply
- 🔄 **FLIPPER** — avg hold time <30 minutes
- 💎 **HOLDER** — avg hold time >7 days
- 🤖 **BOT** — >100 TXs/day, consistent timing patterns
- 👻 **FRESH** — wallet <7 days old
- 🏭 **DEPLOYER** — has deployed tokens/programs

### 3. PnL BREAKDOWN
Top 10 token trades by absolute P&L:
```
$TICKER | Bought: $X | Sold: $X | P&L: +/-$X ([+/-X%])
```
All-time realized P&L: $[total]
Unrealized P&L: $[total]
Win rate: [X]% ([wins]/[total trades])

### 4. CONNECTED WALLETS
Wallets that sent/received SOL to/from this wallet:
- List top 5 by interaction frequency
- Flag if any are known rugs, exchanges, mixers

### 5. NOTABLE ACTIVITY
- Largest single trade
- Fastest flip (buy→sell time)
- Current top holdings by value
- Any suspicious patterns (circular TXs, wash trading indicators)

### 6. RISK CLASSIFICATION
**LOW RISK** — long history, no rug association, normal patterns
**MEDIUM RISK** — some flags, investigate further
**HIGH RISK** — sniper wallet, rug-associated, wash trading patterns

## Constraints

- Shorten all addresses to [first6]...[last4] in output
- Note if Helius API key not set — some data will be missing
- Never doxx — report on on-chain behavior only, no speculation about identity
