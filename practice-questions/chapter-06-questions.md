## Chapter 6: Following the Flow of Funds: Pseudonymity vs Anonymity — Practice Questions

**Q1.** An investigator finds that a wallet sent funds directly to an address on the OFAC SDN list. Two hops earlier, an unrelated exchange deposit address received funds that eventually reached this same wallet through three intermediate addresses. How should the exchange deposit be classified in the case file?

A) Direct exposure, because the funds ultimately reached a sanctioned address
B) No exposure, because the exchange never interacted with the SDN address itself
C) Indirect exposure, because the sanctioned entity was reached only after multiple intermediate hops
D) Direct exposure, because exchanges are always held to a stricter standard than personal wallets

<details>
<summary>Answer</summary>

**Correct: C**

Direct exposure means an address transacted immediately (one hop) with the risky entity. Indirect exposure means the risky entity was reached through one or more intermediary addresses — exactly the case here.

**Why the others are wrong:**
- Reaching a sanctioned address eventually does not make the exposure direct; hop count determines the classification
- Funds did flow toward the SDN address through the chain, so there is exposure — it's just indirect, not zero
- There is no rule that exchange addresses default to direct exposure; classification depends on hop distance, not entity type

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During a trace, an analyst observes a large UTXO repeatedly split into a small payment output and a larger 'change' output sent to a fresh address, with this pattern repeating across many transactions. Which pattern is this?

A) A CoinJoin mixing round
B) A peeling chain
C) A Lightning Network channel settlement
D) A dusting attack

<details>
<summary>Answer</summary>

**Correct: B**

A peeling chain is the classic pattern where a large balance is 'peeled' off in small increments to destinations, with the remainder moved to a new change address each time — commonly used to obscure the ultimate destination of large sums.

**Why the others are wrong:**
- CoinJoin combines multiple users' inputs/outputs in a single equal-value transaction, not sequential splitting
- Lightning settlements close a payment channel on-chain and don't produce a repeating small/large split pattern
- Dusting sends tiny amounts to many addresses to de-anonymize wallets, not repeated large-to-small splits from one source

</details>

---

**Q3.** A suspect converts BTC to ETH via a DEX aggregator, then bridges the ETH to a different chain, then swaps again for a privacy coin. Which evasion technique best describes this overall behavior?

A) Peeling
B) Address poisoning
C) Sybil clustering
D) Chain-hopping

<details>
<summary>Answer</summary>

**Correct: D**

Chain-hopping refers to moving value across multiple assets and/or blockchains in sequence specifically to break the continuity that single-chain tracing tools rely on.

**Why the others are wrong:**
- Peeling is a single-chain UTXO splitting pattern, not cross-asset/cross-chain movement
- Address poisoning is a scam technique using look-alike addresses, unrelated to laundering flow
- Sybil clustering refers to creating many fake identities/nodes, not moving funds across chains

</details>

---

**Q4.** Which factor makes cross-chain bridges a major challenge point in multi-hop tracing?

A) Funds are pooled into a shared liquidity contract, breaking the 1:1 on-chain link between the deposit and withdrawal transaction
B) Bridges always operate without any smart contracts, making them untraceable by design
C) Bridges are illegal in most jurisdictions and therefore excluded from analysis tools
D) Bridges only support privacy coins, so standard clustering heuristics never apply

<details>
<summary>Answer</summary>

**Correct: A**

Most bridges lock or burn assets on the source chain and mint or release equivalent value from a shared pool on the destination chain, so there is no direct on-chain transaction linking a specific deposit to a specific withdrawal — analysts must rely on timing, amount correlation, and off-chain data.

**Why the others are wrong:**
- Many bridges do use smart contracts; the challenge is pooling, not absence of contracts
- Legality varies by jurisdiction and has no bearing on the technical tracing challenge
- Bridges commonly support many asset types, not only privacy coins

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Why do standard blockchain clustering heuristics generally fail against Monero transactions?

A) Monero transactions are never confirmed on a public ledger
B) Monero uses ring signatures with fixed decoy sets and stealth addresses, obscuring the true sender and receiver
C) Monero has no transaction fees, so no metadata exists to analyze
D) Monero blocks are encrypted and cannot be downloaded by non-miners

