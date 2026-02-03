# Solo — Project Overview

## Tagline
Ask Solana anything. Get answers like you're talking to a friend.

## Problem
Solana explorers (Solscan, SolanaFM) are technical. Normies can't read them. Even crypto natives struggle to extract meaning from raw transaction data.

## Solution
Natural language interface powered by agent swarms that:
1. Parse on-chain data (transactions, NFTs, tokens)
2. Cross-reference multiple sources
3. Generate human-readable narratives
4. Verify facts through consensus

## Example Queries

| Query Type | Example | Output |
|------------|---------|--------|
| Wallet activity | "What's Frank DeGods up to?" | "Frank bought 3 SMBs, voted no on MonkeDAO, his DeGod is up 40%" |
| Token research | "Tell me about [token]" | "Launched 2 weeks ago, 5k holders, dev wallet still holds 40%, trending on Twitter" |
| Trend detection | "What's hot this week?" | "AI agent tokens +37%, DeFi down 12%, 3 new collections minting out" |
| Mystery solving | "Who's the biggest buyer of [NFT]?" | "Wallet 0xabc... bought 23% of supply. Linked to [known whale]." |

## Architecture Overview

```
User Query
    ↓
[Query Parser] → Intent classification
    ↓
[Agent Swarm]
  ├── Research Agents (3-5) → Gather data from sources
  ├── Fact-Check Agents (2-3) → Verify accuracy
  └── Narrative Agent (1) → Write human-readable response
    ↓
[Consensus Layer] → Agree on facts, flag disputes
    ↓
[Response Formatter] → Pretty output with visuals
    ↓
User
```

## Data Sources

| Source | Purpose | API |
|--------|---------|-----|
| Helius | Transaction history, parsed instructions | Helius API |
| Tensor/Magic Eden | NFT data, floor prices, rarity | Tensor API |
| Jupiter | Token prices, swap data | Jupiter API |
| Birdeye | Token analytics, holder distribution | Birdeye API |
| X/Twitter | Social context, sentiment | X API / bird CLI |

## MVP Scope (10 Days)

### Week 1: Core
- [ ] Query parsing (simple intent classification)
- [ ] 2 agent types: Research + Narrative
- [ ] Helius integration for wallet/transaction data
- [ ] Basic web interface (chat UI)
- [ ] 3 query types: wallet, token, collection

### Week 2: Polish
- [ ] Add Fact-Check agents
- [ ] Consensus mechanism
- [ ] Shareable response cards
- [ ] 2 more query types: trends, comparisons
- [ ] Demo video

## Viral Mechanics

1. **Shareable Cards** — Beautiful summaries for Twitter
2. **Mystery Wallets** — "Guess who this whale is" challenges
3. **Trend Calls** — Early narrative detection receipts
4. **Personality Profiles** — "Your wallet DNA" shareables

## Success Metrics

| Metric | Target |
|--------|--------|
| Query accuracy | >90% factual accuracy |
| Response time | <5 seconds |
| User retention | 3+ queries per session |
| Social shares | 100+ in first week |

## Differentiation

- **ChatGPT + Solana:** Generic, no real-time data
- **Solscan:** Technical, no narrative
- **Solo:** Real-time + human-readable + verified facts

---

*Full product spec in progress with Kenji*
