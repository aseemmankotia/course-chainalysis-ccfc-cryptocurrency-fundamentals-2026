# Practice Test 2: CCFC: Chainalysis Crypto Fundamentals Certification Prep

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A blockchain analyst is comparing Bitcoin's Nakamoto consensus (Proof of Work) to Ethereum's post-Merge Proof-of-Stake consensus. Which statement correctly describes a security property that PoS chains must address but PoW chains do not?

A) Weak subjectivity: new or offline-for-a-long-time nodes must obtain a recent trusted checkpoint to correctly identify the canonical chain, since a validator's staked history can be costlessly rewritten from genesis
B) 51% attacks are impossible under Proof of Stake
C) Proof of Stake requires specialized mining hardware to consume more energy than Proof of Work
D) Double-spending is only prevented on Proof-of-Stake chains, not Proof-of-Work chains

---

**Q2.** Which pairing correctly matches a stablecoin with its actual collateralization or stabilization mechanism?

A) DAI — overcollateralized by crypto assets locked in smart contracts via the MakerDAO protocol
B) USDC — stabilized purely through an algorithmic seigniorage mechanism with no reserve assets
C) USDT (Tether) — collateralized solely by holdings of other stablecoins
D) TerraUSD (UST) — fully backed 1:1 by USD held in audited bank reserves

---

**Q3.** Under Ethereum's EIP-1559 fee mechanism, which statement correctly describes the base fee?

A) The base fee is a tip paid directly to validators to prioritize transaction inclusion
B) The base fee is fixed at 21,000 gas units for every transaction type on the network
C) EIP-1559 eliminated gas limits entirely, so transactions no longer need to specify one
D) The base fee is burned (permanently removed from circulating supply) and adjusts algorithmically block-to-block based on network demand

---

**Q4.** An investigator reviewing DeFi activity finds a user provided liquidity to an ETH/USDC pool on an automated market maker (AMM) when ETH was priced at $2,000. ETH later rose to $4,000. Compared to simply holding the original ETH and USDC amounts separately, which outcome BEST describes what happened to the liquidity provider's position?

A) The LP earned exactly the same value as holding, since AMMs guarantee price parity with external markets
B) The LP's funds became permanently inaccessible once the external ETH price diverged from the pool price
C) Arbitrageurs voluntarily sent extra ETH into the pool to compensate the LP for taking on price risk
D) The LP experienced impermanent loss — the pool's constant-product formula rebalanced the pool toward more USDC and less ETH as arbitrageurs traded against the price move, so the LP's withdrawn value underperformed simply holding

---

**Q5.** Which statement correctly distinguishes ERC-721 tokens from ERC-20 tokens on Ethereum?

A) ERC-721 tokens are fungible and divisible, while ERC-20 tokens are non-fungible and indivisible
B) ERC-721 defines non-fungible tokens where each token ID is unique and distinct, while ERC-20 defines fungible, interchangeable tokens
C) ERC-721 can only be used to represent stablecoins, while ERC-20 is reserved exclusively for governance tokens
D) ERC-721 tokens cannot be transferred between wallets, while only ERC-20 tokens support transfers

---

**Q6.** A blockchain analyst observes a Bitcoin transaction combining inputs from several apparently unrelated wallets into one transaction, with multiple equal-value outputs distributed to different, previously unlinked addresses and no clear common ownership signal among the inputs. This pattern is most consistent with which technique?

A) A standard multi-signature wallet consolidation transaction
B) A change-address heuristic applied by the analyst's own clustering software
C) A CoinJoin-style mixing transaction that pools inputs from multiple unrelated participants specifically to defeat the common-input-ownership heuristic used in address clustering
D) A replace-by-fee (RBF) double-spend attempt

---

**Q7.** An investigator is analyzing a blockchain that uses Proof of Stake consensus, where validators must lock up crypto assets as collateral and face 'slashing' penalties for malicious or negligent behavior. Which statement BEST describes how this security model differs from a Proof of Work blockchain's approach to preventing attacks?

