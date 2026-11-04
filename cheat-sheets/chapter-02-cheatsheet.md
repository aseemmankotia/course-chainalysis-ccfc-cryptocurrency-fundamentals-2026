## Chapter 2 Cheat Sheet: Bitcoin, Ethereum, Stablecoins, Tokens & the Ecosystem

### Coin vs Token
| | Coin | Token |
|---|---|---|
| Chain | Own native blockchain | Issued on existing chain via smart contract |
| Examples | BTC, ETH | ERC-20 (USDC, WBTC, UNI) |
| Ledger location | Base protocol state | Contract storage (balance mapping) |

### Ledger Models
| Chain | Model | Notes |
|---|---|---|
| Bitcoin | UTXO | Tracks unspent outputs, not balances |
| Ethereum | Account-based | Global state tracks per-address balance; enables smart contracts |

### Stablecoin Types — How the Peg Is Maintained
| Type | Backing | Example | Peg Risk |
|---|---|---|---|
| Fiat-collateralized | Off-chain fiat reserves + attestations | USDC, USDT | Issuer solvency/reserve transparency |
| Crypto-collateralized | Overcollateralized on-chain crypto | DAI | Collateral volatility, liquidation cascades |
| Algorithmic | Supply/demand algorithm, little/no collateral | TerraUSD (UST, failed 2022) | Highest de-peg risk — no hard collateral |

### CEX vs DEX
| | CEX | DEX |
|---|---|---|
| Custody | Custodial (holds keys) | Non-custodial (user holds keys) |
| KYC | Required | Typically none |
| Examples | Coinbase, Binance | Uniswap |
| Investigation value | Can subpoena identity records | Only on-chain address data available |

### Custodians vs Mixers — Ecosystem Risk Roles
| Entity | Function | Regulatory posture | Investigative value |
|---|---|---|---|
| Custodian | Holds keys/assets for users | KYC/AML required, bank-like | High — identity records exist |
| DeFi protocol | Smart-contract-based lending/trading/swaps | Often unregulated, no custodian | Low identity value; exploit/composability risk |
| Mixer/tumbler | Pools/obscures transaction trails | Designed to defeat tracing | Very low — breaks address linkage; major red flag |

### Exam Notes
- ERC-20 balance ≠ ETH balance: tokens are tracked inside contract state, ETH is tracked in protocol account state.
- WBTC = token representation of BTC, custodian-backed — used to bring BTC value into Ethereum DeFi.
- Presence of a mixer hop in a transaction trail = escalate investigation; identity data will not come from the mixer itself.
- Algorithmic stablecoins carry the highest structural de-peg risk of the three types — exam scenarios often reference a de-peg event.
- DEX and DeFi protocols generally have no central party to freeze funds or provide KYC — contrast sharply with CEX/custodian obligations.
