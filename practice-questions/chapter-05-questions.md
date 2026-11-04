## Chapter 5: Address Clustering, Co-Spend Heuristics, and Entity Attribution — Practice Questions

**Q1.** An analyst observes a transaction with 4 inputs from addresses A, B, C, and D, and 2 outputs to addresses E and F. Applying the common-input-ownership heuristic, which conclusion is BEST supported?

A) Addresses E and F are controlled by the same entity
B) Address A is the change address for this transaction
C) This transaction is a CoinJoin and cannot be clustered
D) Addresses A, B, C, and D are controlled by the same entity

<details>
<summary>Answer</summary>

**Correct: D**

The heuristic states that all inputs in a non-CoinJoin transaction must be signed by the same entity because spending requires knowledge of every input's private key.

**Why the others are wrong:**
- Outputs are payments/change, not inputs — the heuristic says nothing about outputs sharing ownership
- Nothing in the scenario indicates which output is change; that requires a separate change-address heuristic
- No evidence (equal-value outputs, unusual input/output ratio) suggests CoinJoin here

</details>

---

**Q2.** A transaction has 6 inputs and 2 outputs: Output 1 = 0.5000000 BTC, Output 2 = 0.31742891 BTC. Using the optimal-change heuristic, which output is MOST LIKELY the change?

A) Output 1, because round numbers indicate change returning to the sender
B) Neither, since the heuristic cannot be applied without knowing wallet software
C) Output 2, because change amounts are typically irregular leftover values
D) Both, since a transaction can have two change outputs

<details>
<summary>Answer</summary>

**Correct: C**

Round numbers usually represent an intended payment amount, while irregular decimal values typically result from subtracting a fee/payment from the input total — the classic signature of change.

**Why the others are wrong:**
- This reverses the heuristic; round numbers indicate the payment, not the change
- The heuristic is explicitly designed to be applied from on-chain value patterns alone, though it is probabilistic, not certain
- A standard two-output transaction has exactly one payment and one change output, not two change outputs

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An analyst is clustering addresses and encounters a transaction with 40 inputs and 40 outputs, where every output has the identical value of 0.1 BTC. What is the CORRECT next step?

A) Apply the common-input-ownership heuristic normally and merge all 40 input addresses into one cluster
B) Apply the optimal-change heuristic to identify the true change output
C) Treat all 40 outputs as belonging to the same entity as the inputs
D) Flag the transaction as a likely CoinJoin and exclude it from standard clustering assumptions

<details>
<summary>Answer</summary>

**Correct: D**

Equal-value outputs combined with a high input/output count is the textbook signature of a CoinJoin, where multiple independent parties combine funds specifically to break the co-spend assumption.

**Why the others are wrong:**
- This would incorrectly merge unrelated entities into one cluster, a known heuristic failure mode
- There is no single 'change' output in a CoinJoin structure since all outputs are equal-value participant outputs
- CoinJoin outputs belong to many different participants, not the input owners collectively

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A law enforcement agency needs to confirm that a specific cluster belongs to a named exchange and requires records tying the cluster to a verified customer account. Which off-chain attribution source is required?

A) Scraping publicly posted deposit addresses from a forum
B) A leaked KYC database found on a dark web marketplace
C) Voluntary disclosure published by the exchange's blog
D) Direct engagement with the exchange via legal process (e.g., subpoena)

<details>
<summary>Answer</summary>

**Correct: D**

Confirming a specific customer account tied to a cluster with evidentiary reliability requires a formal legal request directly to the regulated entity, not passive or unverified sources.

**Why the others are wrong:**
- Scraped addresses give hints about cluster ownership but are not verified customer-account-level evidence
- Leaked data is often unverified, incomplete, and legally problematic to rely on as sole evidence
- Voluntary disclosure only covers what the entity chooses to publish, not specific customer accounts

</details>

---

**Q5.** Which off-chain attribution source is characterized by an analyst manually collecting deposit addresses that services publish for user payments, without contacting the service directly?

A) Scraping
B) Direct engagement
C) Voluntary disclosure
D) KYC leak

<details>
<summary>Answer</summary>

**Correct: A**

Scraping refers to collecting publicly available address data (forum posts, exchange payment pages, invoices) without requiring cooperation or legal process.

**Why the others are wrong:**
- Direct engagement implies active communication or legal request to the entity
- Voluntary disclosure means the entity proactively shares its own addresses, not the analyst collecting them independently
- A KYC leak is a breach of private customer data, not publicly posted addresses

</details>

---

**Q6.** What is the MINIMUM number of inputs a transaction must have for the common-input-ownership heuristic to provide any clustering signal?

A) 1
B) 5
C) There is no minimum — the heuristic works on any transaction
D) 2

<details>
<summary>Answer</summary>

**Correct: D**

The heuristic links multiple input addresses together as commonly owned; with only 1 input there is nothing to cluster together, so at least 2 inputs are required to produce a link.

**Why the others are wrong:**
- A single-input transaction provides no cross-address linkage, so the heuristic yields no new clustering edge
- 5 is an arbitrary higher number with no special significance to the heuristic's basic requirement
- The heuristic specifically requires multiple inputs to generate a linkage; it has no effect on single-input transactions

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which characteristic of an output address MOST STRONGLY supports the one-time change-address heuristic?

A) The address has been reused in at least 10 prior transactions
B) The address belongs to a known exchange hot wallet
C) The address was newly created and has never appeared on-chain before this transaction
D) The output value is a round number

<details>
<summary>Answer</summary>

**Correct: C**

Wallet software typically generates a fresh, never-before-seen address for change to preserve privacy, making 'first appearance on-chain' a strong signal of a change output.

**Why the others are wrong:**
- Reuse actually weakens the change hypothesis, since change addresses are meant to be single-use
- Known exchange hot wallets are far more likely to be payment destinations than change outputs of a customer's own wallet
- Round-number outputs are more consistent with intended payments, per the optimal-change heuristic, not change

</details>

---

**Q8.** What is the fundamental difference between address clustering and entity attribution?

A) Clustering assigns a real-world name; attribution groups addresses by common control
B) They are the same process with different names used by different vendors
C) Clustering groups addresses believed to share a common controller; attribution assigns a real-world identity to that cluster
D) Clustering only applies to exchanges, while attribution only applies to individual users

<details>
<summary>Answer</summary>

**Correct: C**

Clustering is a purely technical/statistical process (grouping addresses via heuristics), while attribution is the separate investigative step of linking that cluster to a known real-world entity using off-chain data.

**Why the others are wrong:**
- This reverses the definitions of clustering and attribution
- They are distinct steps in the analysis pipeline; a cluster can exist unattributed indefinitely
- Both clustering and attribution can apply to exchanges, services, or individuals — there is no such restriction

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