A) Proof of Stake eliminates any economic cost to participate in consensus, making it inherently more decentralized than Proof of Work
B) Proof of Work validators are chosen randomly based on staked amount, while Proof of Stake relies on computational competition to add blocks
C) Proof of Stake relies on economic penalties against validators' staked capital, while Proof of Work relies on the cost of computational power (hash rate) to disincentivize attacks
D) Proof of Stake and Proof of Work both require identical specialized mining hardware, differing only in how energy consumption is reported

---

**Q8.** A compliance analyst is reviewing an on-chain transaction that moves USDT on the Ethereum blockchain. Which statement accurately describes the relationship between USDT and Ethereum in this scenario?

A) USDT is Ethereum's native asset used to pay gas fees, functioning identically to ETH in that role
B) USDT operates on a completely separate blockchain and is only bridged to Ethereum for exchange listing purposes
C) USDT is a token built using the ERC-20 standard, meaning it runs on Ethereum's smart contract infrastructure rather than having its own dedicated blockchain
D) USDT transfers on Ethereum do not require gas fees because Tether operates independently of Ethereum's consensus mechanism

---

**Q9.** A Bitcoin wallet holds a single UTXO worth 0.5 BTC. The user wants to send 0.3 BTC to a merchant, with a network fee of 0.0001 BTC. Which of the following BEST describes how the transaction must be structured?

A) The wallet spends 0.3 BTC from the UTXO and leaves 0.2 BTC untouched in the same UTXO for later use
B) The wallet splits the existing UTXO into two 0.25 BTC UTXOs before broadcasting, then spends one
C) The wallet consumes the entire 0.5 BTC UTXO as input and creates two outputs: 0.3 BTC to the merchant and 0.1999 BTC as change back to a wallet-controlled address
D) The wallet sends the full 0.5 BTC to the merchant and later requests a manual refund of 0.2 BTC

---

**Q10.** An Ethereum account has an on-chain nonce of 15 (meaning the next valid transaction must use nonce 15). The wallet software broadcasts a new transaction using nonce 16 while no transaction with nonce 15 has yet been submitted or confirmed. What is the MOST likely result?

A) The transaction with nonce 16 is mined immediately because gas price, not nonce, determines mining priority
B) The transaction with nonce 16 remains stuck (pending) in the mempool until a transaction with nonce 15 is submitted and confirmed, because the account model enforces strict sequential nonce ordering
C) The network automatically renumbers the transaction to nonce 15 so it can be processed right away
D) The transaction is dropped outright because out-of-order nonces are never accepted into the mempool

---

**Q11.** A crypto exchange wants to secure roughly 95% of customer funds against remote hacking, requiring that rare, batch-signed withdrawals be reviewed and approved by multiple staff members before broadcast. Which storage approach BEST meets these requirements?

A) A hot wallet with single-key signing configured for instant, low-friction withdrawals
B) A custodial hot wallet protected only by two-factor authentication on the withdrawal interface
C) A single hardware wallet that stays permanently connected to the exchange's production server
D) A cold storage multisignature wallet with keys generated and held offline, requiring manual or air-gapped signing by multiple parties

---

**Q12.** Which statement correctly differentiates the UTXO model (e.g., Bitcoin) from the account-based model (e.g., Ethereum)?

A) The UTXO model tracks a single running balance per address, while the account model tracks discrete unspent transaction outputs
B) Both models track balances identically, differing only in the digital signature algorithm used
C) The account model requires no global state, while the UTXO model requires maintaining a global state tree of balances
D) In the UTXO model, each transaction consumes existing unspent outputs and creates new ones, while in the account model, a transaction directly debits and credits a running balance tracked using a per-account nonce

---

**Q13.** You inspect a Bitcoin transaction on a block explorer and observe: 3 confirmations, 2 inputs totaling 1.2 BTC, 2 outputs of 0.7 BTC and 0.4999 BTC, and a transaction fee of 0.0001 BTC. What can you correctly conclude?

