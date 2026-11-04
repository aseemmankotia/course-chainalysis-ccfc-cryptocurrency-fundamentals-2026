## Chapter 10: Stolen Funds, Hacks, Sanctions Evasion, and Money-Laundering Patterns — Practice Questions

**Q1.** A DeFi protocol is exploited via a reentrancy bug. The stolen tokens are bridged to a second chain, run through a non-custodial mixer, then deposited at a centralized exchange under a freshly created account. Which money-laundering stage does the mixer step represent?

A) Placement
B) Integration
C) Structuring
D) Layering

<details>
<summary>Answer</summary>

**Correct: D**

Layering is the stage where funds are moved through multiple transactions/instruments (mixers, bridges, chain-hopping) specifically to obscure the original source. Placement already occurred when the exploit moved funds out of the protocol; the exchange deposit under a new identity is the integration attempt.

**Why the others are wrong:**
- Placement is the initial introduction of illicit funds into the financial system — that already happened at the moment of the exploit/theft, not at the mixer step.
- Integration is the final stage where laundered funds re-enter the legitimate economy (e.g., cashed out as fiat or converted to assets) — that's the exchange deposit, not the mixer.
- Structuring is a placement-stage technique (breaking amounts to avoid reporting thresholds), not a layering technique like mixing.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** Within roughly 30 minutes of the February 2025 exchange hack attributed to a North Korea-linked group (~$1.46B stolen), investigators observed the stolen ETH being split across hundreds of newly created addresses almost immediately. What is this specific typology called?

A) Chain-hopping
B) Structuring
C) Rapid dispersal
D) Nesting

<details>
<summary>Answer</summary>

**Correct: C**

Rapid dispersal is the immediate post-hack behavior of fragmenting stolen funds across many addresses within minutes to hours, before exchanges/law enforcement can flag or freeze the deposit address, complicating clustering and tracing.

**Why the others are wrong:**
- Chain-hopping refers to moving value across different blockchains/assets, not simply fragmenting addresses on the same chain.
- Structuring is a fiat/AML term for breaking transactions to stay under reporting thresholds, not a crypto-native fragmentation technique.
- Nesting describes an unregistered service operating inside a licensed VASP's account, unrelated to address fragmentation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Which OFAC-sanctioned virtual currency mixer was the first ever designated (May 2022) and was used to launder a portion of the proceeds from the March 2022 Ronin Bridge hack?

A) Tornado Cash
B) Blender.io
C) Sinbad.io
D) ChipMixer

<details>
<summary>Answer</summary>

**Correct: B**

Blender.io was designated by OFAC in May 2022 as the first-ever sanctioned virtual currency mixer, specifically cited for laundering funds stolen in the Ronin Bridge hack.

**Why the others are wrong:**
- Tornado Cash was designated later (August 2022) and became the primary mixer Lazarus Group used after Blender.io was sanctioned.
- Sinbad.io was designated in November 2023, well after the Ronin hack, as a suspected successor to Blender.io.
- ChipMixer was seized/disrupted by law enforcement (2023) but was not the mixer specifically tied to the Ronin hack laundering.

</details>

---

**Q4.** An OFAC designation in November 2023 targeted a Bitcoin mixer believed to be a rebranded successor to a previously sanctioned mixing service, heavily used by a North Korea-linked hacking group. Which service was sanctioned?

A) Wasabi Wallet
B) Sinbad.io
C) Samourai Whirlpool
D) Garantex

<details>
<summary>Answer</summary>

**Correct: B**

Sinbad.io was sanctioned by OFAC on November 29, 2023, identified as functioning as a likely successor to Blender.io and used extensively by the Lazarus Group to launder bridge-hack proceeds.

**Why the others are wrong:**
- Wasabi Wallet is a Bitcoin CoinJoin coordinator, not an OFAC-sanctioned custodial mixer, and is not tied to this designation.
- Samourai Whirlpool is also a CoinJoin implementation; its founders were criminally charged (2024) but it was not OFAC-sanctioned as a Lazarus successor mixer.
- Garantex was sanctioned (2022) as a Russian exchange linked to ransomware/darknet proceeds, not as a Bitcoin mixer or Lazarus successor service.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Under FATF Recommendation 16 (the Travel Rule), at what threshold must VASPs collect and transmit originator and beneficiary information for a virtual asset transfer?

