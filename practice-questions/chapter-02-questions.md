## Chapter 2: Bitcoin, Ethereum, Stablecoins, Tokens, and the Crypto Ecosystem — Practice Questions

**Q1.** During an investigation, an address received BTC via a mixing service, then forwarded funds to a platform where the funds were later cashed out to a bank account. Which entity is best positioned to provide identity information tying the wallet to a real person?

A) The mixer operator
B) The centralized exchange (CEX) used for cash-out
C) A decentralized exchange (DEX)
D) A public blockchain explorer

<details>
<summary>Answer</summary>

**Correct: B**

CEXs are custodial and legally required to perform KYC/AML, so they hold identity records tied to wallet addresses.

**Why the others are wrong:**
- Mixers are designed to sever the link between sender and receiver and typically retain no identity data.
- DEXs are non-custodial and generally require no identity verification.
- Explorers only expose public on-chain data, never off-chain identity.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A company issues a token claiming 1:1 backing by USD held in audited bank accounts, with monthly reserve attestations published. What type of stablecoin is this?

A) Fiat-collateralized
B) Crypto-collateralized
C) Algorithmic
D) Native coin

<details>
<summary>Answer</summary>

**Correct: A**

Backing by off-chain fiat reserves with attestations is the defining feature of fiat-collateralized stablecoins like USDC/USDT.

**Why the others are wrong:**
- Crypto-collateralized stablecoins (e.g., DAI) are backed by on-chain crypto assets, not bank-held fiat.
- Algorithmic stablecoins use supply/demand mechanisms with little or no collateral.
- 'Native coin' is not a stablecoin classification.

</details>

---

**Q3.** A suspect swaps BTC for wrapped BTC (WBTC) on Ethereum, then trades it on a DEX without completing any identity verification. What characteristic of the DEX enabled this?

A) DEX platforms are non-custodial and generally do not require identity verification
B) DEX platforms require custodial accounts like a bank
C) DEX platforms block all anonymous transactions
D) DEX platforms only accept fiat currency

<details>
<summary>Answer</summary>

**Correct: A**

DEXs let users trade directly from self-custodied wallets via smart contracts, so no KYC gate exists.

**Why the others are wrong:**
- DEXs are non-custodial by design — they never hold user keys.
- DEXs are permissionless; they do not block anonymous trading.
- DEXs trade crypto assets/tokens, not fiat.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which entity holds users' private keys on their behalf and is typically subject to KYC/AML obligations comparable to a bank?

A) A custodian
B) A decentralized exchange (DEX)
C) A mixer
D) A smart contract

<details>
<summary>Answer</summary>

**Correct: A**

Custodians (e.g., exchanges, custodial wallet providers) hold private keys and are regulated similarly to financial institutions.

**Why the others are wrong:**
- DEXs are non-custodial and hold no user keys.
- Mixers exist to obscure identity, not comply with KYC/AML.
- Smart contracts are code, not regulated legal entities.

</details>

---

**Q5.** A user wants to trade tokens while retaining full control of their private keys at all times. Which platform type should they use?

A) Decentralized exchange (DEX)
B) Centralized exchange (CEX)
C) Custodial wallet service
D) Traditional bank

<details>
<summary>Answer</summary>

**Correct: A**

DEXs execute trades via smart contracts directly against the user's self-hosted wallet, so keys never leave user control.

**Why the others are wrong:**
- CEXs take custody of assets/keys once deposited.
- Custodial wallets, by definition, hold keys for the user.
- Banks do not operate as crypto trading venues.

</details>

---

**Q6.** On Ethereum, what mechanism distinguishes an ERC-20 token balance from native ETH held in a wallet?

A) ERC-20 balances are recorded in smart contract storage (e.g., a balance mapping), while ETH balances are tracked in the base protocol account state
B) ERC-20 tokens use the UTXO model like Bitcoin
C) ERC-20 tokens require a completely separate blockchain
D) ERC-20 tokens never incur gas fees

<details>
<summary>Answer</summary>

**Correct: A**

ERC-20 tokens are implemented as smart contracts that maintain their own internal ledger of balances, separate from the protocol-level ETH account balance.

**Why the others are wrong:**
- Ethereum uses an account-based model, not UTXO, for both ETH and tokens.
- ERC-20 tokens live on Ethereum itself; they do not need a separate chain.
- Token transfers still consume gas paid in ETH.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Bitcoin's ledger tracks discrete spendable outputs rather than account balances. What is this model called?

A) Account-based model
B) Smart contract state model
C) Merkle proof model
D) UTXO (Unspent Transaction Output) model

<details>
<summary>Answer</summary>

**Correct: D**

Bitcoin uses the UTXO model, where each transaction consumes prior outputs and creates new ones; wallet 'balance' is the sum of unspent outputs.

**Why the others are wrong:**
- Account-based tracking is Ethereum's model, not Bitcoin's.
- Smart contract state applies to platforms like Ethereum, not Bitcoin's base layer.
- Merkle proofs are a data structure used for verification, not a ledger accounting model.

</details>

---

**Q8.** What is the fundamental distinction between a 'coin' and a 'token' in the crypto ecosystem?

A) Coins are always worth more in market value than tokens
B) Tokens can only represent stablecoins
C) Coins are unregulated while tokens are always regulated securities
D) A coin operates on its own native blockchain, while a token is issued on top of an existing blockchain via smart contracts

<details>
<summary>Answer</summary>

**Correct: D**

Coins like BTC and ETH have their own native chain and consensus mechanism; tokens like ERC-20 assets are created and managed by smart contracts on an existing chain.

**Why the others are wrong:**
- Market value has nothing to do with the coin/token classification.
- Tokens represent many asset types beyond stablecoins (utility, governance, NFTs, etc.).
- Regulatory status varies case-by-case and is not defined by the coin/token label.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

