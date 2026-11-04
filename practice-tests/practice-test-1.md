# Practice Test 1: CCFC: Chainalysis Crypto Fundamentals Certification Prep

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A blockchain network validates transactions by having participants stake collateral rather than compete with computational power. Which consensus mechanism does this describe, and what is the primary trade-off compared to the alternative?

A) Proof of Stake — validators are chosen based on the amount of cryptocurrency they lock up, offering lower energy use but raising concerns about wealth concentration in validation power
B) Proof of Work — requires specialized ASIC hardware and consumes more energy than staking-based consensus
C) Proof of Authority — validators are pre-approved corporate entities, offering high throughput but no decentralization
D) Delegated Proof of Work — miners delegate hashing power to pools, reducing energy use while preserving full decentralization

---

**Q2.** A financial institution needs to offer clients a digital asset that maintains a stable value pegged to the US dollar for use in payments, without the price volatility of Bitcoin or Ether. Which type of crypto asset should the institution select?

A) Stablecoin
B) Wrapped token
C) Utility token
D) Governance token

---

**Q3.** On the Bitcoin network, a new block is added to the blockchain approximately every 10 minutes on average. What mechanism ensures this block time remains roughly constant despite fluctuations in total network hash power?

A) Difficulty adjustment recalculates every 2016 blocks based on the time taken to mine the previous 2016 blocks
B) The block reward halves every 210,000 blocks
C) Validators vote every epoch to adjust block time
D) Miners manually set block time in each block header

---

**Q4.** Which statement BEST distinguishes Ethereum from Bitcoin at the protocol level?

A) Ethereum has a fixed maximum supply of 21 million coins like Bitcoin
B) Bitcoin uses account-based balances while Ethereum uses the UTXO model
C) Both networks rely exclusively on Proof of Work following their most recent upgrades
D) Ethereum supports Turing-complete smart contracts enabling programmable applications, while Bitcoin's scripting language is intentionally limited

---

**Q5.** An investigator observes that funds tied to a hack were sent through a service that pools transactions from many users and redistributes them, obscuring the transaction trail before the funds reach an exchange. Which type of service is being used, and why does it complicate blockchain analysis?

A) A mixer/tumbler, because it deliberately breaks the on-chain link between input and output addresses by combining and redistributing funds from multiple sources
B) A custodial exchange wallet, because deposits from multiple users share the same hot wallet address
C) A hardware wallet, because it stores private keys offline
D) A smart contract escrow, because it holds funds until conditions are met

---

**Q6.** A developer wants to build a decentralized lending application where users can borrow and lend crypto assets without a centralized intermediary holding custody of funds. Which segment of the crypto ecosystem does this represent?

A) Centralized exchange (CEX)
B) Custodial wallet provider
C) Payment processor
D) Decentralized Finance (DeFi) protocol

---

**Q7.** A blockchain network requires validators to lock up a quantity of the network's native cryptocurrency as collateral in order to be selected to propose and validate new blocks, with malicious behavior resulting in a loss of that collateral. Which consensus mechanism does this describe?

A) Proof of Stake
B) Proof of Authority
C) Proof of Work
D) Proof of Elapsed Time

---

**Q8.** An investigator is tracing funds that moved from a centralized exchange withdrawal address, through a series of DeFi protocol interactions, and ultimately into a service that pools many users' funds together and breaks the on-chain link between depositors and withdrawers before the funds re-emerge at unrelated addresses. Which component of the crypto ecosystem does the pooling service represent?

A) A custodial wallet provider
B) A stablecoin issuer
C) A mixer (tumbler)
D) A blockchain oracle

---

**Q9.** In Bitcoin's key architecture, which statement accurately describes the relationship between a private key, public key, and address?

A) The address is generated first, then used to derive the public key via SHA-256
B) The private key is derived from the public key using elliptic curve multiplication, then hashed to create the address
C) The private key and address are mathematically identical; only their encoding format differs
D) The public key is derived from the private key using elliptic curve multiplication, and the address is created by hashing the public key

---

**Q10.** A compliance analyst is building a tool that must calculate an address's exact spendable balance by summing all unspent transaction outputs associated with that address, rather than reading a single balance field. Which blockchain model does this describe, and which cryptocurrency uses it?

A) Account model, as used by Ethereum
B) Account model, as used by Bitcoin
C) UTXO model, as used by Ethereum
D) UTXO model, as used by Bitcoin

