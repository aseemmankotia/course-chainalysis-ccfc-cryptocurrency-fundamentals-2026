## Chapter 2: Bitcoin, Ethereum, Stablecoins, Tokens, and the Crypto Ecosystem — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Coin vs Token — core distinction? | Coin = native asset on its own blockchain (BTC, ETH). Token = issued via smart contract on an existing chain (e.g., ERC-20 on Ethereum). Exam tip: needs its own consensus/chain → coin. |
| 2 | Bitcoin's ledger accounting model? | UTXO (Unspent Transaction Output) — tracks discrete spendable outputs, not account balances. Exam tip: contrast with Ethereum's account-based model. |
| 3 | Ethereum's ledger accounting model? | Account-based — global state tracks a running balance per address. Exam tip: enables smart contracts to hold and manage token balances directly. |
| 4 | ERC-20 token standard defines what? | Standard functions (transfer, balanceOf, approve, allowance) for fungible tokens on Ethereum. Exam tip: balances live in contract storage, separate from the base ETH ledger. |
| 5 | Fiat-collateralized stablecoin — mechanism and example? | Backed 1:1 by fiat reserves held by the issuer, redeemable via the issuer, trust relies on audits/attestations. Example: USDC. Exam tip: peg risk = issuer solvency and reserve transparency. |
| 6 | Crypto-collateralized stablecoin — mechanism and example? | Backed by overcollateralized crypto assets locked in smart contracts, liquidated if collateral value drops. Example: DAI. Exam tip: peg risk = collateral volatility and liquidation cascades. |
| 7 | Algorithmic stablecoin — mechanism and notable failure? | Maintains peg via supply/demand algorithms and a secondary token, with little or no collateral. TerraUSD (UST) de-pegged and collapsed in 2022. Exam tip: highest de-peg risk of the three stablecoin types. |
| 8 | CEX vs DEX — custody difference? | CEX (e.g., Coinbase, Binance) is custodial, holds user keys, requires KYC. DEX (e.g., Uniswap) is non-custodial, users retain keys, typically no KYC. Exam tip: 'not your keys, not your coins' applies to CEX deposits. |
| 9 | Custodian vs mixer — regulatory obligation? | Custodians (exchanges, custodial wallets) must perform KYC/AML and retain identity records. Mixers obscure transaction trails and typically retain no identity data. Exam tip: mixers are a major red flag in investigations. |
| 10 | Why are mixers/tumblers an ecosystem risk point? | They pool and mix funds from many users, breaking the on-chain link between sender and receiver addresses, hindering tracing. Exam tip: presence of a mixer hop signals need for deeper investigation. |
| 11 | DeFi protocols — key ecosystem risk? | Smart contract exploits, no central custodian to freeze/recover funds, and composability risk where protocols stack atop one another and amplify losses. Exam tip: DeFi generally lacks KYC or a recovery mechanism. |
| 12 | Wrapped BTC (WBTC) — what is it? | An ERC-20 token representing BTC 1:1, backed by BTC held by a custodian, allowing Bitcoin value to be used in Ethereum DeFi. Exam tip: it is a custodial-backed token, not a native coin. |
