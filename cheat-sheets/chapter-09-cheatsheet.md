## Chapter 9 Cheat Sheet: Scams, Ransomware, Darknet Markets

### Typology Fund-Flow Comparison
| Typology | Trigger Pattern | Fund Flow Signature | Duration |
|---|---|---|---|
| Rug pull | DEX token pump | Deployer/LP holder drains liquidity pool in one event | Single sudden event |
| Pig butchering | Romance/investment chat grooming | Many small victim deposits → consolidation → stablecoin → OTC/exchange off-ramp | Weeks to months (long con) |
| Ponzi / HYIP | 'Guaranteed high returns' pitch | New deposits directly fund 'returns' to earlier investors; no external revenue | Recurring cycle until collapse |
| Ransomware | Ransom demand address published | Ransom payment → chain-hopping through intermediaries → exchange/mixer cash-out | Single payment, multi-hop cash-out |
| Darknet exit scam | Vendor/market trust built over time | Sudden mass outflow of escrowed funds to new addresses + site goes dark | Single terminal event |

### Darknet Market Mechanics
| Mechanism | Purpose | Exam Trap |
|---|---|---|
| Multisig escrow (2-of-3) | Holds buyer funds until order completion; needs 2 of {buyer, vendor, market} keys | Confused with single-custody escrow (market alone controls release — higher scam risk) |
| Vendor bond | Refundable collateral vendor posts before selling; forfeited for violations | Confused with escrow — bond is vendor-level trust, escrow is per-transaction |
| Finalize Early (FE) | Buyer allows fund release to vendor before confirming receipt | Exploited by 'trusted' vendors to solicit FE from multiple buyers then vanish |
| Exit scam | Operator/vendor drains held funds and disappears | Look for one large outflow + site downtime, not steady payout pattern |

### Ransomware Payment Flow
1. Ransom demand address published to victim.
2. Victim pays (often BTC or Monero) to demand address.
3. Funds moved through **chain-hopping** — multiple unrelated intermediary wallets/chains.
4. Funds converge at exchange, mixer, or OTC desk for cash-out.
5. **Double extortion**: adds data-leak threat, raising demand and urgency.

### On-Chain Indicators Analysts Look For
- **Funnel pattern**: many small inbound → one large outbound (pig butchering, Ponzi).
- **Single drain event**: liquidity pool emptied right after price spike (rug pull).
- **Mass terminal outflow + platform downtime**: exit scam.
- **Multi-hop, cross-chain movement**: ransomware cash-out obfuscation.

### Victim Reports
Victim-reported cases ground-truth on-chain heuristics to a confirmed scam type — critical for validating typology models before applying them to unreported wallet clusters. Reports supplement, never replace, clustering analysis.
