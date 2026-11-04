# Answer Key — Practice Test 1

**Q1. Correct: A**

The scenario describes Proof of Stake, where validators lock up (stake) cryptocurrency instead of expending computational power; the well-known trade-off is that entities with more capital can accumulate more validation power, raising centralization/wealth-concentration concerns.

---

**Q2. Correct: A**

Stablecoins (e.g., USDC, USDT) are specifically designed to maintain a stable value pegged to a fiat currency like the US dollar, making them suitable for payments without volatility exposure.

---

**Q3. Correct: A**

Bitcoin's protocol recalculates mining difficulty every 2016 blocks (roughly every two weeks) by comparing actual time elapsed to the target of 10 minutes per block, adjusting difficulty up or down to keep block time constant as hash power changes.

---

**Q4. Correct: D**

Ethereum's core differentiator is its Turing-complete Ethereum Virtual Machine (EVM), which allows arbitrary smart contract logic and decentralized applications, whereas Bitcoin's scripting language is deliberately restricted to simple transaction conditions.

---

**Q5. Correct: A**

The scenario describes a mixer (or tumbler), a service designed specifically to obscure the on-chain trail by pooling funds from many sources and redistributing them, making it difficult for analysts to link the original source to the final destination.

---

**Q6. Correct: D**

DeFi protocols use smart contracts to offer financial services such as lending and borrowing without a centralized intermediary taking custody of user funds, matching the scenario exactly.

---

**Q7. Correct: A**

Proof of Stake (PoS) requires validators to stake (lock up) native tokens as collateral; dishonest validators can have their stake 'slashed.' Ethereum transitioned from PoW to PoS in 'The Merge' in September 2022.

---

**Q8. Correct: C**

Mixers (also called tumblers) are services designed to obscure the on-chain trail between the source and destination of funds by pooling deposits from many users and redistributing withdrawals in a way that breaks direct address-to-address linkage — a key obfuscation typology covered in the CCFC ecosystem domain.

---

**Q9. Correct: D**

Bitcoin uses secp256k1 elliptic curve multiplication to derive the public key from the private key (one-way, computationally infeasible to reverse). The address is then created by hashing the public key (SHA-256 followed by RIPEMD-160), which is also one-way, so an address cannot be used to recover the public key or private key.

---

**Q10. Correct: D**

Bitcoin uses the UTXO (Unspent Transaction Output) model, where there is no persistent balance field — an address's spendable balance must be calculated by summing all UTXOs that reference that address and have not yet been spent.

---

**Q11. Correct: C**

Because Bitcoin's UTXO model requires spending an entire unspent output, wallets typically send the leftover amount (input minus payment minus fee) back to an address the sender controls. The output tied to prior activity linked to the sender, rather than the unfamiliar recipient address, is the change — this is a core clustering heuristic used in blockchain analysis.

---

**Q12. Correct: B**

The private key generates a digital signature (ECDSA) over the transaction data. The broadcast transaction includes this signature along with the corresponding public key, allowing any node to verify authenticity by checking the signature against the public key without ever seeing the private key.

---

**Q13. Correct: C**

Cold storage keeps private keys entirely offline, so a remote attacker who compromises the exchange's internet-facing systems can only access the smaller hot wallet balance, not the majority of funds held in cold storage — this is the fundamental security rationale behind the hot/cold split.

---

**Q14. Correct: B**

Combining many small UTXOs into a single output is a common wallet-management technique called UTXO consolidation, used to reduce future transaction fees. Six confirmations is a widely used industry threshold (roughly one hour of block production) considered highly resistant to blockchain reorganization, meaning the transaction is effectively finalized.

---

**Q15. Correct: A**

UTXOs must be spent in full; any input not sent to the recipient is returned as 'change' to a change address (often a new address), minus the miner fee.

---

**Q16. Correct: A**

The multi-input (co-spend) heuristic assumes that if multiple addresses are used as inputs in a single transaction, the entity signing the transaction must control the private keys for all of them, so they are clustered together as one entity.

---

**Q17. Correct: D**

Pseudonymity means activity is tied to a persistent identifier (the address) rather than a directly visible identity, but that identifier can be de-anonymized through clustering, exchange KYC data, IP correlation, or other off-chain evidence — unlike true anonymity where no such linkage is possible.

---

**Q18. Correct: C**

A peel chain is a common obfuscation and fund-movement pattern where a large balance moves through many hops, each time 'peeling' off a small amount (often to cash out or pay a service) while the bulk continues on, making the flow harder to follow manually.

---

**Q19. Correct: B**

Analysts use signals such as address reuse patterns, round-number payment amounts, output address type consistency with the input, and use of a fresh unused address to infer which output is change returning to the sender versus the actual payment.

---

**Q20. Correct: A**

Attribution requires linking on-chain clusters to real-world entities, which is done using off-chain intelligence — known service addresses, law enforcement data, open-source intelligence, and direct reporting from exchanges/services — not purely on-chain statistics.

---

**Q21. Correct: B**

CoinJoin protocols intentionally combine inputs from many unrelated users into one transaction so that the multi-input heuristic's core assumption — that all inputs belong to one entity — no longer holds, deliberately undermining clustering accuracy.

---

**Q22. Correct: B**

CoinJoin transactions are specifically constructed to defeat the common-input-ownership heuristic by combining inputs from multiple unrelated parties into one transaction with equal-value outputs. Analysts must recognize these patterns and exclude them from automatic clustering to avoid falsely attributing unrelated users to the same entity.

---

**Q23. Correct: A**

