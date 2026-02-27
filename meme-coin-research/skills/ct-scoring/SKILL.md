---
name: ct-scoring
description: Crypto Twitter (CT) / X narrative strength scoring for a token. Analyzes account age, follower quality, KOL mentions, engagement rates, and narrative memorability to score a token's social momentum from 0-100. Use when asked "what's the CT score", "how's the narrative", "is CT hyped on X token".
---

# CT Score — Social Momentum Intelligence

## Overview

Narrative drives price in meme coins. This skill quantifies it.

## CT Score Components (100 pts total)

### Account Quality (25 pts)
- Main account age: >30 days (5pt) | >90 days (10pt) | >1 year (15pt)
- Follower count: >1K (5pt) | >10K (10pt)
- No follower-buying signs (verified organic: 0 or -10pt)

### Content Quality (25 pts)
- Posts per day: 3-5 = optimal (10pt), <1 or >10 = lower
- Engagement rate: >3% (10pt) | >7% (15pt)
- Original content vs. reposts: mostly original (10pt)
- Meme quality: iconic/original (10pt) | template-based (5pt) | none (0pt)

### KOL & Community (30 pts)
- KOL mentions (>100K followers): 5pt each, max 20pt
- Community posts (not official account): >10 posts (5pt) | >50 (10pt)
- Telegram activity: >100 msgs/day (10pt)

### Narrative Memorability (20 pts)
- One-line pitch clarity (can you explain it in 5 words?): 10pt if yes
- Timing alignment (riding a meta: AI, dog, anime, etc.): 10pt
- Uniqueness: first of its kind in current cycle: bonus 5pt

## CT Score Verdict
- 80-100: 🔥 **BASED** — strong narrative, CT is cooking
- 60-79:  📈 **BUILDING** — potential, needs more amplification
- 40-59:  😐 **MEH** — narrative exists but not sticky yet
- 20-39:  📉 **WEAK** — struggling to get traction
- 0-19:   💀 **DEAD** — no narrative, no community

## Output
```
CT SCORE: [X]/100 — [BASED/BUILDING/MEH/WEAK/DEAD]

Breakdown:
  Account Quality:  [X]/25
  Content Quality:  [X]/25
  KOL & Community:  [X]/30
  Narrative:        [X]/20

Key signal: [one sentence on what's driving or killing the score]
```