<details>
<summary>Answer</summary>

**Correct: B**

Ring signatures (fixed ring size of 16 since the 2022 protocol upgrade) mix the real input among decoys, RingCT hides amounts, and stealth addresses generate a unique one-time address per receipt — defeating common-input-ownership and address-reuse heuristics that work on transparent chains like Bitcoin.

**Why the others are wrong:**
- Monero transactions are recorded on a public blockchain, just with obfuscated data fields
- Monero does have transaction fees; the issue is obfuscation of participants, not absence of fees
- The blockchain is publicly downloadable; it's the transaction contents that are cryptographically obscured, not the blocks themselves

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** For an exam-style case file, which single entry BEST documents a fund flow that passed through a non-custodial bridge and a decentralized exchange before reaching a risky entity four hops later?

A) A one-line note stating 'funds are dirty' with no supporting transaction hashes
B) A hop-by-hop log listing each transaction hash, timestamp, amount, address cluster, and confidence level, ending with the classification of exposure as indirect at four hops
C) Only the final transaction hash that touched the risky entity, omitting earlier hops for brevity
D) A screenshot of the risky entity's public reputation without any on-chain transaction data

<details>
<summary>Answer</summary>

**Correct: B**

Proper documentation requires a reproducible, hop-by-hop chain of evidence — hashes, timestamps, amounts, clustering rationale, and a stated confidence level — culminating in an accurate exposure classification (direct vs indirect) based on actual hop distance.

**Why the others are wrong:**
- Unsupported conclusions without transaction evidence are not admissible or defensible in a case file
- Omitting intermediate hops removes the evidentiary trail needed to justify the exposure classification
- Reputation alone without on-chain linkage does not establish fund flow and is not sufficient documentation

</details>

---

**Q7.** Which statement correctly distinguishes pseudonymity from true anonymity in the context of public blockchains like Bitcoin and Ethereum?

A) Pseudonymous chains hide all transaction data from the public; anonymous chains publish everything
B) There is no meaningful difference — both terms describe the same privacy guarantee
C) Pseudonymous chains expose all transaction data publicly under persistent addresses that can potentially be linked to real identities; true anonymity means transaction details and participants cannot be linked even with full ledger access
D) Pseudonymity applies only to exchanges, while anonymity applies only to individual wallets

<details>
<summary>Answer</summary>

**Correct: C**

Bitcoin/Ethereum are pseudonymous: every transaction is public and tied to an address (a pseudonym) that can be de-anonymized through clustering, KYC leaks, or metadata. True anonymity, as attempted by privacy coins, aims to prevent linkage even with complete access to the ledger.

**Why the others are wrong:**
- It's the reverse: pseudonymous chains are fully transparent, not hidden
- The distinction is heavily tested precisely because the terms are NOT interchangeable
- The distinction is about ledger transparency/linkability, not about the type of entity holding the wallet

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** An analyst applies the multi-hop tracing methodology and finds that confidence in the linkage between the source wallet and the destination entity drops significantly after passing through an unhosted wallet, then a DEX swap, then a bridge, then a privacy coin conversion. What is the CORRECT interpretation for the case file?

A) Confidence should be documented as degraded and explicitly noted per hop, since each mixing/obfuscation point (DEX swap, bridge, privacy coin conversion) introduces uncertainty that compounds across the chain
B) Confidence should remain at 100% since the trace successfully followed every hop
C) The trace should be discarded entirely because any use of a privacy coin invalidates all prior hops
D) Confidence only matters for the final hop; earlier hops require no confidence rating

<details>
<summary>Answer</summary>

**Correct: A**

Multi-hop tracing methodology requires a running confidence assessment — each obfuscation technique (swap, bridge, privacy coin) reduces certainty of linkage, and this compounding uncertainty must be documented at each hop rather than assumed away.

**Why the others are wrong:**
- Successfully following addresses on-chain does not guarantee attribution certainty, especially through mixing points
- Prior hops with strong evidence remain valid even if later hops are weaker; the whole trace isn't invalidated
- Every hop's confidence matters because the overall case strength depends on the weakest links in the chain

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

