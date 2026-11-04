## Chapter 1: Blockchain 101: Distributed Ledgers, Blocks, and Consensus — Practice Questions

**Q1.** A blockchain network shows a single mining pool controls 55% of total network hashrate. Which attack becomes newly feasible against this Proof of Work chain?

A) 51% double-spend / chain reorganization attack
B) Sybil attack via fake nodes
C) Front-running via mempool manipulation
D) Smart contract reentrancy attack

<details>
<summary>Answer</summary>

**Correct: A**

Controlling a majority of hashpower lets an attacker mine faster than the honest network, allowing them to build a longer private chain and reorganize/rewrite recently confirmed blocks to double-spend.

**Why the others are wrong:**
- Sybil attacks involve creating many fake node identities; PoW mitigates Sybil resistance through hashpower cost, not node count, so this is unrelated to hashrate percentage.
- Front-running/MEV relates to transaction ordering within a block, not to majority hashpower control.
- Reentrancy is a smart contract code vulnerability, unrelated to consensus-layer hashrate concentration.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An auditor wants to verify that block #500,000 has not been altered since it was recorded, without re-downloading the entire chain. Which block-structure property enables this?

A) Each block stores the hash of the previous block, so altering data changes the hash and breaks the link to all subsequent blocks
B) Each node keeps a private copy of every user's password
C) The timestamp field is encrypted with the miner's private key
D) The nonce value is broadcast in real time to all users

<details>
<summary>Answer</summary>

**Correct: A**

Because each header embeds the previous block's hash, any change to historical data changes that block's hash, invalidating every block that follows — this chaining is what makes the ledger tamper-evident.

**Why the others are wrong:**
- Nodes never store user passwords; this has no relation to blockchain data integrity.
- Timestamps are not encrypted with a miner's private key.
- Nonce broadcasting relates to mining the block, not to detecting tampering afterward.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A community adds a rule that tightens validation so that blocks previously considered valid under the old rules are now rejected, but non-upgraded nodes still accept blocks created under the new rules as valid. What type of change is this?

A) Hard fork
B) Soft fork
C) Sybil resistance change
D) Genesis block reset

<details>
<summary>Answer</summary>

**Correct: B**

A soft fork is a backward-compatible rule tightening — old, non-upgraded nodes still recognize new blocks as valid, so no chain split is required.

**Why the others are wrong:**
- A hard fork is a non-backward-compatible change requiring all nodes to upgrade or the chain splits into two.
- Sybil resistance describes how a network prevents fake identity attacks, unrelated to protocol upgrade type.
- A genesis block reset would mean starting a new chain from block zero, not a rule change.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which consensus mechanism selects the block producer based on the amount of cryptocurrency a participant has locked up as collateral, rather than computational work?

A) Proof of Work
B) Proof of Elapsed Time
C) Proof of Burn
D) Proof of Stake

<details>
<summary>Answer</summary>

**Correct: D**

Proof of Stake (used by Ethereum since the Merge) selects validators to propose/attest blocks based on staked collateral rather than computational effort.

**Why the others are wrong:**
- Proof of Work selects the block producer via computational hashpower (Bitcoin's mechanism).
- Proof of Elapsed Time uses a random wait time within a trusted execution environment, used in some permissioned chains, not stake amount.
- Proof of Burn selects based on coins permanently destroyed, not staked/locked collateral.

</details>

---

**Q5.** Which single field within a block header allows nodes to cryptographically link a block to its immediate predecessor?

A) Merkle root
B) Nonce
C) Previous block hash
D) Block reward

<details>
<summary>Answer</summary>

**Correct: C**

The previous block hash field stores the hash of the prior block's header, forming the literal 'chain' in blockchain.

**Why the others are wrong:**
- The Merkle root summarizes the transactions inside the current block, not the link to the prior block.
- The nonce is the value miners adjust to satisfy the PoW difficulty target, unrelated to chaining.
- Block reward is the incentive paid to the miner/validator, not part of the header's linking mechanism.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** On the Bitcoin network, mining difficulty recalculates approximately every how many blocks to keep block time near 10 minutes?

A) 210 blocks
B) 21000 blocks
C) 2016 blocks
D) 100000 blocks

<details>
<summary>Answer</summary>

**Correct: C**

Bitcoin recalculates difficulty every 2016 blocks, roughly every two weeks, targeting an average 10-minute block time.

**Why the others are wrong:**
- 210 blocks is far too short an interval and matches no actual Bitcoin parameter.
- 21000 blocks is roughly 10x too many and doesn't match the real adjustment interval.
- 100000 blocks is far too large, would mean adjustments every ~2 years, not matching protocol design.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** What is the minimum ETH stake required to operate an independent solo validator node on the Ethereum network?

A) 1 ETH
B) 10 ETH
C) 32 ETH
D) 100 ETH

<details>
<summary>Answer</summary>

**Correct: C**

32 ETH is the standard deposit required to activate a solo validator on Ethereum's Proof of Stake consensus layer.

**Why the others are wrong:**
- 1 ETH is far below the protocol's solo validator requirement (though staking pools can accept smaller pooled amounts).
- 10 ETH is still below the required deposit for an independent validator.
- 100 ETH is more than required; the protocol minimum for one validator slot is fixed at 32 ETH.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Why are public blockchains like Bitcoin and Ethereum described as pseudonymous rather than anonymous?

A) Transactions require government ID verification before being broadcast
B) Wallet addresses are not directly tied to real-world identities, but all transaction history is publicly visible and can be linked to identities through analysis or exchange KYC data
C) All transaction data is encrypted and only visible to the sender and receiver
D) Node operators must register their real names with a central authority

<details>
<summary>Answer</summary>

**Correct: B**

Addresses themselves carry no name attached, but every transaction is permanently public, allowing chain analysis firms and exchanges (via KYC) to de-anonymize users over time — hence 'pseudonymous', not anonymous.

**Why the others are wrong:**
- No government ID check occurs at the protocol level for broadcasting transactions on permissionless chains.
- Transaction data on public blockchains is not encrypted — it is openly readable by anyone, which is precisely why linkage/analysis is possible.
- There is no central authority requiring node operator name registration on permissionless networks like Bitcoin or Ethereum.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

