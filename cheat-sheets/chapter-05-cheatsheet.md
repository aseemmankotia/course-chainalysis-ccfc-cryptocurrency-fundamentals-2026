## Chapter 5 Cheat Sheet: Clustering, Co-Spend, Attribution

### Core Heuristics
| Heuristic | Rule | Breaks When |
|---|---|---|
| Common-input-ownership (co-spend) | All inputs in a tx share one controller (need all private keys to sign) | CoinJoin / mixing transactions |
| One-time change address | Change output is a fresh address never seen on-chain before | Address reuse for change |
| Optimal-change | Non-round-number output = change; round-number output = payment | Wallets that round change deliberately |

### Clustering vs Attribution
| | Clustering | Attribution |
|---|---|---|
| Type | Technical/statistical | Investigative |
| Input | On-chain heuristics | Off-chain data |
| Output | Group of addresses = same controller | Real-world name (exchange, service, person) |
| Confidence | Probabilistic, heuristic-based | Depends on source reliability |

### Off-Chain Attribution Sources
| Source | Description | Legal Process Needed? |
|---|---|---|
| Scraping | Publicly posted deposit/payment addresses (forums, invoices) | No |
| KYC leak | Breached exchange/customer databases | No (but unverified/risky) |
| Voluntary disclosure | Entity self-publishes its own addresses | No |
| Direct engagement | Subpoena / legal request to regulated entity | Yes |

### CoinJoin Red Flags (heuristic breakers)
- High input count AND high output count in one tx
- Many outputs of **identical value**
- Roughly equal number of inputs and outputs
- Action: exclude these transactions from naive co-spend clustering

### Peel Chain Pattern
- Large input repeatedly split: small payment out + remainder to new change address, hop after hop
- Common in: exchange withdrawal fan-out, layering/laundering

### Key Exam Traps
1. **Round-number confusion**: round output = payment, NOT change (reverse of common student assumption)
2. **Clustering ≠ identity**: a large confident cluster is still anonymous until attributed
3. **CoinJoin blind application**: applying co-spend heuristic to a CoinJoin tx merges unrelated entities — a critical false-positive
4. **Source reliability confusion**: KYC leaks and scraped data are investigative leads, NOT evidentiary proof; only direct engagement (legal process) yields verified customer-account attribution

### Tool-Agnostic Visualization Concept (e.g., Reactor-style tools)
- Nodes = clusters/entities
- Edges = transactions between clusters
- Node size/color = balance or risk indicator
- Exam tests the *concept* of graph-based cluster visualization, not specific vendor UI steps