A) The transaction is still unconfirmed and currently sitting in the mempool
B) One of the two outputs is very likely a change output returned to the sender, and the transaction has already been included in at least three blocks
C) The transaction must have used the account model, since it has multiple inputs
D) The 0.0001 BTC fee was paid by the recipient rather than the sender

---

**Q14.** A compliance analyst needs to continuously monitor all incoming funds to a set of customer-controlled Bitcoin addresses but must never have the ability to move or spend those funds. Which wallet configuration is BEST suited to this need?

A) A hot wallet configured with full private key access for rapid transaction signing
B) A watch-only wallet configured using only public keys or addresses, with no private key material present
C) A cold hardware wallet kept in a bank vault and accessed quarterly
D) A custodial exchange wallet where the exchange holds and controls the private keys

---

**Q15.** A Bitcoin wallet holds three UTXOs: 0.3 BTC, 0.5 BTC, and 0.7 BTC. The user wants to send 0.9 BTC to a merchant, and the wallet's coin selection algorithm selects the 0.5 BTC and 0.7 BTC UTXOs as transaction inputs. After a 0.0001 BTC network fee, what happens to the leftover 0.2999 BTC?

A) The leftover amount is automatically returned to the merchant as a refund on a separate transaction
B) The leftover amount is destroyed, since UTXOs must be fully consumed once selected as inputs
C) The leftover amount stays in the original 0.5 BTC and 0.7 BTC UTXOs untouched, since only 0.9 BTC was needed
D) The leftover amount is sent to a change output, typically a new address controlled by the sender's own wallet

---

**Q16.** An investigator applies the common-input-ownership heuristic to a Bitcoin transaction that turns out to be a CoinJoin combining inputs from many unrelated wallets. What is the correct analytical conclusion?

A) The heuristic correctly clusters all input addresses because they signed the same transaction
B) The heuristic automatically detects and excludes CoinJoin transactions using digital signature analysis
C) The heuristic should not be applied to CoinJoin transactions since doing so would incorrectly merge addresses controlled by unrelated entities
D) The heuristic identifies the CoinJoin as a peeling chain and flags all outputs as change

---

**Q17.** While tracing funds from a hack, an analyst observes dozens of sequential transactions where each transaction sends a small amount to a new address and forwards the large remainder to another new address, repeating many times. What pattern is this?

A) A CoinJoin mixing round
B) A peeling chain, used to gradually move and obscure funds while retaining most value in a new change address each hop
C) A deposit address consolidation pattern typical of exchange sweeps
D) A failure of the change address heuristic caused by address reuse

---

**Q18.** Which clustering heuristic groups addresses by identifying which output in a transaction is likely returning value back to the sender, based on cues like address type or non-round value?

A) Common-input-ownership heuristic
B) Address reuse heuristic
C) Change address heuristic, which flags the output likely returning value to the sender based on characteristics like address type or non-round value
D) Peel chain heuristic

---

**Q19.** An analyst has a cluster of on-chain addresses believed to belong to a specific unlicensed exchange. Which approach is primarily used to attribute this cluster to that real-world entity?

A) Applying the common-input-ownership heuristic exclusively to all transactions
B) Monitoring mempool propagation timing across nodes
C) Analyzing on-chain transaction volume alone without external data
D) Combining off-chain data such as KYC records, subpoenas, and public web information with on-chain clustering results

---

**Q20.** Exchanges typically assign a unique deposit address to each customer. Why are these deposit addresses generally NOT merged into a single cluster by the common-input-ownership heuristic?

A) Exchanges use identical addresses for every customer
B) Deposit addresses are typically each used once to receive funds and aren't spent together in a single transaction, so the co-spend heuristic doesn't link them
C) Deposit addresses are always multisig and cannot be clustered
D) Deposit addresses are excluded from the blockchain protocol itself

---

