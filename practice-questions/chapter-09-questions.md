## Chapter 9: Scams, Ransomware, and Darknet Markets — Practice Questions

**Q1.** An analyst traces a wallet that received dozens of small deposits from newly-created retail wallets over several weeks. Each deposit is quickly consolidated into a hub wallet, converted to a stablecoin, and forwarded to an address associated with an OTC broker known to service scam operations. Victims report being coached via messaging apps into a fake trading platform. Which typology BEST fits this pattern?

A) Rug pull
B) Ransomware extortion
C) Darknet market vendor payout
D) Pig butchering scam

<details>
<summary>Answer</summary>

**Correct: D**

The long build-up via messaging apps, gradual small deposits from retail victims, consolidation, stablecoin conversion, and OTC broker off-ramp is the classic pig butchering fund funnel.

**Why the others are wrong:**
- Rug pull: a rug pull is a single sudden liquidity removal event from a DeFi pool, not a slow multi-victim deposit pattern.
- Ransomware extortion: ransomware involves a single ransom payment from a victim organization, not many small retail deposits.
- Darknet market vendor payout: vendor payouts come from marketplace escrow release, not retail victim onboarding via chat apps.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A newly deployed token on a decentralized exchange sees its price spike within hours due to coordinated buying. Shortly after, the deployer wallet removes all liquidity from the pool, causing the token price to collapse to near zero. What typology does this describe?

A) Ponzi scheme
B) Rug pull
C) Darknet market exit scam
D) Pig butchering scam

<details>
<summary>Answer</summary>

**Correct: B**

Removing liquidity from a DeFi pool right after a coordinated price pump is the defining on-chain signature of a rug pull.

**Why the others are wrong:**
- Ponzi scheme: Ponzi schemes pay early investors with later investors' funds; there is no liquidity pool mechanic involved.
- Darknet market exit scam: exit scams involve a marketplace operator absconding with escrowed vendor/buyer funds, not DEX liquidity.
- Pig butchering scam: this involves long-term social engineering of individual victims, not a token liquidity event.

</details>

---

**Q3.** Funds paid to a ransomware group's demand address are immediately split across several intermediary wallets, passed through a series of unrelated addresses over multiple hops, and finally deposited at an exchange under a different apparent identity. What is this pattern called and why do analysts track it?

A) Peel chaining, used to identify the original victim's payment address
B) Chain-hopping, used to obscure the link between the ransom address and the cash-out exchange
C) Vendor bonding, used to guarantee marketplace trust
D) Liquidity pooling, used to inflate token price before a rug pull

<details>
<summary>Answer</summary>

**Correct: B**

Chain-hopping across multiple intermediary wallets is the standard ransomware cash-out obfuscation technique that analysts must trace to reach the final off-ramp.

**Why the others are wrong:**
- Peel chaining describes repeatedly sending small change amounts from one wallet in a linear chain, a related but distinct laundering technique, not the multi-hop obfuscation described.
- Vendor bonding is a darknet market mechanism unrelated to ransomware cash-out.
- Liquidity pooling relates to DeFi rug pulls, not ransomware laundering.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** On-chain analysis shows a wallet receiving continuous deposits from new participants, with outgoing 'return' payments to earlier participants that are funded directly by new deposits rather than any external revenue-generating activity. Which typology does this fund flow indicate?

A) Rug pull
B) Darknet market escrow release
C) Ransomware ransom payment
D) Ponzi / high-yield investment scheme

<details>
<summary>Answer</summary>

**Correct: D**

Paying existing participants' returns directly from new participant deposits, with no external revenue source, is the defining fund-flow signature of a Ponzi/high-yield investment scheme.

**Why the others are wrong:**
- Rug pull is a single liquidity-drain event, not a continuous deposit/payout cycle.
- Darknet market escrow release is a one-time transaction tied to a completed order, not recurring investor payouts.
- Ransomware ransom payment is a one-time extortion payment, not a recurring deposit-funded payout scheme.

