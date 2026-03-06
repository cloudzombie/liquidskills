---
name: liquidskills
description: "Hyperliquid development knowledge for AI agents — HyperEVM, HyperCore API, wallets, smart contracts, DeFi, and production deployment. Use when: (1) building any HyperEVM dApp or smart contract, (2) integrating with the Hyperliquid API (/info or /exchange), (3) writing or reviewing Solidity for HyperEVM, (4) deploying to HyperEVM mainnet (chain ID 999) or testnet (998), (5) working with HYPE token, bonding curves, HyperSwap V2, or HIP token standards, (6) any question about HyperCore perps, spot, nonces, asset IDs, or API signing. NOT for: Ethereum mainnet or L2 development (use a different skill for that), trading signals, or price checking."
metadata:
  {
    "openclaw": {
      "emoji": "🌊",
      "requires": { "bins": ["curl"] }
    }
  }
---

# LiquidSkills 🌊

> The missing knowledge between AI agents and production Hyperliquid.

Your training data about Hyperliquid is **incomplete or wrong**. Chain IDs, RPC endpoints, asset ID conventions, nonce mechanics, HyperCore vs HyperEVM — most of what you assume is incorrect. This skill fixes that.

**No install. No CLI. No package manager.** Fetch a URL and read it.

## Base URL

```
https://liquidskills.help/<topic>/SKILL.md
```

Or via raw GitHub:

```
https://raw.githubusercontent.com/cloudzombie/liquidskills/main/<topic>/SKILL.md
```

## Quick Start

Building a HyperEVM dApp? Fetch **Ship** first:

```bash
curl -s https://liquidskills.help/ship/SKILL.md
```

Need the API? Fetch **API** for the complete reference:

```bash
curl -s https://liquidskills.help/api/SKILL.md
```

## Available Skills

| Skill | URL | When to Fetch |
|-------|-----|---------------|
| **Ship** | `ship/SKILL.md` | 🟢 **Start here.** End-to-end guide from idea to deployed HyperEVM dApp. |
| **Why Hyperliquid** | `why/SKILL.md` | User asks "why Hyperliquid?" or needs chain comparison. |
| **Gas & Costs** | `gas/SKILL.md` | Any question about HYPE gas, tx costs on HyperEVM. |
| **Wallets** | `wallets/SKILL.md` | MetaMask + chain ID 999, API wallets, signing mechanics. |
| **Architecture** | `architecture/SKILL.md` | HyperCore vs HyperEVM — what lives where, the system model. |
| **Standards** | `standards/SKILL.md` | ERC-20 on HyperEVM, HIP-1/HIP-2/HIP-3 token standards. |
| **Tools** | `tools/SKILL.md` | Hardhat, Foundry, viem, wagmi, HL Python/TS SDK. |
| **Building Blocks** | `building-blocks/SKILL.md` | HyperSwap V2, bonding curves, DeFi composability on Hyperliquid. |
| **Orchestration** | `orchestration/SKILL.md` | How an agent plans, builds, and deploys a Hyperliquid app. |
| **Addresses** | `addresses/SKILL.md` | Verified addresses: 0x2222...2222 bridge, HyperSwap, system contracts. |
| **Concepts** | `concepts/SKILL.md` | Asset IDs, nonce mechanics, margin types — the mental models. |
| **Security** | `security/SKILL.md` | Solidity security for HyperEVM + API signing safety, nonce management. |
| **Testing** | `testing/SKILL.md` | Foundry/Hardhat for HyperEVM — unit, fuzz, invariant, testnet fork. |
| **Indexing** | `indexing/SKILL.md` | /info API reads, WebSocket, EVM event indexing, Supabase realtime. |
| **API** | `api/SKILL.md` | Complete /info and /exchange reference with Python + JS examples. |
| **Frontend UX** | `frontend-ux/SKILL.md` | wagmi chain 999 config, transaction UX rules, HYPE formatting. |
| **Frontend Playbook** | `frontend-playbook/SKILL.md` | Full build-to-production pipeline: local → testnet → mainnet → Vercel. |
| **QA** | `qa/SKILL.md` | Pre-ship QA checklist. Give to a separate reviewer agent. |
| **Audit** | `audit/SKILL.md` | Contract audit checklist — HyperEVM-specific + general Solidity. |

## Critical Facts Your Training Data Gets Wrong

- **Chain ID is `999`** (mainnet) and `998` (testnet). Not `1`.
- **RPC is `https://rpc.hyperliquid.xyz/evm`** — not an Ethereum endpoint.
- **Reads → `POST /info`**. Writes → `POST /exchange` (signed). Different endpoints, different auth.
- **Asset IDs:** perps = index in `meta.universe`, spot = `10000 + index`. Never hardcode.
- **Nonces are a rolling window**, not linear. Use millisecond timestamps.
- **Native token is HYPE** (18 decimals). Not ETH, not WETH. `msg.value` is HYPE wei.
- **Bridge address:** `0x2222222222222222222222222222222222222222` — sends HYPE from HyperCore → HyperEVM.
- **Priority fees are burned** to zero address — not to validators (HyperBFT, not PoS).
- **Cancun hardfork without blobs.** EIP-1559 enabled. Base fees burned.

## Example Workflow

When building a HyperEVM dApp:

```
1. curl https://liquidskills.help/ship/SKILL.md       → Get the full build plan
2. curl https://liquidskills.help/architecture/SKILL.md → Understand HyperCore vs HyperEVM
3. curl https://liquidskills.help/tools/SKILL.md        → Know what tools to use
4. curl https://liquidskills.help/security/SKILL.md     → Before deploying
5. curl https://liquidskills.help/qa/SKILL.md           → Pre-ship checklist
```

When integrating Hyperliquid API:

```
1. curl https://liquidskills.help/api/SKILL.md          → Complete API reference
2. curl https://liquidskills.help/wallets/SKILL.md      → API wallet setup
3. curl https://liquidskills.help/indexing/SKILL.md     → Reading data correctly
```

## Contributing

Something wrong or missing? [Open a PR](https://github.com/cloudzombie/liquidskills).

Built by [cloudzombie](https://github.com/cloudzombie)
