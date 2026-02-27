---
name: bundle-strategy
description: Multi-wallet coordinated buy strategy for pump.fun launches. Plans wallet count, SOL allocation, timing spread, and sell strategy to build curve momentum without triggering sniper/rug signals. Use when asked about "bundling", "coordinated buy", "how many wallets", "launch bundle strategy".
---

# Bundle Strategy — Coordinated Launch Intelligence

## Overview

Coordinated buys done right look organic. Done wrong they look like a rug setup.

## Bundle Architecture

### Wallet Count vs. SOL Available

| SOL Budget | Wallets | Per Wallet | Strategy |
|-----------|---------|-----------|----------|
| 0.5 SOL | 5 | 0.1 SOL | Micro-seed — proof of life |
| 1-2 SOL | 6-8 | 0.15-0.25 SOL | Standard launch bundle |
| 3-5 SOL | 10-15 | 0.2-0.35 SOL | Strong launch — fills 5-7% curve |
| 5-10 SOL | 15-20 | 0.25-0.5 SOL | Power launch — significant curve fill |

### Timing Spread (critical for organic appearance)

Do NOT buy all in the same block. Spread as follows:
- Block 1: 1 wallet (dev buy — small, 0.05-0.1 SOL)
- Blocks 2-10: 0 wallets (let organic buyers in)
- Min 2-5: 2-3 wallets buy naturally
- Min 5-15: 3-5 more wallets buy
- Min 15-30: remaining wallets fill in

### Source Diversity

Each wallet should receive SOL from a different source:
- CEX withdrawal (different amounts = less pattern-matched)
- Different timing (not all funded in same block)
- Never all from same parent wallet in single TX

## Buy Size Calculation

For a 85 SOL graduation target:
- 1 SOL bundle fill = ~1.2% of curve
- 3 SOL bundle fill = ~3.5% of curve
- 10 SOL bundle fill = ~12% of curve

Target: bundle covers 5-15% of curve, rest organic.

## Exit Strategy

**Never** dump the bundle all at once. Stagger:
- Take 25% off at 2x from entry price
- Take 25% off at 5x
- Let 50% ride to graduation (or set stop loss at entry)
- Coordinate wallet exits: spread over 24-48h minimum

## Constraints

- This is strategy planning only — not financial advice
- Coordinated trading may be restricted in some jurisdictions — user's responsibility
- Always leave enough organic room for community to drive graduation
