## Chapter 4: Building, Signing, Broadcasting a Transaction, and Wallet Custody Models — Practice Questions

**Q1.** An exchange requires 6 confirmations before crediting a customer's Bitcoin deposit into their trading account. Why does the exchange wait for multiple confirmations instead of crediting after the first?

A) Bitcoin transactions are not actually broadcast to the network until the 6th block is mined
B) The network charges a lower fee once 6 confirmations have passed
C) Waiting reduces the risk that a blockchain reorganization reverses the transaction after it appeared confirmed
D) Miners require 6 separate signatures from the sender before the transaction is valid

<details>
<summary>Answer</summary>

**Correct: C**

Deeper confirmations mean more blocks would need to be re-mined for a reorg to reverse the transaction, making it economically and computationally harder to double-spend. Exchanges use this as a practical finality threshold.

**Why the others are wrong:**
- Broadcasting happens immediately after signing, not after blocks are mined — this confuses broadcast with confirmation
- Fees are set at broadcast time based on size and market rate; confirmation count does not change the fee already paid
- Signatures are created once at signing time, not accumulated per confirmation

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A user needs a wallet for daily coffee purchases and quick peer-to-peer payments, and accepts a higher risk of theft in exchange for instant access. Which wallet type best fits this need?

A) Hardware wallet stored offline in a drawer
B) Paper wallet stored in a bank safe deposit box
C) Software hot wallet installed on a mobile phone
D) Air-gapped multisig cold storage vault

<details>
<summary>Answer</summary>

**Correct: C**

A hot wallet keeps keys on an internet-connected device, trading security for convenience — ideal for frequent, low-value transactions.

**Why the others are wrong:**
- A hardware wallet is cold storage — secure but too slow/inconvenient for daily spending
- A paper wallet is cold storage and inaccessible for instant transactions
- An air-gapped multisig vault is designed for maximum security of large holdings, not daily spending

</details>

---

**Q3.** A company keeps 95% of its Bitcoin treasury offline in a hardware wallet that never touches the internet, and 5% in an exchange account for daily operational liquidity. This is best described as which strategy?

A) A fully custodial architecture
B) A single-key non-custodial model with no redundancy
C) A multisig-only architecture with no hot wallet component
D) A hot/cold wallet segregation strategy

<details>
<summary>Answer</summary>

**Correct: D**

Splitting funds between cold storage (bulk, high security) and hot storage (small amount, operational liquidity) is the industry-standard risk-management pattern.

**Why the others are wrong:**
- Custodial refers to who holds the keys (a third party), not the hot/cold split described here
- The scenario explicitly uses two storage types, not a single key with no redundancy
- The scenario includes a hot exchange balance, so it is not multisig-only

</details>

---

**Q4.** The phrase 'Not your keys, not your coins' is a warning about the risk associated with which wallet model?

A) Non-custodial wallet, where the user holds the private keys
B) Hot wallet, regardless of who holds the keys
C) Cold wallet, regardless of who holds the keys
D) Custodial wallet, where a third party holds the private keys

<details>
<summary>Answer</summary>

**Correct: D**

In a custodial wallet (e.g., an exchange account), the platform controls the private keys, meaning the user does not have direct, independent control over their funds.

**Why the others are wrong:**
- Non-custodial wallets give the user the keys — this is the opposite of the risk being warned about
- Hot vs cold describes connectivity/security, not who controls the keys
- Cold wallets can be either custodial or non-custodial; the phrase specifically targets key ownership

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which tool would you use to independently verify that a specific transaction has been confirmed and check its current number of confirmations, without relying on your wallet's interface?

A) Your wallet's local transaction cache
B) A mempool fee estimator API
C) Your hardware wallet's firmware update log
D) A public block explorer

<details>
<summary>Answer</summary>

**Correct: D**

A block explorer queries the blockchain directly, letting you look up a transaction ID and see its status, block height, and confirmation count independently of any single wallet.

**Why the others are wrong:**
- A wallet's local cache reflects what the wallet software has synced, which can be stale or wrong
- A fee estimator only projects future fee rates, it does not confirm transaction status
- Firmware logs relate to device software, not blockchain transaction data

</details>

---

**Q6.** A user needs their Bitcoin transaction to confirm in the next block due to a time-sensitive payment. What should they do when broadcasting the transaction?

A) Increase the amount of BTC being sent
B) Reduce the number of inputs used in the transaction
C) Set a high fee rate (sat/vByte) so miners prioritize including it
D) Wait until network congestion naturally clears before broadcasting

<details>
<summary>Answer</summary>

**Correct: C**

Miners select transactions from the mempool based on fee rate per vByte, so a higher fee rate increases the chance of near-term inclusion.

**Why the others are wrong:**
- The BTC amount sent has no bearing on miner prioritization
- Fewer inputs reduces transaction size (and thus fee cost at a given rate) but does not itself guarantee priority
- Waiting contradicts the stated time-sensitive requirement

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A transaction was broadcast with a very low fee and has sat unconfirmed in the mempool for hours. Which technique lets the sender increase the fee on that same transaction to speed up confirmation?

A) Replace-By-Fee (RBF)
B) Converting the transaction to Proof of Stake
C) Performing a double-spend attack
D) Overriding it with a multisig signature

<details>
<summary>Answer</summary>

**Correct: A**

RBF allows a sender to rebroadcast the same transaction (same inputs) with a higher fee, replacing the original low-fee version in the mempool, provided RBF was signaled at creation.

**Why the others are wrong:**
- Consensus mechanism cannot be changed per-transaction
- Double-spending refers to fraudulently spending the same funds twice, not fee bumping
- Multisig relates to requiring multiple signatures to authorize spending, not fee replacement

</details>

---

**Q8.** What is the correct order of the transaction lifecycle?

A) Sign, Build, Broadcast, Confirm
B) Broadcast, Build, Sign, Confirm
C) Build, Sign, Broadcast, Confirm
D) Build, Broadcast, Sign, Confirm

<details>
<summary>Answer</summary>

**Correct: C**

A transaction must first be constructed (inputs/outputs selected), then signed with the private key to authorize spending, then broadcast to the network mempool, and finally confirmed when included in a block.

**Why the others are wrong:**
- A transaction cannot be signed before it is constructed — there is nothing to sign yet
- Broadcasting an unbuilt transaction is not possible
- An unsigned transaction cannot be validly broadcast; nodes would reject it

</details>

---

