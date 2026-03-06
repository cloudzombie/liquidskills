# LIQUIDSKILLS

**The missing knowledge between AI agents and production Hyperliquid.**

An agent can read any skill file and instantly know what it needs to build, deploy, and ship on Hyperliquid — without stale training data, wrong chain IDs, or broken assumptions.

🌐 **[liquidskills.help](https://liquidskills.help)** *(live)*

---

## What Is This?

LIQUIDSKILLS is a set of SKILL.md files — each one focused, dense, and immediately useful. Point an AI agent at any URL and it reads the content, corrects its misconceptions, and builds correctly.

The Hyperliquid skill set for AI agents. Built for builders.

---

## Skills

| Skill | URL | What It Covers |
|---|---|---|
| **Main Router** | `SKILL.md` | Start here — routes you to the right skill |
| **Ship** | `ship/SKILL.md` | End-to-end: idea → deployed on HyperEVM |
| **Why Hyperliquid** | `why/SKILL.md` | HyperBFT, native orderbook, honest tradeoffs |
| **Gas & Costs** | `gas/SKILL.md` | HYPE gas, real costs on HyperEVM |
| **Wallets** | `wallets/SKILL.md` | MetaMask + chain 999, API wallets, signing |
| **Architecture** | `architecture/SKILL.md` | HyperCore vs HyperEVM — the system model |
| **Standards** | `standards/SKILL.md` | ERC-20 on HyperEVM, HIP-1/2/3 token standards |
| **Tools** | `tools/SKILL.md` | Hardhat, Foundry, viem, wagmi, HL SDK |
| **Building Blocks** | `building-blocks/SKILL.md` | HyperSwap V2, bonding curves, DeFi legos |
| **Orchestration** | `orchestration/SKILL.md` | How an agent plans and deploys end-to-end |
| **Addresses** | `addresses/SKILL.md` | Verified addresses: bridge, HyperSwap, system |
| **Concepts** | `concepts/SKILL.md` | Asset IDs, nonces, margins, mental models |
| **Security** | `security/SKILL.md` | Solidity security + API signing safety |
| **Testing** | `testing/SKILL.md` | Foundry/Hardhat for HyperEVM, fuzz, invariants |
| **Indexing** | `indexing/SKILL.md` | `/info` API, WebSocket, EVM event indexing |
| **API** | `api/SKILL.md` | Complete `/info`, `/exchange`, WebSocket reference |
| **Frontend UX** | `frontend-ux/SKILL.md` | wagmi + chain ID 999, transaction UX rules |
| **Frontend Playbook** | `frontend-playbook/SKILL.md` | Full build-to-production pipeline |
| **QA** | `qa/SKILL.md` | Pre-ship QA checklist |
| **Audit** | `audit/SKILL.md` | Contract audit checklist, HyperEVM-specific |

---

## How to Use

### Tell your agent directly
```
"Read https://raw.githubusercontent.com/cloudzombie/liquidskills/main/SKILL.md before you start building"
```

### curl / fetch
```bash
curl -s https://raw.githubusercontent.com/cloudzombie/liquidskills/main/SKILL.md
curl -s https://raw.githubusercontent.com/cloudzombie/liquidskills/main/api/SKILL.md
```

### Load a specific skill
```bash
curl -s https://raw.githubusercontent.com/cloudzombie/liquidskills/main/wallets/SKILL.md
```

---

## Key Facts Every Agent Gets Wrong

- **Chain ID:** HyperEVM mainnet is `999`, testnet is `998`. Not `1`.
- **RPC:** `https://rpc.hyperliquid.xyz/evm` — not an Ethereum endpoint.
- **API:** `POST https://api.hyperliquid.xyz/info` for reads, `POST /exchange` for signed writes.
- **Asset IDs:** Perps = index in `meta.universe`. Spot = `10000 + index`. Never hardcode.
- **Nonces:** Rolling window, not linear. Use millisecond timestamps.
- **Native token:** HYPE (18 decimals) — not ETH, not WETH.
- **Bridge address:** `0x2222222222222222222222222222222222222222` moves HYPE from HyperCore → HyperEVM.
- **Priority fees:** Burned to zero address — not to validators/validators don't exist.
- **Hardfork:** Cancun without blobs. EIP-1559 enabled.

---

## Built With

- No framework. No build step. No dependencies.
- Every skill is a standalone Markdown file — readable by any LLM.
- Served directly from GitHub raw URLs.

---

## Contributing

Something wrong or missing? Open a PR.

Built by [cloudzombie](https://github.com/cloudzombie).  
Built by [cloudzombie](https://github.com/cloudzombie).

MIT License.