---

**Q11.** A Bitcoin transaction has one input of 0.5 BTC and two outputs: 0.3 BTC to an unfamiliar address and 0.1999 BTC sent back to an address with prior transaction history linked to the sender. Which output most likely represents the change returned to the sender?

A) The 0.3 BTC output, because it is the larger amount
B) Neither output; Bitcoin transactions do not generate change
C) The 0.1999 BTC output sent to the address with prior history linked to the sender
D) The 0.3 BTC output, because unfamiliar addresses always represent change

---

**Q12.** When a Bitcoin transaction is created, which of the following correctly describes the signing and broadcast process?

A) The public key signs the transaction, and only the signature is broadcast to the network
B) The private key signs the transaction, and the entire signed transaction, including the public key and signature, is broadcast to the network
C) The private key encrypts the transaction data, and nodes decrypt it using the sender's public key before broadcasting
D) The wallet software broadcasts the raw private key alongside the transaction so nodes can verify signatures

---

**Q13.** An exchange holds 95% of customer crypto assets in cold storage wallets that are never connected to the internet, and 5% in hot wallets used for daily withdrawal processing. From a security standpoint, what is the primary reason this custody structure reduces risk exposure?

A) Cold wallets automatically generate new addresses for every transaction, making clustering impossible
B) Hot wallets use a different blockchain consensus mechanism that is inherently more secure
C) Cold storage private keys are offline and cannot be accessed remotely, limiting the funds exposed to a compromise of internet-connected systems
D) Cold storage transactions are not recorded on the public blockchain, making them untraceable

---

**Q14.** An investigator views a Bitcoin transaction with 12 inputs, each contributing a small UTXO from the same address history, and 1 output. The transaction has 6 confirmations on the network. What does this transaction structure and confirmation count most likely indicate?

A) A change output was mistakenly omitted, meaning the transaction is still pending
B) A UTXO consolidation transaction that has been confirmed by 6 subsequent blocks, generally considered a secure confirmation depth
C) The transaction is invalid because Bitcoin does not allow more than 2 inputs per transaction
D) The transaction has only 6 confirmations, meaning it is unconfirmed and could still be reversed by the sender

---

**Q15.** In the UTXO model used by Bitcoin, a wallet has one unspent output worth 0.5 BTC and wants to send 0.2 BTC to a recipient. How does the transaction typically handle the remaining balance?

A) The full 0.5 BTC input is consumed, 0.2 BTC goes to the recipient, and the remainder (minus fees) is sent back to a change address controlled by the sender
B) The wallet splits the 0.5 BTC output into two new addresses automatically without a transaction fee
C) The 0.3 BTC difference remains locked in the original UTXO until manually reclaimed by the sender
D) The transaction fails because partial spending of a UTXO is not permitted

---

**Q16.** An investigator sees a transaction with five input addresses and two output addresses. Applying the common-spend (multi-input) heuristic, which conclusion is BEST supported?

A) All five input addresses are almost certainly controlled by the same entity, since spending them together requires knowledge of all corresponding private keys
B) The two output addresses must belong to the same entity as the inputs
C) The transaction is definitely a CoinJoin mixing transaction
D) No clustering conclusion can be drawn because outputs outnumber a single recipient

---

**Q17.** Which statement BEST describes why public blockchains like Bitcoin are described as 'pseudonymous' rather than 'anonymous'?

A) Every transaction requires a government-issued ID to be recorded on-chain
B) Addresses are permanently linked to real-world identities from the moment of wallet creation
C) Blockchain data is encrypted so no one can ever view transaction history
D) Transactions are publicly visible and permanently linked to addresses, and those addresses can potentially be tied to real-world identities through off-chain data and analysis

---

**Q18.** An analyst is tracing funds and observes a series of transactions where a large amount is repeatedly split into a small payment to a new address and a large remainder sent to another new address, over dozens of hops. What is this pattern called, and what is its typical purpose?

A) A CoinJoin, used to combine unrelated users' funds into a single anonymous pool
B) A change address heuristic, used only to identify the wallet software that created the transaction
C) A peel chain, often used to obscure the destination of funds by gradually 'peeling off' smaller amounts while moving the bulk of value forward
D) A double-spend attempt, exploiting a race condition in the mempool

---

