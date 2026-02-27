---
name: degen-dd
description: Rapid degen due diligence on any Solana or EVM token. Given a contract address (CA), pulls live data from DexScreener, pump.fun, Helius, and Birdeye to produce a complete degen DD report. Covers: price, market cap, volume, liquidity, holder distribution, top wallets, dev wallet behavior, team token allocation, contract flags, social signals, and a DEGEN SCORE (0–100). Fires automatically when user provides a CA or asks "rug check", "is this safe", "what's the DD on X", "should I ape".
---

# Degen DD — Rapid Token Analysis

## Overview

Full degen due diligence in under 60 seconds. No Bloomberg terminal. No IR decks. Just raw on-chain data and a verdict.

## Data Sources (pull in this order)

1. **DexScreener** — price, MC, 24h volume, liquidity, age, pair address
2. **pump.fun** (Solana) — bonding curve %, king of the hill status, graduated/not
3. **Helius/Solscan** — top 20 holders, dev wallet TXs, creator wallet history
4. **Birdeye** — price history, volume spikes, holder count trend

## DD Report Structure

### 1. TOKEN SNAPSHOT
```
Name: [name] ($TICKER)
CA: [contract_address]
Chain: [Solana / ETH / Base]
Age: [X hours/days]
Price: $[price] | MC: $[market_cap]
Liquidity: $[liquidity] | 24h Vol: $[volume]
Holders: [count] | Transactions: [count]
Bonding: [X/85 SOL] ([%]%) ← pump.fun only
```

### 2. RED FLAGS CHECK
Run through each flag — mark ✅ CLEAR or 🚨 FLAG:
- [ ] Dev wallet sold >20% of supply
- [ ] Top 10 wallets hold >50% of supply
- [ ] Liquidity locked? (if graduated)
- [ ] Contract verified / mintable / freezable
- [ ] Volume is fake (buy/sell ratio >80/20)
- [ ] Age <1 hour with no organic volume
- [ ] Social links dead or freshly created
- [ ] Creator wallet launched >3 rugs previously

### 3. WHALE ACTIVITY
- Top 5 holders: address (shortened), % held, unrealized P&L
- Dev wallet: last TX, balance, previous launches
- Sniper wallets: count within first 3 blocks, % they hold

### 4. SOCIAL & NARRATIVE
- X/Twitter: account age, follower count, post frequency
- Telegram: member count, message rate
- Narrative strength: [STRONG / MODERATE / WEAK / NONE]

### 5. DEGEN SCORE

Score out of 100 — weighted:
- On-chain safety: 40pts (holder distribution, liquidity, dev behavior)
- Momentum: 30pts (volume trend, new holders/hour, bonding %)
- Narrative: 20pts (social strength, meme quality, timing)
- Upside: 10pts (MC vs. comparable tokens at similar stage)

**VERDICT: APE 🟢 / WATCH 🟡 / AVOID 🔴**

## Output Format

Always end with a one-line verdict:
> "Degen score: [X]/100 — [APE/WATCH/AVOID]. [One sentence reason.]"

## Constraints

- Never recommend specific dollar amounts
- Flag when data is unavailable (don't hallucinate metrics)
- Note if Birdeye/Helius API keys not configured — state which data is missing