**Q21.** Which statement best explains why Bitcoin is considered 'pseudonymous' rather than 'anonymous'?

A) Transactions are recorded under persistent addresses that can potentially be linked to real-world identities through clustering and off-chain data, rather than being untraceable
B) Every address is directly linked to a government-issued ID at creation
C) Bitcoin transactions are fully encrypted and cannot be viewed by anyone except sender and receiver
D) Anonymity and pseudonymity are interchangeable terms in blockchain analysis

---

**Q22.** An investigator reviews a Bitcoin transaction with 5 inputs and 2 outputs and applies the common-input-ownership (co-spend) heuristic to conclude that all 5 input addresses belong to a single entity. One of the inputs is later identified as originating from a known CoinJoin coordinator output. Which statement BEST explains why the investigator's clustering conclusion may be flawed?

A) The heuristic is still valid because CoinJoin transactions only obfuscate output addresses through mixing and never affect the ownership of input addresses.
B) The heuristic assumes all inputs in a transaction share a single owner, but CoinJoin transactions deliberately combine inputs from multiple independent, unrelated participants, which breaks that core assumption.
C) The heuristic fails here because CoinJoin transactions always use exactly one input address, so multi-input clustering could not apply in the first place.
D) The heuristic remains fully accurate because blockchain analysis tools automatically detect and exclude all CoinJoin transactions from any clustering dataset.

---

**Q23.** On the exam, which statement BEST captures the distinction between pseudonymity and anonymity as it applies to analyzing transactions on a public blockchain?

A) Pseudonymous and anonymous are interchangeable terms in blockchain analysis because neither type of address can ever be linked to a real-world identity.
B) Pseudonymous addresses can never be linked to an identity under any circumstances, while anonymous transactions can always be traced directly through on-chain data alone.
C) Pseudonymous means activity is tied to a persistent address whose real-world identity can potentially be uncovered through external data such as KYC records, exchange deposits, or IP metadata, whereas true anonymity means no such link could ever be established.
D) Anonymity refers to transaction data that is cryptographically encrypted on the public ledger, while pseudonymity refers to transaction data stored in unencrypted plaintext.

---

**Q24.** A VASP is determining whether a cryptocurrency transfer triggers Travel Rule data-sharing obligations under FATF Recommendation 16. Under FATF's guidance, what is the threshold above which originator and beneficiary information must be collected and transmitted?

A) $250 USD/EUR
B) $3,000 USD/EUR
C) $10,000 USD/EUR
D) $1,000 USD/EUR

---

**Q25.** A VASP in a jurisdiction with fully implemented Travel Rule regulations sends a transaction to a VASP in a jurisdiction that has not yet enacted Travel Rule legislation. This scenario, where uneven regulatory implementation timelines across jurisdictions create compliance gaps, is commonly referred to as what?

A) Jurisdictional lag
B) Travel Rule arbitrage
C) Regulatory shadowing
D) The sunrise issue

---

**Q26.** A compliance analyst uses a KYT (Know Your Transaction) tool to monitor incoming deposits. The tool flags a transaction because the funds passed through two intermediary wallets before reaching a darknet market, rather than being sent directly from the market. This type of exposure is best described as:

A) Direct exposure
B) Indirect exposure
C) Custodial exposure
D) Peel chain exposure

---

**Q27.** Under a risk-based AML program, which scenario would MOST likely require a VASP to apply Enhanced Due Diligence (EDD) rather than standard Customer Due Diligence (CDD)?

A) A customer is a politically exposed person (PEP) receiving funds from a high-risk jurisdiction
B) A customer completes a low-value routine retail purchase
C) A customer verified with government ID at onboarding
D) A customer transacts only within a domestic exchange

---

**Q28.** OFAC has added specific cryptocurrency wallet addresses to the Specially Designated Nationals (SDN) List, such as those associated with the Lazarus Group. What is the PRIMARY compliance obligation this creates for a U.S. VASP?