A) $1,000
B) $250
C) $3,000
D) $10,000

<details>
<summary>Answer</summary>

**Correct: A**

FATF Recommendation 16 sets the VASP Travel Rule threshold at USD/EUR 1,000 for collecting and transmitting originator/beneficiary data.

**Why the others are wrong:**
- $250 is not a recognized FATF or common jurisdictional threshold for the Travel Rule.
- $3,000 is the traditional wire-transfer Travel Rule threshold under the Bank Secrecy Act framework, not the FATF VASP threshold.
- $10,000 is the cash transaction reporting threshold (e.g., CTR/Form 8300), unrelated to the VASP Travel Rule.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A licensed exchange (Exchange A) discovers that one of its corporate accounts is actually an unregistered broker letting hundreds of its own unverified customers trade through that single account, effectively accessing Exchange A's liquidity without Exchange A ever KYC'ing the end users. What is the PRIMARY compliance risk this 'nested service' arrangement creates?

A) Higher trading fees for Exchange A
B) Loss of visibility into the true beneficial owners/originators of transactions
C) Automatic triggering of a Travel Rule exemption
D) Reduced blockchain confirmation times

<details>
<summary>Answer</summary>

**Correct: B**

Nesting hides the true originators/beneficiaries behind a single verified account, meaning the licensed VASP's KYC and transaction monitoring only 'sees' the nested broker, not the actual underlying customers — a major sanctions-screening and AML blind spot.

**Why the others are wrong:**
- Trading fees are a commercial/business consideration, not the compliance risk being tested.
- Nesting does not exempt anyone from the Travel Rule — it actually undermines Travel Rule compliance by obscuring true parties.
- Confirmation times are a blockchain-layer technical matter unrelated to nested-service AML risk.

</details>

---

**Q7.** Which term describes moving stolen assets sequentially across multiple different blockchains and asset types (e.g., ETH → BTC via a bridge/DEX aggregator → converted again into a privacy coin) specifically to break the on-chain trace?

A) Chain-hopping
B) Peel chain
C) CoinJoin
D) Structuring

<details>
<summary>Answer</summary>

**Correct: A**

Chain-hopping is the layering technique of converting/transferring value across multiple different chains and asset types via bridges, swaps, or DEX aggregators, forcing investigators to reconstruct the trail across disparate ledgers.

**Why the others are wrong:**
- A peel chain is a same-chain sequential pattern of splitting off small amounts from one large UTXO into successive new addresses — it does not involve crossing chains or asset types.
- CoinJoin is a same-chain (typically Bitcoin) transaction-merging obfuscation technique among multiple participants, not a cross-chain technique.
- Structuring refers to breaking transaction amounts to evade reporting thresholds, not moving across chains/assets.

</details>

---

**Q8.** A foreign-based exchange with no U.S. offices and no direct U.S. customers processes a transfer of a USD-pegged stablecoin issued by a U.S. company, and settlement routes through U.S.-based validator/blockchain infrastructure. Under what basis could OFAC still assert jurisdiction over this transaction?

A) All cryptocurrency is automatically subject to U.S. jurisdiction regardless of nexus
B) Because the exchange must register with FinCEN regardless of any U.S. nexus
C) Because a U.S. nexus exists through the U.S. stablecoin issuer and/or U.S.-based settlement infrastructure
D) OFAC has no jurisdiction unless a U.S. person is directly a party to the trade

<details>
<summary>Answer</summary>

**Correct: C**

OFAC jurisdiction attaches through U.S. nexus points — a U.S.-incorporated stablecoin issuer, U.S. dollar-denominated clearing, or U.S.-based technology/infrastructure touching the transaction — even without a direct U.S. counterparty to the trade.

**Why the others are wrong:**
- Crypto is not automatically U.S. jurisdiction by default; jurisdiction depends on demonstrable U.S. nexus, not the mere existence of a blockchain.
- FinCEN registration requirements are a separate BSA/MSB question and don't establish OFAC sanctions jurisdiction on their own.
- OFAC jurisdiction can attach via U.S. nexus points (issuer, infrastructure, dollar-clearing) even absent a directly transacting U.S. person — this is the exact scenario the question tests.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

