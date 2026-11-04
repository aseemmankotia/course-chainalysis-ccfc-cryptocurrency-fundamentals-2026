# Ch.6 Cheat Sheet: Pseudonymity vs Anonymity & Fund Flow Tracing

## Exposure Classification
| Type | Definition |
|---|---|
| Direct exposure | Wallet transacts in exactly 1 hop with a risky entity |
| Indirect exposure | Risky entity reached through ≥2 hops via intermediaries |

**Rule:** Classification = hop count, NOT entity type or transaction size.

## Pseudonymity vs True Anonymity
| Property | Pseudonymous (BTC/ETH) | Anonymous (Monero) |
|---|---|---|
| Ledger visibility | Fully public | Public ledger, obscured contents |
| Address linkability | Possible via clustering/KYC leaks | Prevented by design |
| Amount visibility | Public | Hidden (RingCT) |
| Sender/receiver visibility | Public address | Ring-signature mixed / stealth address |

## Obfuscation Patterns
| Pattern | Mechanism | Signal |
|---|---|---|
| Peeling chain | Large UTXO repeatedly split: small spend + large change to new address | Repeating split pattern over many txns from one source |
| Layering | Funds routed through many intermediary wallets/services in stages | Increasing hop count with no clear business purpose |
| Chain-hopping | Asset/chain conversions in sequence (swap → bridge → swap) | Loss of continuity between chains |
| CoinJoin | Multiple users combine inputs/outputs in one equal-value tx | Many equal-value outputs, ambiguous ownership |

## Why Privacy Coins Resist Standard Heuristics (Monero)
- Ring signatures: fixed ring size of **16** (1 real + 15 decoys) since 2022 upgrade
- RingCT: hides transaction amounts
- Stealth addresses: unique one-time address per receipt
- Result: Common Input Ownership Heuristic (CIOH) and address-reuse clustering fail

## Cross-Chain Bridges = Tracing Break Point
- Most bridges lock/burn on source chain, mint/release from **shared pooled contract** on destination chain
- No 1:1 on-chain transaction link between deposit and withdrawal
- Tracing relies on: timing correlation, amount correlation, off-chain data (KYC, IP logs)

## Multi-Hop Tracing Methodology — Steps
1. Identify source address and initial cluster
2. Trace each hop: hash, timestamp, amount, receiving cluster
3. Note every obfuscation point (mixer, DEX, bridge, privacy coin) — each **degrades confidence**
4. Assign a confidence level per hop (confidence compounds/decreases across hops)
5. Classify final exposure as direct (1 hop) or indirect (multi-hop)
6. Document conclusion with full hop-by-hop evidentiary trail — never omit hops for brevity

## Common Exam Traps
- Confusing pseudonymous with anonymous (they are NOT the same)
- Marking multi-hop exposure as "direct" because funds *eventually* reached a risky entity
- Assuming privacy coin use invalidates the entire prior trace (it degrades confidence, doesn't erase evidence)
- Skipping intermediate hop documentation in a case file for "simplicity"