A) The VASP may simply monitor the address without further action
B) The obligation only applies if the counterparty is a domestic customer
C) The VASP must freeze/block transactions involving those addresses and file required reports
D) The obligation only applies to transactions exceeding $10,000

---

**Q29.** Under the FATF definition of a Virtual Asset Service Provider (VASP), which of the following entities would generally NOT be classified as a VASP?

A) A developer who publishes open-source, non-custodial wallet software with no ongoing service
B) A centralized cryptocurrency exchange
C) A custodial wallet provider
D) A cryptocurrency ATM operator

---

**Q30.** A Virtual Asset Service Provider (VASP) processes a crypto transfer equivalent to USD 1,200 on behalf of a customer to a beneficiary held at another VASP. Under the FATF Travel Rule (Recommendation 16), which of the following is required?

A) The originating VASP must obtain and transmit the required originator and beneficiary information to the beneficiary VASP, since the transfer exceeds the FATF threshold of USD/EUR 1,000
B) The originating VASP only needs to verify its own customer's identity; transmitting beneficiary information to the receiving VASP is optional at the VASP's discretion
C) No Travel Rule data is required because the transfer is below the $3,000 threshold used for traditional bank wire transfers
D) The Travel Rule only applies to transfers between unhosted (self-custodied) wallets, not VASP-to-VASP transfers

---

**Q31.** OFAC adds a specific cryptocurrency wallet address to the Specially Designated Nationals (SDN) List. A US-based exchange discovers that a customer's account holds funds that were previously deposited from that now-designated address. What is the exchange's compliance obligation?

A) Freeze (block) the funds traceable to the designated address and file a report with OFAC, since property in which a designated person has an interest must be blocked regardless of who currently holds it
B) Report the customer to FinCEN under the Bank Secrecy Act, but only if the original deposit exceeded the $10,000 Currency Transaction Report threshold
C) No action is required unless the customer subsequently attempts to send funds directly back to the sanctioned address
D) Simply flag the account for enhanced monitoring going forward, since the sanctioned party is the address owner, not the customer

---

**Q32.** An investigator reviews a case where the victim was contacted online by a stranger who spent several weeks building a personal relationship before introducing a 'guaranteed high-return' crypto trading platform. The victim deposited funds over several months, watched fake profits accrue on a spoofed dashboard, and was ultimately unable to withdraw any funds. On-chain, the deposit address received funds from dozens of similar victims before rapidly consolidating and cashing out through a chain of intermediary wallets to a single exchange deposit address. Which illicit-activity typology does this scenario BEST describe?

A) SIM-swapping account takeover
B) Rug pull
C) Ponzi scheme
D) Pig butchering

---

**Q33.** A ransomware affiliate receives a Bitcoin ransom payment. The affiliate immediately swaps the BTC for Monero using an instant-exchange service, holds the funds for several weeks, then swaps the Monero back into Bitcoin and deposits it at a mainstream exchange. Which laundering technique does this scenario illustrate?

A) Structuring
B) Chain-hopping
C) Peel chain
D) Layering via mixer

---

**Q34.** Blockchain analysts observe that proceeds from darknet market vendor sales are frequently deposited into wallet clusters that ultimately settle inside the address space of a single large, licensed exchange, despite the vendor never completing that exchange's own KYC process. Which type of service is most likely facilitating this cash-out?

A) Nested exchange
B) Decentralized exchange (DEX)
C) Mixer
D) Lending protocol

---

**Q35.** An attacker steals funds from a DeFi protocol exploit. Analysts trace the stolen funds through a rapid sequence of more than 50 wallets, where at each hop the vast majority of the balance is forwarded to the next wallet and only a small amount is split off, until the funds reach a mixing service. Which laundering technique does this pattern describe?

A) Peel chain
B) Structuring
C) Chain-hopping
D) Nested exchange placement

---

**Q36.** Which of the following best describes a terrorism-financing typology commonly identified through blockchain analysis?

