# Answer Key — Practice Test 2

**Q1. Correct: A**

Because PoS validators don't burn external resources like PoW miners, an attacker who acquires old private keys can theoretically build an alternate 'costless' chain from genesis. PoS clients mitigate this with weak subjectivity checkpoints — new nodes trust a recent, socially-agreed block hash rather than re-deriving history purely from chain rules, unlike PoW where the longest valid chain is objectively verifiable.

---

**Q2. Correct: A**

DAI is generated when users lock crypto collateral (e.g., ETH, WBTC) into MakerDAO Vaults in excess of the DAI minted, making it an overcollateralized, crypto-backed stablecoin governed by smart contracts rather than a central issuer.

---

**Q3. Correct: D**

EIP-1559 introduced a base fee that is algorithmically adjusted up or down depending on whether the prior block was more or less than 50% full, and this base fee amount is burned rather than paid to validators, which can make ETH deflationary during high-demand periods.

---

**Q4. Correct: D**

In a constant-product AMM (x*y=k), arbitrageurs buy the underpriced asset (ETH, post price rise) from the pool until pool price matches the market, leaving the pool holding relatively more USDC and less ETH than before. When the LP withdraws, the value of their share is typically lower than if they had simply held the original token amounts — this gap is impermanent loss.

---

**Q5. Correct: B**

ERC-721 is the standard for non-fungible tokens (NFTs), where each token has a unique tokenId and metadata making it non-interchangeable, whereas ERC-20 defines fungible tokens where each unit is identical and interchangeable (e.g., USDC, UNI).

---

**Q6. Correct: C**

CoinJoin-style mixers intentionally combine inputs from multiple unrelated users into a single transaction with equal-value outputs, breaking the common-input-ownership heuristic that blockchain analysis tools rely on to cluster addresses belonging to the same entity — this is the defining goal of mixing services.

---

**Q7. Correct: C**

PoS secures the network by requiring validators to stake capital that can be destroyed (slashed) if they act maliciously or go offline, creating a direct financial disincentive. PoW instead secures the network through the real-world cost of acquiring and running hash power, making attacks expensive in hardware and energy rather than staked capital.

---

**Q8. Correct: C**

When issued on Ethereum, USDT is implemented as an ERC-20 token — a smart contract that tracks balances and transfers using Ethereum's existing consensus and settlement layer, rather than operating its own independent blockchain.

---

**Q9. Correct: C**

UTXOs are indivisible — the entire UTXO must be consumed as an input, and any leftover value not sent to the recipient must be returned as a new 'change' output, typically to a fresh address controlled by the sender.

---

**Q10. Correct: B**

The account-based model tracks a running nonce per account and requires transactions to be processed in strict sequential order; a transaction with a nonce higher than the next expected value sits pending until the gap is filled.

---

**Q11. Correct: D**

Offline, air-gapped cold storage with multisignature approval directly matches the requirement for infrequent, multi-party-reviewed withdrawals and minimizes exposure to remote compromise, which is the standard approach for the bulk of exchange reserves.

---

**Q12. Correct: D**

This correctly states the core structural difference: UTXO chains consume/create discrete unspent outputs per transaction, while account chains maintain a running balance per address updated sequentially via nonces.

---

**Q13. Correct: B**

With two inputs totaling 1.2 BTC and two outputs summing to 1.1999 BTC (fee = 0.0001 BTC), one output is almost certainly a change output; 3 confirmations means the transaction has already been included in a block and two additional blocks have been mined on top of it.

---

**Q14. Correct: B**

A watch-only wallet imports only public keys or addresses, allowing full visibility into balances and incoming transactions without ever holding the private key needed to spend funds — exactly matching the monitor-only requirement.

---

**Q15. Correct: D**

In the UTXO model, an input UTXO must be spent in its entirety — you cannot partially spend a UTXO. Any amount not sent to the recipient or paid as a fee must be returned to the sender as a new 'change' output, usually generated at a fresh change address to preserve privacy and avoid address reuse.