**Q19.** Which characteristic is a commonly used heuristic to identify the CHANGE output in a typical Bitcoin transaction with two outputs?

A) The change output is always the first output listed in the transaction
B) The change output typically has a value type/format (e.g., round number vs. non-round, or address type) that differs from the payment output, and is often sent to a new, previously unused address
C) The change output always has a higher transaction fee attached than the payment output
D) The change output is always sent back to the exact same address that sent the original input

---

**Q20.** A compliance analyst has clustered a set of addresses using the multi-input heuristic and now wants to attribute this cluster to a real-world entity such as a specific exchange. Which source is MOST useful for making this attribution?

A) Off-chain data such as known deposit/withdrawal addresses reported by exchanges, tagged data from investigations, web-scraped service information, or subpoena results
B) The total number of transactions the cluster has ever made
C) The color and design of the entity's publicly viewable website homepage
D) The average block confirmation time of transactions sent by the cluster

---

**Q21.** Which technique is specifically designed to break or weaken the effectiveness of the common-input-ownership (co-spend) heuristic used in blockchain clustering?

A) Using a hardware wallet instead of a software wallet
B) CoinJoin-style transactions that combine inputs from multiple unrelated participants into a single transaction with mixed outputs
C) Sending funds through a centralized exchange with mandatory KYC
D) Using a block explorer to view transaction history

---

**Q22.** An investigator is using the common-input-ownership heuristic to cluster addresses believed to belong to a single wallet. The transaction history includes several CoinJoin transactions, where the investigator notices unusually large numbers of inputs and outputs of identical value. What is the BEST action for the investigator to take when applying the clustering heuristic to these specific transactions?

A) Apply the heuristic normally, since CoinJoin transactions strengthen the confidence of the common-input-ownership assumption
B) Exclude these transactions from automatic clustering, since CoinJoin is designed to break the assumption that all inputs share a single owner
C) Merge every input and output address of the CoinJoin transaction into one cluster, since all parties intentionally combined funds
D) Discard the entire address cluster built so far, since one CoinJoin transaction invalidates all prior clustering for that entity

---

**Q23.** A company explains that Bitcoin is 'pseudonymous rather than anonymous.' Which statement BEST captures why this distinction matters for blockchain analysis and investigations?

A) Addresses act as persistent public identifiers, and once one address in a cluster is linked to a real-world identity through off-chain data, the entire cluster's transaction history can be attributed to that identity
B) Every transaction requires a government-issued ID to be embedded directly in the blockchain, so identities are always public
C) Transaction data is encrypted end-to-end, so analysis firms must decrypt each block before any address can ever be identified
D) Anonymity and pseudonymity are functionally identical for investigative purposes, since neither can ever be linked to a real-world identity

---

**Q24.** A U.S.-based virtual asset service provider (VASP) processes an outbound crypto transfer of $2,500 on behalf of a customer to a beneficiary at another hosted-wallet VASP. Under FinCEN's Travel Rule as applied to convertible virtual currency, what is the VASP's obligation regarding transmission of originator and beneficiary information?

A) The VASP must transmit full originator and beneficiary information because all crypto transfers require it regardless of amount
B) The VASP must transmit the information only because the counterparty is also a VASP, regardless of amount
C) The VASP must transmit the information because the transfer exceeds the FATF Recommendation 16 threshold of $1,000
D) The VASP has no obligation to transmit this information because the transfer is below the $3,000 FinCEN Travel Rule threshold

---

**Q25.** During screening, a VASP identifies that a customer's outgoing transaction is destined for a wallet address listed on OFAC's Specially Designated Nationals (SDN) list. What is the compliance-correct action?

A) Allow the transaction to proceed but flag it for review after settlement
B) Only monitor future transactions from the same customer without acting on this one
C) Cancel the customer's account without taking any action regarding the specific transaction or funds
D) Reject the transaction, block/freeze the associated funds as required, and file a report with OFAC

---

**Q26.** A compliance team wants a solution that continuously screens live, on-chain cryptocurrency transactions and wallet addresses against risk indicators (e.g., darknet market exposure, sanctioned addresses) in real time as transactions occur. Which compliance function does this describe?

A) Customer Due Diligence (CDD)
B) Know Your Customer (KYC) onboarding
C) Enhanced Due Diligence (EDD) periodic review
D) Know Your Transaction (KYT) monitoring

---

