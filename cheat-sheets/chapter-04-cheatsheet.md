# Chapter 4 Cheat Sheet: Transaction Lifecycle & Wallet Custody

## Transaction Lifecycle (order matters on exam)
| Step | What Happens |
|---|---|
| 1. Build | Select inputs (funds to spend), define outputs (recipient + change) |
| 2. Sign | Private key generates a digital signature authorizing the spend |
| 3. Broadcast | Signed transaction sent to network nodes, enters the mempool |
| 4. Confirm | Miner/validator includes it in a block |
| 5. Finality (relative) | Additional confirmations reduce reorg risk over time |

## Transaction Components
- **Inputs**: references to previously received funds (UTXOs) being spent
- **Outputs**: destination(s) receiving funds, including a change output back to sender
- **Fee**: implicit — sum(inputs) − sum(outputs); goes to the miner/validator

## Fee Mechanics
- Fee = transaction size (vBytes) × fee rate (sat/vByte)
- Fee does **not** scale with the amount of crypto sent
- Stuck low-fee transaction fixes: **RBF** (replace transaction) or **CPFP** (child pays for parent)

## Confirmations & Finality
- More confirmations = lower risk that a **reorg** reverses the transaction
- Bitcoin: 6 confirmations is a common industry standard for treating a transaction as settled for large amounts
- No blockchain transaction has absolute mathematical finality — only probabilistic security

## Hot vs Cold Wallets
| Feature | Hot Wallet | Cold Wallet |
|---|---|---|
| Connectivity | Online / internet-connected | Offline |
| Convenience | High | Low |
| Security risk | Higher (exposed to online attacks) | Lower |
| Typical use | Daily spending, small balances | Long-term storage, bulk holdings |
| Example | Mobile app wallet | Hardware wallet, paper wallet |

## Custodial vs Non-Custodial
| Feature | Custodial | Non-Custodial |
|---|---|---|
| Key control | Third party (e.g., exchange) | User |
| Recovery | Platform-managed (password reset) | User-managed (seed phrase) |
| Risk | Platform insolvency/hack/freeze | User error (lost keys = lost funds) |
| Slogan | "Not your keys, not your coins" | Full self-custody |

## Reading a Block Explorer
- Look up by **txid** (64-char hex string)
- Check: confirmation count, block height, inputs/outputs, fee paid, timestamp
- Independent of wallet UI — trust the chain, not the app

## Common Exam Traps
- Confusing **broadcast** (instant, to mempool) with **confirmation** (requires mining)
- Assuming fee scales with amount sent (it scales with size × fee rate)
- Assuming hot/cold is the same axis as custodial/non-custodial — they are independent (an exchange's custodial wallet uses both hot and cold storage internally)
- Assuming one confirmation equals full finality