---

**Q16. Correct: C**

The common-input-ownership (co-spend) heuristic assumes all inputs to a transaction are controlled by a single entity. CoinJoin transactions are specifically designed to violate this assumption by combining inputs from multiple independent participants, so applying the heuristic here produces false clustering and must be recognized and excluded.

---

**Q17. Correct: B**

A peeling chain is a well-known typology where funds are moved through a long sequence of transactions, peeling off a small amount at each hop while the bulk of value continues to a new address, often used to obscure the flow of illicit funds while preserving most of the balance.

---

**Q18. Correct: C**

The change address heuristic identifies the output most likely representing change returned to the spender, using signals such as address format mismatch with other outputs, or an amount that isn't a round number, allowing analysts to link the change address back to the sender's cluster.

---

**Q19. Correct: D**

Attribution requires linking a purely on-chain cluster to a real-world identity, which is achieved by correlating clustering results with off-chain intelligence such as law enforcement data, subpoenaed exchange records, public statements, forum posts, or leaked data — on-chain analysis alone cannot establish identity.

---

**Q20. Correct: B**

The co-spend heuristic clusters addresses only when they appear together as inputs in the same transaction. Customer deposit addresses receive funds individually and are swept separately (often later, in batches with other deposit addresses, revealing the exchange cluster differently), so they are not directly co-spent with each other and the heuristic alone does not merge every customer's deposit address into one cluster.

---

**Q21. Correct: A**

Pseudonymity means identities are masked by persistent identifiers (addresses) rather than plaintext names, but those identifiers can be de-anonymized over time through clustering heuristics and off-chain intelligence — unlike true anonymity, where no such linkage is ever possible.

---

**Q22. Correct: B**

CoinJoin protocols are specifically designed to combine inputs from multiple unrelated users into one transaction, which directly violates the common-input-ownership heuristic's assumption that co-spent inputs share a single controller. Analysts must recognize CoinJoin patterns and adjust confidence in clustering results accordingly.

---

**Q23. Correct: C**

Most public blockchains (like Bitcoin and Ethereum) are pseudonymous, not anonymous: every transaction is permanently and publicly recorded under an address, and that address can potentially be attributed to a real person or entity through off-chain data (exchange KYC, subpoenas, metadata leaks, clustering). True anonymity would mean no such attribution path exists at all, which is not the case for most public chains.

---

**Q24. Correct: D**

FATF Recommendation 16 (the 'Travel Rule') sets the threshold at USD/EUR 1,000 — transfers above this amount require VASPs to obtain, hold, and transmit required originator and beneficiary information to the counterparty VASP.

---

**Q25. Correct: D**

The 'sunrise issue' describes the compliance gap created because countries adopt and enforce FATF Travel Rule requirements at different times, meaning a compliant VASP may still transact with a counterparty VASP that has no legal obligation (or capability) to send/receive required data.

---

**Q26. Correct: B**

Indirect exposure refers to funds that trace back to a high-risk entity (like a darknet market) through one or more intermediary addresses/hops, as opposed to funds received directly from the risky entity's known wallet.

---

**Q27. Correct: A**

Politically Exposed Person (PEP) status combined with funds sourced from a high-risk jurisdiction are classic risk factors that FATF and AML frameworks identify as triggering mandatory Enhanced Due Diligence, including deeper source-of-funds verification and ongoing enhanced monitoring.

---

**Q28. Correct: C**

Once a wallet address is designated on the OFAC SDN List, U.S. persons and VASPs are legally required to block/freeze any assets involving that address and file a blocked property report with OFAC, regardless of transaction size or counterparty location.

---

**Q29. Correct: A**

FATF's VASP definition centers on entities that conduct exchange, transfer, safekeeping/administration of virtual assets, or participate in financial services related to an issuer's offer/sale, as a business on behalf of another person. A developer who releases non-custodial, open-source software with no ongoing control over user funds or business relationship does not meet this definition.

---

**Q30. Correct: A**

