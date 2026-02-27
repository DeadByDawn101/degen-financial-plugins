# degen-financial-plugins

> Plugins that turn Claude into a degen crypto specialist — bonding curves, wallet forensics, meme coin DD, pump.fun launches, and on-chain portfolio tracking.

Forked from [`anthropics/financial-services-plugins`](https://github.com/anthropics/financial-services-plugins) and degenified. Same architecture, completely different soul.

Built for [Claude Code](https://claude.com/product/claude-code). Works with any Claude API setup.

---

## What This Is

Anthropic built enterprise financial plugins for investment bankers. We built the degen version for on-chain traders, meme coin operators, and anyone who needs Claude to understand crypto-native workflows.

| Anthropic Plugin | Degen Version | What it does |
|---|---|---|
| `financial-analysis` | **`crypto-analysis`** | Token DD, bonding curves, wallet forensics, rug checks |
| `equity-research` | **`meme-coin-research`** | Launch analysis, CT scoring, narrative engineering |
| `investment-banking` | **`pump-launch`** | pump.fun launch playbook, bundle strategy |
| `private-equity` | **`wallet-forensics`** | Whale tracking, sniper detection, fund tracing |
| `wealth-management` | **`defi-portfolio`** | PnL tracking, position management |

---

## Plugins

### `crypto-analysis` — Core (install first)

Wires Claude to on-chain data sources and gives it crypto-native analysis skills.

**MCP Connectors:** DexScreener · Helius · Jupiter · pump.fun · Birdeye · Solscan · Defined

**Skills:**
- `degen-dd` — Full due diligence: snapshot, red flags, whale activity, DEGEN SCORE (0-100)
- `bonding-curve` — Curve progress, graduation velocity, buy impact calculator
- `wallet-forensics` — Full wallet profile, behavior classification, PnL, connected wallets
- `rugcheck` — 20-point rug pull risk checklist, GO/NO-GO verdict

**Commands:**
```
/ape [CA]      — Full degen DD + DEGEN SCORE verdict
/bonding [CA]  — Bonding curve progress + graduation intel
/wallet [addr] — Full wallet forensics report
/rug [CA]      — Fast rug pull risk assessment
```

---

### `meme-coin-research` — Add-on

CT scoring, launch quality analysis, and narrative building.

**Commands:**
```
/ct-score [CA]     — CT/X narrative strength score (0-100)
/launch-dd [CA]    — Early stage launch quality analysis
/narrative [brief] — Build or audit a token's narrative
```

---

### `pump-launch` — Add-on

End-to-end pump.fun launch planning and execution strategy.

**Commands:**
```
/launch [concept]  — Full launch playbook (pre-launch to graduation)
/bundle [SOL]      — Bundle strategy for coordinated launch buys
```

---

### `wallet-forensics` — Add-on

Deep whale investigation and holder mapping.

**Commands:**
```
/whale [CA]        — Top holder map with classification + sell pressure
/sniper [CA]       — Sniper wallet detection for any token
/trace [wallet]    — Fund tracing + connected wallet graph
```

---

### `defi-portfolio` — Add-on

Cross-wallet portfolio tracking and PnL analytics.

**Commands:**
```
/pnl [wallet]      — Full realized + unrealized PnL breakdown
/positions [wallet]— Current open positions with entry/current price
```

---

## Install

```bash
# Add this marketplace
claude plugin marketplace add DeadByDawn101/degen-financial-plugins

# Install core first (required)
claude plugin install crypto-analysis@degen-financial-plugins

# Add any combination of add-ons
claude plugin install meme-coin-research@degen-financial-plugins
claude plugin install pump-launch@degen-financial-plugins
claude plugin install wallet-forensics@degen-financial-plugins
claude plugin install defi-portfolio@degen-financial-plugins
```

---

## Configure API Keys

Add to your environment (`.env` or shell profile):

```bash
HELIUS_API_KEY=your_helius_key      # https://helius.dev — Solana RPC + enhanced APIs
BIRDEYE_API_KEY=your_birdeye_key    # https://birdeye.so — token analytics
SOLSCAN_API_KEY=your_solscan_key    # https://pro.solscan.io — Solana explorer
DEFINED_API_KEY=your_defined_key    # https://defined.fi — multi-chain analytics
```

DexScreener and pump.fun work without API keys.

---

## Architecture

Same file-based structure as the original:

```
plugin-name/
├── .claude-plugin/plugin.json   # Manifest
├── .mcp.json                    # Data connectors (core only)
├── commands/                    # Slash commands
└── skills/                      # Domain knowledge (auto-activates)
```

Skills are markdown. Commands are markdown. No code, no build steps, no infrastructure.

---

## Built By

[RavenX AI](https://github.com/DeadByDawn101) — gothic crypto goddess energy meets enterprise plugin architecture.

Forked from [anthropics/financial-services-plugins](https://github.com/anthropics/financial-services-plugins) — Apache 2.0.

---

## Disclaimer

These plugins assist with on-chain research and crypto workflow automation. They do not provide financial or investment advice. Always do your own research. On-chain activity involves real financial risk.
