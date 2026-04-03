# Flamingo — Pay-Per-Signal Bitcoin Intelligence Agent

> *An autonomous AI agent that hunts verified market signals, sells them via x402 micropayments, and earns BTC rewards on mainnet.*

---

## Overview

Flamingo is a fully autonomous Bitcoin and DeFi news intelligence agent built on the [AIBTC](https://aibtc.com) network. It runs perpetually on Stacks mainnet, sourcing, verifying, and monetizing high-quality market signals — with zero human intervention required between cycles.

Each signal Flamingo files is backed by on-chain data, academic research, or verified market activity. Each signal sold earns BTC. Each approved signal earns a reward from the aibtc.news Publisher.

---

## What It Does

| Layer | Capability |
|---|---|
| **Sourcing** | Pulls arxiv papers (LLMs, AI infrastructure, agent research) and live Stacks/Bitcoin market data via Tenero |
| **Verification** | Cross-checks signals using the `aibtc-news-fact-checker` skill before filing |
| **Publishing** | Files verified signals to [aibtc.news](https://aibtc.news) as correspondent |
| **Monetization** | Sells intelligence reports via x402 micropayment endpoints — pay-per-access, no subscription |
| **Earning** | Receives $25 sBTC per signal included in the daily brief; earns leaderboard points for verified corrections |
| **Memory** | Accumulates sourcing patterns, contact history, and learned market heuristics across cycles |

---

## Architecture

```
┌─────────────────────────────────────────────────────┐
│                   Autonomous Loop                    │
│                                                      │
│  Read STATE.md → Execute Phases → Write STATE.md     │
│       ↓                                              │
│  [Heartbeat] [Inbox] [Research] [Signal] [Sleep]     │
└─────────────────────────────────────────────────────┘
         ↓                    ↓                ↓
    AIBTC Inbox          arxiv-research      Tenero
    (agent comms)        (paper digests)   (market data)
         ↓                    ↓                ↓
    x402 Endpoints       aibtc.news        On-chain Txns
    (sell signals)       (file signals)    (mainnet wallet)
```

**Cycle duration:** 5 minutes
**Self-improvement:** Every 10th cycle, Flamingo edits its own loop instructions based on observed patterns
**Identity:** Registered on `identity-registry-v2` — verifiable on-chain agent identity

---

## Skills Used

- [`arxiv-research`](https://aibtc.com) — Fetches and scores arXiv papers on AI and agent infrastructure
- [`tenero`](https://aibtc.com) — Live Stacks market analytics: token data, whale trades, trending pools, wallet activity
- [`aibtc-news-correspondent`](https://aibtc.com) — Claims beats, files signals, earns sBTC rewards
- [`aibtc-news-fact-checker`](https://aibtc.com) — Verifies and corrects signals for leaderboard points
- [`x402`](https://aibtc.com) — Scaffolds pay-per-access endpoints for selling signal reports

---

## Wallet & Identity

| Field | Value |
|---|---|
| **Network** | Stacks Mainnet |
| **STX Address** | `SPH5V9GG3J76V55HWK1TQ1EFXKJ6M67KD7SYQ880` |
| **BTC (SegWit)** | `bc1qhqp40885hnq9dyuztt40l7p5gl7lts8lzahhqr` |
| **Identity Contract** | `SP1NMR7MY0TJ1QA7WQBZ6504KC79PZNTRQH4YGFJD.identity-registry-v2` |
| **Agent Profile** | `https://aibtc.com/api/agents/SPH5V9GG3J76V55HWK1TQ1EFXKJ6M67KD7SYQ880` |

---

## Signal Quality Standard

Flamingo does not file noise. Every signal must meet:

1. **On-chain or academic source** — not secondhand social media
2. **Verified before broadcast** — fact-checker pass or data confirmation
3. **Actionable** — tells a reader something they can use, not just something that happened

> *One insight filed well beats three filed carelessly.*

---

## OWS Hackathon

**Track:** Autonomous Agents / DeFi Intelligence
**Built with:** Claude Code · AIBTC MCP · Stacks Mainnet · x402 Protocol
**Status:** Live on mainnet — wallet funded, identity registered, loop operational

---

*Flamingo stands still while everything moves around it. Then it strikes.*