A) A single large transfer sent directly from a wallet already sanctioned by OFAC
B) Ransomware proceeds converted immediately into a privacy coin
C) Token liquidity removed from a DEX pool shortly after launch
D) Numerous small donations solicited via social media and messaging apps, consolidated into a single wallet before cash-out

---

**Q37.** A user intends to send funds to an address they used previously. They copy what appears to be that same address from their wallet's transaction history, but the funds are instead sent to an attacker-controlled address that shares identical first and last characters with the legitimate one. Which typology does this describe?

A) Address poisoning
B) Pig butchering
C) SIM-swapping
D) Rug pull

---

**Q38.** An elderly investor is contacted online by someone who spends several months building a trusted personal relationship before introducing a 'can't-lose' crypto trading platform. The investor deposits crypto in increasing amounts, watches fabricated profits accumulate on a slick dashboard, and is eventually told to pay a 'tax' or 'release fee' before any withdrawal is processed. Which illicit-activity typology does this MOST closely describe?

A) Classic Ponzi scheme
B) Pig butchering scam
C) Rug pull
D) Ransomware extortion

---

**Q39.** Investigators trace stolen funds moving from Bitcoin to Ethereum to Litecoin through a series of swap services and cross-chain bridges, specifically to break the transaction trail across different blockchains. Which laundering technique is this?

A) Peel chain
B) Smurfing
C) Address poisoning
D) Chain hopping

---

**Q40.** Funds stolen in a major exchange hack are routed through a decentralized cross-chain bridge, converted into several different cryptocurrencies, spread across many unhosted wallets, and finally consolidated at a nested exchange service known for weak KYC controls. This layered, high-volume laundering pattern is MOST consistent with which typology?

A) State-sponsored hack-proceeds laundering (e.g., DPRK-linked operations)
B) Darknet market vendor cash-out
C) Rug pull liquidity drain
D) Terrorism financing via small-dollar crowdfunding

---

**Q41.** A wallet receives 50 BTC. At each subsequent hop, it sends 49 BTC of 'change' to a newly generated address and peels off a small 1 BTC output to a separate destination, repeating this exact pattern across 15 sequential hops before the final change address deposits into an exchange. Which obfuscation technique is being used?

A) Peel chain
B) CoinJoin mixing
C) Chain hopping
D) Nested exchange layering

---

**Q42.** During due diligence, an investigator finds that a counterparty VASP address receives high volumes from other exchanges, has no independent regulatory registration, and ultimately settles all customer withdrawals through its parent exchange's hot wallet. How should this counterparty be classified for risk purposes?

A) P2P exchange
B) DeFi protocol
C) Nested exchange
D) Mixing service

---

**Q43.** An analyst is preparing investigation notes to escalate a suspicious fund flow for potential SAR filing. Which piece of evidence is essential so that another analyst could independently reproduce and verify the traced fund flow?

A) The analyst's subjective risk score for the wallet
B) The analyst's personal notes summarizing the suspected intent
C) Transaction hashes (TXIDs) and the specific addresses in the fund flow
D) A screenshot of the wallet's current USD balance

---

**Q44.** A wallet has never transacted directly with a sanctioned entity, but received funds from Wallet B, which itself received funds from a sanctioned wallet two hops earlier. How is this wallet's exposure to the sanctioned entity classified?

A) Direct exposure
B) Indirect exposure
C) Zero exposure
D) Category exposure

---

**Q45.** An investigation traces stolen funds from a sanctioned hacking group through a mixing service, after which the outputs are deposited into a compliant, licensed exchange. Under a risk-based KYT approach, how should the exchange treat these incoming deposits?

A) Ignore them, since the mixer breaks the on-chain link to the sanctioned entity for compliance purposes
B) Automatically block the deposit only if the exact incoming TXID matches a sanctioned wallet address
C) Treat the deposits as high risk and subject them to enhanced due diligence and investigation
D) Rely solely on the customer's self-attestation regarding the source of funds

---

