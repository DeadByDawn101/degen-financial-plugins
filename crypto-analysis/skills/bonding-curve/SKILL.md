---
name: bonding-curve
description: Bonding curve analysis for pump.fun tokens. Given a CA, pulls real-time curve state from pump.fun API and calculates graduation progress, SOL needed, price impact of buy sizes, and estimated time to graduation based on current velocity. Fires when user asks about bonding curve, graduation, "how far to grad", "how much SOL to graduate".
---

# Bonding Curve Intelligence

## Overview

pump.fun bonding curves graduate at 85 SOL (virtual reserves). This skill tracks everything about a token's curve journey.

## Data Pull

From `https://client-api-2-74b1891ee9f9.herokuapp.com/coins/{CA}`:
- `virtual_sol_reserves` → current SOL in curve (divide by 1e9)
- `virtual_token_reserves` → tokens remaining
- `real_sol_reserves` → actual SOL deposited
- `complete` → graduated boolean
- `king_of_the_hill_timestamp` → if it hit king status

## Curve Report Structure

```
🎯 BONDING CURVE REPORT — $TICKER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Current:   [X.XXX] SOL / 85 SOL
Progress:  [XX.X%] ████░░░░░░ 
Remaining: [XX.XXX] SOL to graduation
Status:    [ALIVE / GRADUATED / KING OF THE HILL]

📈 VELOCITY ANALYSIS
Current velocity: [X.X] SOL/hour (based on last 6h)
Est. graduation:  [X hours / X days] at current pace
Peak velocity:    [X.X] SOL/hour at [time]

💰 BUY IMPACT CALCULATOR
0.1 SOL buy → [X]% curve fill, [X]% price impact
0.5 SOL buy → [X]% curve fill, [X]% price impact
1.0 SOL buy → [X]% curve fill, [X]% price impact
3.0 SOL buy → [X]% curve fill, [X]% price impact

🏆 GRADUATION INTEL
At graduation: migrates to Raydium with ~$69K liquidity
Graduation SOL: 12 SOL locked as Raydium LP
Post-grad MC target: $[calc based on token price at 85 SOL]
```

## Constraints

- Always show graduation = 85 SOL (hardcoded pump.fun constant)
- Velocity is estimated — mark as estimate if <2h of data
- Price impact calculations use constant product formula: k = x * y