FATF Recommendation 16 sets the virtual asset Travel Rule threshold at USD/EUR 1,000. Above this amount, the originating VASP must collect and transmit required originator and beneficiary data (name, account/wallet identifier, and physical address or other identifying number) to the beneficiary VASP before or simultaneously with the transfer.

---

**Q31. Correct: A**

OFAC's blocking requirement attaches to property and interests in property connected to an SDN, not merely to direct counterparties. Once a US person (including a VASP) identifies blockable funds traceable to a designated address, it must immediately freeze those assets and file a report with OFAC, typically within 10 business days, regardless of the dollar amount involved.

---

**Q32. Correct: D**

The scenario matches the defining features of pig butchering: prolonged relationship-building ('fattening the pig'), a fraudulent investment platform showing fake returns, and funds funneled from many victims into shared collection wallets before cash-out.

---

**Q33. Correct: B**

Chain-hopping refers to moving value across multiple blockchains or asset types (here BTC to XMR and back to BTC) to break the on-chain trail, exploiting the difficulty of tracing through a privacy coin and cross-chain conversions.

---

**Q34. Correct: A**

A nested exchange is a smaller business operating on top of, or inside, a larger exchange's omnibus wallet infrastructure, often with weaker KYC controls, letting customers transact without directly onboarding with the parent exchange — a common darknet market vendor cash-out route.

---

**Q35. Correct: A**

A peel chain is a sequence of transactions in which a small amount is 'peeled off' at each hop while the bulk of funds continues moving forward through many wallets — a classic technique used to complicate tracing before reaching a cash-out point such as a mixer.

---

**Q36. Correct: D**

Terrorism-financing campaigns frequently rely on public solicitation across social media and messaging apps, collecting many small, low-value donations from a broad donor base that are consolidated on-chain before cash-out — a pattern distinct from a single sanctioned transfer or a DeFi exit scam.

---

**Q37. Correct: A**

Address poisoning involves an attacker sending a small or zero-value transaction from a lookalike address (matching the first and last characters of a legitimate one) into a victim's transaction history, hoping the victim later copies the wrong address and sends funds directly to the attacker.

---

**Q38. Correct: B**

Pig butchering is defined by the long-term relationship-building ('fattening') phase before the victim is moved onto a fraudulent trading platform and manipulated into depositing escalating amounts before being blocked from withdrawing.

---

**Q39. Correct: D**

Chain hopping specifically refers to converting funds across multiple different blockchains/assets via swap services or bridges to obscure the trail, which is exactly what's described.

---

**Q40. Correct: A**

This multi-hop, cross-chain, high-volume laundering flow through bridges and nested exchanges matches documented patterns used by state-sponsored actors (such as DPRK-linked groups) to launder proceeds from large exchange hacks.

---

**Q41. Correct: A**

A peel chain is defined by a large 'change' amount carrying forward through repeated hops while a small amount is 'peeled off' at each step — exactly the pattern described here, and it's one of the most heavily tested fund-tracing patterns on the CCFC.

---

**Q42. Correct: C**

A nested exchange operates its own customer base and order flow but relies on a parent exchange's wallet infrastructure for settlement, typically without independent KYC/AML oversight — this creates elevated risk because the parent exchange may have limited visibility into the nested exchange's own customers.

---

**Q43. Correct: C**

TXIDs and addresses are the objective, verifiable on-chain data points that allow anyone to reconstruct and audit the fund flow — this is the minimum standard for defensible investigation documentation and reporting.

---

**Q44. Correct: B**

Indirect exposure captures risk that flows through one or more intermediary wallets rather than through a direct transaction with the sanctioned entity — this is a core risk-scoring concept tested on the CCFC.

---

**Q45. Correct: C**

Mixing obscures but does not eliminate underlying illicit-origin risk; a risk-based KYT approach flags funds with mixer exposure for enhanced due diligence rather than treating the mixing step as a compliance 'reset', since exposure through obfuscation services is itself a known high-risk indicator.

---