</details>

---

**Q5.** A darknet marketplace requires prospective vendors to lock a refundable amount of cryptocurrency with the market operator before they are permitted to list products for sale. Which mechanism does this describe?

A) Vendor bond
B) Multisig escrow
C) Finalize early (FE)
D) Liquidity pool

<details>
<summary>Answer</summary>

**Correct: A**

A vendor bond is collateral posted by a vendor to the marketplace, forfeited for rule violations, used to deter scam vendors and establish trust before listing privileges are granted.

**Why the others are wrong:**
- Multisig escrow is the transaction-level mechanism holding buyer funds until order completion, not a vendor-level trust deposit.
- Finalize early (FE) is a buyer privilege that releases escrowed funds to the vendor before order confirmation, unrelated to vendor bonding.
- Liquidity pool is a DeFi construct unrelated to darknet marketplaces.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A trusted vendor on a darknet market convinces multiple established buyers to release their escrowed funds before receiving the product, citing shipping delays. Shortly after, the vendor disappears with the released funds. Which mechanism was exploited?

A) Vendor bond forfeiture
B) Multisig 2-of-3 escrow
C) Rug pull liquidity removal
D) Finalize early (FE)

<details>
<summary>Answer</summary>

**Correct: D**

Finalize early lets the buyer instruct escrow to release funds to the vendor before the order is confirmed complete; scam vendors exploit trusted status to solicit FE from multiple buyers simultaneously before absconding.

**Why the others are wrong:**
- Vendor bond forfeiture is a penalty process enforced by the market against a vendor, not something a vendor uses to defraud buyers.
- Multisig 2-of-3 escrow, when used properly, requires two of three keys (buyer, vendor, market) to release funds and would prevent this if FE was not invoked.
- Rug pull liquidity removal is a DeFi typology unrelated to darknet market escrow.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which single on-chain indicator is MOST associated with a darknet marketplace exit scam, as opposed to normal vendor payout activity?

A) Steady, proportional outflows from the market's hot wallet to many distinct vendor-controlled addresses over time
B) Small periodic deposits from many new buyer wallets into the market's deposit addresses
C) Vendor addresses transacting exclusively with mixers before reaching an exchange
D) A sudden, large-scale outflow of nearly all funds held across the market's escrow/hot wallets to a small number of new addresses, followed by market site downtime

<details>
<summary>Answer</summary>

**Correct: D**

An exit scam is characterized by the operator draining nearly all escrowed/held funds in one large movement to a small set of new addresses, coinciding with the market going offline.

**Why the others are wrong:**
- Steady proportional vendor payouts describe normal market operation, not an exit scam.
- Small periodic buyer deposits are routine marketplace activity, not indicative of an exit scam.
- Mixer usage by vendors is common laundering behavior generally but is not the specific signature that distinguishes an exit scam from normal operations.

</details>

---

**Q8.** Why do victim-reported cases (e.g., through law enforcement complaint portals) matter significantly for typology attribution in blockchain analysis?

A) They ground-truth on-chain patterns to a confirmed real-world scam type, allowing analysts to build and validate heuristics that can then be applied to unreported, similar wallet clusters
B) They provide the exact private keys needed to seize funds directly
C) They are legally required before any blockchain analysis can be performed
D) They eliminate the need for on-chain clustering entirely

<details>
<summary>Answer</summary>

**Correct: A**

Victim reports supply the confirmed context (e.g., 'this was a romance investment scam') that lets analysts validate that a given on-chain pattern truly corresponds to a specific typology, enabling that heuristic to be applied confidently to other unreported wallets exhibiting the same pattern.

**Why the others are wrong:**
- Victim reports almost never include private keys; they provide narrative and transaction context, not cryptographic access.
- Blockchain analysis can and does occur without any victim report; reports are valuable, not mandatory, for analysis to proceed.
- Victim reports supplement, not replace, on-chain clustering — clustering is still required to trace fund flow and identify additional related addresses.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