Pseudonymity means addresses are not inherently tied to a name, but they are permanent, public, and reusable identifiers recorded on an immutable ledger. Once real-world attribution data (from an exchange KYC record, a public post, a subpoena, or other off-chain source) links even one address to an identity, clustering heuristics can extend that attribution across the entire linked cluster's full transaction history.

---

**Q24. Correct: D**

FinCEN's Travel Rule (extending the 1996 Funds Transfer Rule/Recordkeeping Rule to convertible virtual currency) sets the U.S. threshold at $3,000. A $2,500 transfer falls below this threshold, so the strict transmittal obligation under U.S. regulation is not triggered, though many VASPs voluntarily collect this data at lower amounts.

---

**Q25. Correct: D**

OFAC sanctions compliance requires U.S. persons and VASPs to block (freeze) property in which a sanctioned person has an interest and to report the blocked transaction to OFAC, rather than allowing it to proceed.

---

**Q26. Correct: D**

KYT (Know Your Transaction) is the ongoing, transaction-level monitoring function that screens wallet addresses and on-chain activity in real time for exposure to illicit or high-risk sources, complementing customer-level KYC checks.

---

**Q27. Correct: A**

Risk-based AML programs use exposure thresholds from KYT tools to trigger escalation. Material exposure to high-risk typologies like darknet markets typically triggers EDD, deeper investigation of the customer and source of funds, and consideration of a Suspicious Activity Report (SAR) filing, rather than an arbitrary high percentage cutoff.

---

**Q28. Correct: D**

CDD is the standard process of verifying customer identity and assessing baseline risk for all customers. EDD applies additional measures — such as source-of-funds verification, senior management approval, and more frequent monitoring — for customers or transactions identified as higher risk (e.g., PEPs, high-risk jurisdictions, or high on-chain risk exposure).

---

**Q29. Correct: C**

Under a risk-based Travel Rule compliance program, a receiving VASP is expected to treat missing required originator/beneficiary information as a red flag warranting additional scrutiny, and may reject, delay, or request the missing information before completing the transaction, rather than processing it as usual.

---

**Q30. Correct: A**

FATF Recommendation 16 guidance for virtual assets sets the Travel Rule threshold at USD/EUR 1,000, requiring originating and beneficiary VASPs to obtain and transmit required originator and beneficiary information.

---

**Q31. Correct: B**

KYT tools continuously monitor blockchain transactions in real time, screening for exposure to illicit actors, sanctioned addresses, and other risk indicators, enabling VASPs to flag or escalate suspicious activity for AML compliance.

---

**Q32. Correct: B**

Pig butchering (sha zhu pan) specifically involves long-term relationship building — often via dating or social apps — followed by introduction to a fraudulent investment platform that shows fake returns to encourage larger deposits before blocking withdrawals.

---

**Q33. Correct: B**

A rug pull is characterized by developers abruptly removing liquidity or otherwise abandoning a project shortly after launch, causing the token's value to crash and leaving investors with worthless holdings.

---

**Q34. Correct: B**

The core distinction is timing and mechanism: Ponzi schemes sustain payouts to earlier participants using new investor capital over time, while rug pulls involve a sudden, often one-time, draining of project funds or liquidity shortly after launch.

---

**Q35. Correct: B**

Double extortion ransomware combines file encryption with data exfiltration and a threat of public leak, demanding payment for both decryption and non-disclosure — a well-documented ransomware evolution tracked in typology analysis.

---

**Q36. Correct: C**

Moving stolen funds across multiple blockchains and through swaps/mixers before consolidation is a textbook example of layering, specifically executed through chain-hopping — a common technique for obscuring the origin of stolen or hacked funds.

---

**Q37. Correct: B**

Using nested accounts and intermediary wallets to disguise the true origin of funds tied to a sanctioned jurisdiction or entity, in order to circumvent sanctions restrictions, is the defining pattern of sanctions evasion.

---

**Q38. Correct: C**

Pig butchering scams involve long-term social engineering (often via dating/messaging apps) to build trust before directing victims to fraudulent investment platforms, matching the multi-week cultivation and 'guaranteed returns' pattern described.

---

**Q39. Correct: C**

Chain-hopping refers to moving funds across multiple different blockchains (often via bridges or swap services) specifically to break the transaction trail on any single chain, which matches the cross-chain bridge movement described with no mixer involved.

---

**Q40. Correct: A**

Moving the full ransom payment immediately to a known high-risk service without splitting or layering the funds is a direct, unobfuscated cash-out attempt, which is easier for blockchain analysis tools to trace back to the ransomware wallet and the receiving service's other illicit exposure.

---

**Q41. Correct: D**

Formal reporting through a SAR/STR with a fully documented transaction trail and, where appropriate, VASP notification is the standard compliance response to confirmed illicit-fund exposure, preserving evidence and supporting law enforcement action.

---

**Q42. Correct: C**

Direct exposure to a high-risk entity must be assessed on its own merits (dollar value, entity type, recency) regardless of the percentage share of total activity — small percentages of large volumes can still represent significant illicit value.

---

**Q43. Correct: D**

Direct exposure measures first-hop (immediate counterparty) contact with a flagged entity, while indirect exposure captures exposure that passes through intermediary hops, both of which inform an address's overall risk profile.

---

**Q44. Correct: C**

Clustering heuristics attribute related addresses to a single real-world entity, which prevents underestimating an entity's total activity and exposure during an investigation or risk assessment.

---

**Q45. Correct: C**

Case files must contain objective, reproducible evidence — a documented transaction trail with attribution and risk indicators — so the findings can withstand scrutiny and support further legal action.

---

