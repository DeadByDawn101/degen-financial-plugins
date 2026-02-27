---
name: rugcheck
description: Fast rug pull risk assessment for any token. Checks contract flags, liquidity lock status, dev wallet activity, top holder concentration, and social verification. Returns a RISK SCORE and GO/NO-GO verdict. Fires automatically when user says "rug check", "is this safe", "check this token", or provides a CA with no other context.
---

# Rug Check — Risk Assessment

## Overview

30-second rug pull risk assessment. Technical flags only — no speculation.

## Check List

Run every check. Mark: ✅ PASS | 🚨 FAIL | ⚠️ WARN | ❓ UNKNOWN

### Contract Safety
- [ ] Mint authority disabled (can't print new tokens)
- [ ] Freeze authority disabled (can't freeze wallets)
- [ ] Contract verified/open source
- [ ] No proxy patterns / upgradeable contracts
- [ ] Token program: standard SPL vs Token-2022 (note which)

### Liquidity
- [ ] Liquidity locked (if graduated — check Raydium LP burn/lock)
- [ ] Liquidity >$10K
- [ ] Liquidity not 100% owned by single wallet
- [ ] No large LP removals in past 24h

### Distribution
- [ ] Top holder <20% of supply
- [ ] Top 10 holders <50% of supply
- [ ] Dev/team wallet <10% of supply
- [ ] No wallet bought >5% in first block

### Dev Behavior
- [ ] Dev wallet still holds (not sold 100%)
- [ ] Dev wallet history: no previous rugs
- [ ] No stealth launches from same wallet
- [ ] Social accounts predate token launch

### Social Verification
- [ ] Website live and not parked
- [ ] X/Twitter account >30 days old
- [ ] Telegram invite link works
- [ ] No copy-paste whitepaper

## Risk Score

Count failures:
- 0–1 failures: 🟢 LOW RISK — degen away
- 2–3 failures: 🟡 MEDIUM RISK — size down, watch closely
- 4–6 failures: 🔴 HIGH RISK — avoid or micro position only
- 7+ failures: 💀 RUG RISK — do not touch

## Output

```
RUG CHECK — $TICKER
━━━━━━━━━━━━━━━━━━
✅ PASS: [X] checks
🚨 FAIL: [X] checks  
⚠️ WARN: [X] checks
❓ UNKNOWN: [X] checks

RISK: [LOW / MEDIUM / HIGH / RUG]
VERDICT: [one sentence]
```
