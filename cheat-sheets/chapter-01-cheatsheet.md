## Chapter 1 Cheat Sheet — Blockchain 101

### PoW vs PoS
| | Proof of Work (Bitcoin) | Proof of Stake (Ethereum, post-Merge) |
|---|---|---|
| Block producer selection | Miner solves computational puzzle | Validator chosen by staked ETH |
| Resource cost | Energy/hashpower | Capital (staked collateral) |
| Attack threshold | >50% network hashrate | >50% staked value |
| Penalty for misbehavior | Wasted energy/orphaned block | Slashing (loss of stake) |
| Ethereum switch date | Pre-Sept 2022 | Since 'the Merge', Sept 2022 |

### Hard Fork vs Soft Fork
| | Hard Fork | Soft Fork |
|---|---|---|
| Backward compatible? | No | Yes |
| Old node behavior | Rejects new blocks → chain splits | Still accepts new blocks as valid |
| Requires all nodes upgrade? | Yes | No |
| Example | Bitcoin Cash split from Bitcoin | SegWit on Bitcoin |

### Block Header Fields
| Field | Purpose |
|---|---|
| Previous block hash | Links block to prior block (creates the chain) |
| Merkle root | Summarizes all transactions in this block |
| Timestamp | Time block was created |
| Nonce | Value miners adjust to meet PoW difficulty target |
| Difficulty target | Threshold hash must be below to be valid (PoW) |
| Version | Protocol/software version flag |

### Key Numbers
| Fact | Value |
|---|---|
| Bitcoin block time target | ~10 minutes |
| Bitcoin difficulty adjustment | Every 2016 blocks (~2 weeks) |
| Ethereum solo validator stake | 32 ETH |
| Ethereum Merge (PoW→PoS) | September 2022 |
| 51% attack threshold | Majority hashrate (PoW) or majority stake (PoS) |

### Why Tamper-Evident
Each block header stores the hash of the previous block. Change any past data → that block's hash changes → every following block's stored 'previous hash' no longer matches → chain is broken and requires majority consensus to override.

### Pseudonymous ≠ Anonymous
- Address ≠ identity directly, BUT all transactions are public and permanently traceable.
- De-anonymization happens via chain analysis + exchange KYC linking address to real identity.
- Exam trap: choosing 'anonymous' when the correct term is always 'pseudonymous' for public chains.

### Nodes / Miners / Validators
- **Node**: stores ledger copy, validates transactions/blocks, relays data.
- **Miner (PoW)**: competes via hashpower to produce next block.
- **Validator (PoS)**: staked participant selected to propose/attest blocks; subject to slashing.