**Q27.** A VASP's transaction monitoring system flags a customer whose incoming funds show a cumulative exposure of 15% originating from addresses associated with a sanctioned darknet market over the past 90 days. Per a typical risk-based compliance program, what should this trigger?

A) Escalation to Enhanced Due Diligence (EDD), including further investigation of the fund source and possible SAR filing
B) Automatic account closure with no further review required
C) No action, since the exposure is below a 50% materiality threshold
D) A one-time email notice to the customer requesting clarification, with no internal escalation

---

**Q28.** Which statement correctly distinguishes Customer Due Diligence (CDD) from Enhanced Due Diligence (EDD) in a crypto AML program?

A) CDD and EDD are identical processes applied to all customers regardless of risk level
B) CDD is only required for institutional customers, while EDD is only required for retail customers
C) EDD replaces the need for KYC identity verification, while CDD is used only for transaction monitoring
D) CDD is the baseline identity verification and risk assessment applied to all customers, while EDD is additional, heightened scrutiny applied to higher-risk customers or transactions

---

**Q29.** A VASP receives an incoming crypto transfer from a foreign VASP that is subject to the FATF Travel Rule but fails to provide any originator information as required. Following a risk-based approach, what is the most appropriate action for the receiving VASP?

A) Automatically process the transaction as normal since the sending VASP bears sole responsibility for compliance
B) Ignore the missing data if the transaction amount is below $10,000
C) Treat the missing information as a red flag, apply additional scrutiny, and consider rejecting or delaying the transaction pending the missing data
D) Report the incident only if the customer requests a refund

---

**Q30.** The FATF Travel Rule requires VASPs to share originator and beneficiary information for transactions above a certain threshold. What is the commonly referenced threshold amount used in FATF guidance?

A) USD/EUR 1,000
B) USD/EUR 3,000
C) USD/EUR 500
D) USD/EUR 10,000

---

**Q31.** A VASP implements a Know Your Transaction (KYT) solution to monitor incoming and outgoing crypto transactions. What is the primary purpose of KYT in this context?

A) To verify the government-issued identification of new customers during onboarding
B) To continuously screen and score transactions against blockchain-derived risk indicators, such as exposure to sanctioned or illicit entities
C) To automatically freeze all customer accounts exceeding a preset transaction volume
D) To replace the need for customer due diligence (CDD) entirely by relying solely on blockchain data

---

**Q32.** An individual meets someone on a dating app who gradually builds trust over weeks, then introduces a 'can't-miss' crypto trading platform showing consistently rising fake profits. The victim is coached to keep depositing more funds until, upon trying to withdraw, all withdrawals are blocked and the counterparty disappears. Which typology does this describe?

A) Rug pull
B) Pig butchering scam
C) Ransomware attack
D) Darknet market exit scam

---

**Q33.** Developers launch a new token, hype it heavily on social media, and once liquidity pool deposits reach a peak, they immediately withdraw all liquidity from the decentralized exchange pool, causing the token price to collapse to near zero within minutes. Which typology best fits this scenario?

A) Ponzi scheme
B) Rug pull
C) Chain-hopping
D) Sanctions evasion

---

**Q34.** Which statement BEST distinguishes a Ponzi scheme from a rug pull in the context of crypto financial crime typologies?

A) Both terms describe the identical typology and are used interchangeably in blockchain analysis.
B) Ponzi schemes pay earlier investors using funds from new investors over an extended period, while rug pulls involve an abrupt exit where operators drain project funds or liquidity almost immediately after launch.
C) Rug pulls always involve compromised private keys, whereas Ponzi schemes never involve any form of key compromise.
D) Ponzi schemes only occur on centralized exchanges, while rug pulls can only occur on decentralized exchanges.

---

**Q35.** An attacker deploys ransomware that encrypts a victim organization's files AND exfiltrates sensitive data beforehand, then threatens to publicly leak the stolen data unless an additional crypto payment is made on top of the decryption ransom. Which term best describes this specific ransomware behavior?

A) Chain-hopping
B) Double extortion ransomware
C) Darknet market vendor exit scam
D) Layering

---

**Q36.** Following a cross-chain bridge exploit, the attacker moves stolen funds through several different blockchains, swapping assets via decentralized exchanges and passing funds through a mixing service before consolidating the proceeds at a centralized exchange deposit address. This sequence of obfuscation techniques is best classified as an example of which laundering pattern?

A) Pig butchering
B) Rug pull
C) Layering via chain-hopping
D) Terrorism financing

---

**Q37.** An entity linked to a sanctioned jurisdiction uses a network of nested exchange accounts and several intermediary wallets to obscure the origin of funds before ultimately cashing out at an exchange, in an apparent attempt to evade OFAC-administered sanctions. Which typology does this scenario represent?

A) Darknet market activity
B) Sanctions evasion
C) Ransomware payment
D) Rug pull

---

**Q38.** An investigator reviews a victim's crypto wallet history and finds funds were sent over several weeks to an address associated with a platform promising guaranteed high returns on 'trading education,' after the victim was cultivated for months through a romance-style relationship on a messaging app before being introduced to the platform. Which illicit-activity typology does this MOST closely match?

A) Ransomware double-extortion scheme
B) Darknet market vendor payout
C) Pig butchering scam
D) Sanctioned mixer usage

---

**Q39.** An address cluster receives stolen funds from a hack, then those funds are moved through several unrelated blockchains via cross-chain bridges before arriving at a cash-out exchange, with no single mixing service used at any point. Which laundering technique does this describe?

A) Peel chaining on a single blockchain
B) Coinjoin mixing
C) Chain-hopping
D) Nested exchange layering

---

**Q40.** A ransomware operator receives a Bitcoin payment directly to a wallet address published in the ransom note, then immediately forwards the full amount to a service that also processes deposits from previously sanctioned darknet market wallets, with no attempt to break the funds into smaller amounts first. From a typology standpoint, what does the operator's behavior in this scenario represent?

A) Direct cash-out without obfuscation, increasing traceability risk
B) A textbook peel chain layering technique
C) Use of the Lightning Network to avoid on-chain analysis
D) A FATF Travel Rule compliant transfer

---

**Q41.** A compliance analyst has traced funds from a confirmed ransomware payment address through several intermediary wallets, ending at a deposit address at a licensed VASP. What is the BEST next step?

A) Immediately freeze all funds held in the analyst's own personal wallet
B) Publicly disclose the flagged address on social media to warn other users
C) Delete the internal transaction records to limit the analyst's personal liability
D) File a SAR/STR with the relevant FIU and, if an existing relationship permits, notify the VASP's compliance team, documenting the full transaction path and cluster attribution

---

**Q42.** A wallet receives 5% of its total inbound value directly from a known darknet market address, with the remaining 95% coming from a reputable exchange. How should this be handled in risk assessment?

A) The wallet is automatically classified high risk regardless of the exposure percentage or amount
B) The wallet is automatically cleared as low risk because most inbound funds come from a legitimate exchange
C) The wallet has direct exposure to darknet market risk and must be evaluated based on the absolute value and materiality of that exposure, not dismissed simply because it is a small percentage
D) Exposure below 10% of total inbound volume is never flagged or reported by KYT tools

---

**Q43.** In blockchain risk-scoring configurations, what differentiates 'direct exposure' from 'indirect exposure' to a flagged entity?

A) Direct exposure applies only to fiat off-ramp transactions, while indirect exposure applies only to on-chain crypto transfers
B) Direct and indirect exposure are identical metrics; the terms differ only by vendor naming convention
C) Indirect exposure is always scored as higher risk than direct exposure in every configuration
D) Direct exposure is funds received from or sent to a flagged entity in the immediate transaction hop, while indirect exposure reflects exposure occurring through one or more intermediary addresses

---

**Q44.** Why is address clustering important for investigations and risk reporting?

A) It encrypts wallet addresses to protect the privacy of legitimate users
B) It calculates mining or staking rewards owed to a wallet
C) It groups multiple addresses believed to be controlled by the same entity, giving investigators a more accurate picture of total counterparty exposure and fund flows
D) It fully replaces the need for KYC documentation during onboarding

---

**Q45.** An investigator is finalizing a case file documenting a suspected sanctions evasion typology for referral to law enforcement. Which piece of information is MOST critical to include in the report?

A) The current market price of the cryptocurrency at the time the report was written
B) A list of every address the receiving exchange has ever processed
C) A complete, timestamped transaction trail showing fund flow with cluster attributions, entity risk indicators, and exportable evidence from the analysis tool
D) The investigator's personal opinion on whether the wallet owner is guilty

---

