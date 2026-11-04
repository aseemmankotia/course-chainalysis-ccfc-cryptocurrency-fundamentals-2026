## Chapter 7: AML/CFT Obligations, VASP Requirements, and the FATF Travel Rule — Practice Questions

**Q1.** A VASP based in Country A processes a virtual asset transfer of $2,500 to a VASP in Country B. Country A has fully implemented the FATF Travel Rule; Country B has not yet passed enabling legislation. The originating VASP collects and transmits the required originator and beneficiary information, but the receiving VASP has no legal obligation to screen or retain it. What is this scenario an example of?

A) The sunrise issue
B) A sanctions violation under OFAC jurisdiction
C) A structuring violation under AML law
D) A failure of the risk-based approach

<details>
<summary>Answer</summary>

**Correct: A**

The sunrise issue refers to the regulatory gap created when jurisdictions implement FATF Travel Rule requirements at different times, leaving inconsistent obligations between counterparty VASPs.

**Why the others are wrong:**
- No sanctioned party or jurisdiction is indicated; this isn't an OFAC matter.
- Structuring involves deliberately breaking transactions to avoid reporting thresholds, not a jurisdictional implementation gap.
- The risk-based approach concerns internal program design and resource allocation, not cross-border legal asymmetry.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A crypto exchange determines that customers using privacy coins and mixing services present higher money laundering risk than customers making routine BTC purchases, and applies enhanced due diligence only to the higher-risk group. This is an example of:

A) The Travel Rule
B) CFT-specific screening
C) A risk-based approach to AML program design
D) Sunrise issue mitigation

<details>
<summary>Answer</summary>

**Correct: C**

A risk-based approach allocates compliance resources (EDD, monitoring intensity) proportionally to assessed customer, product, and geographic risk rather than applying uniform controls to all customers.

**Why the others are wrong:**
- The Travel Rule governs originator/beneficiary information sharing between VASPs, not internal risk tiering.
- CFT screening specifically targets terrorism financing indicators, not general risk segmentation.
- Sunrise issue mitigation addresses jurisdictional implementation gaps, not internal customer risk scoring.

</details>

---

**Q3.** A company operates a platform that only provides non-custodial software wallets, never takes control of users' private keys, and does not facilitate any exchange or transfer on behalf of customers. Under the FATF VASP definition, is this company a VASP?

A) Yes, because it deals in virtual assets
B) No, because it does not conduct any of the defined VASP activities on behalf of another person
C) Yes, because all wallet providers are automatically VASPs
D) No, because non-custodial wallets are exempt by statute in every jurisdiction

<details>
<summary>Answer</summary>

**Correct: B**

FATF's VASP definition requires conducting specified activities (exchange, transfer, safekeeping/administration, or participation in issuer offerings) as a business on behalf of another person. A purely non-custodial software provider that never acts on a customer's behalf does not meet this test.

**Why the others are wrong:**
- Merely 'dealing in' virtual assets is not the FATF standard; the activity must be conducted on behalf of another.
- Not all wallet providers are VASPs — custody and on-behalf-of activity are the determining factors.
- There is no universal statutory exemption; the answer rests on the FATF activity-based definition, not blanket carve-outs.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which international body issued the standard commonly known as 'Recommendation 16' that extended traditional wire-transfer information-sharing obligations to virtual asset transfers?

A) FinCEN
B) OFAC
C) FATF
D) The Basel Committee

<details>
<summary>Answer</summary>

**Correct: C**

FATF (Financial Action Task Force) issues the Recommendations, including Recommendation 16 (the Travel Rule), and extended it to virtual assets and VASPs through its 2019 Interpretive Note.

**Why the others are wrong:**
- FinCEN is a US Treasury bureau that implements and enforces AML rules domestically; it does not issue the international FATF standards.
- OFAC administers US sanctions programs and is unrelated to issuing the Travel Rule standard.
- The Basel Committee focuses on international banking prudential standards, not AML/CFT recommendations.

</details>

---

**Q5.** A US-based VASP identifies that a customer's wallet address appears on a published sanctions list. Which US body's list and enforcement authority is directly implicated?

A) FinCEN
B) OFAC
C) FATF
D) SEC

<details>
<summary>Answer</summary>

**Correct: B**

OFAC (Office of Foreign Assets Control) administers and enforces US economic sanctions, including the SDN List, and has directly sanctioned specific virtual asset wallet addresses.

**Why the others are wrong:**
- FinCEN administers the Bank Secrecy Act and AML recordkeeping/reporting rules but does not maintain the sanctions list itself.
- FATF sets international AML/CFT standards but has no enforcement authority or sanctions list.
- The SEC regulates securities markets and is not the relevant authority for sanctions screening.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Under FATF's Travel Rule guidance for virtual asset transfers, at what threshold amount does the full originator and beneficiary information requirement generally apply?

A) USD/EUR 250
B) USD/EUR 3,000
C) USD/EUR 10,000
D) USD/EUR 1,000

<details>
<summary>Answer</summary>

**Correct: D**

FATF's standard sets the Travel Rule threshold at USD/EUR 1,000 for requiring full originator and beneficiary information; below this, a reduced information set is permitted.

**Why the others are wrong:**
- $250 is not a recognized FATF threshold figure.
- $3,000 is the threshold historically used under the US Bank Secrecy Act's Recordkeeping/Travel Rule for money transmitters, not the FATF international standard — a common point of confusion.
- $10,000 is the US currency transaction reporting (CTR) threshold, unrelated to the Travel Rule information-sharing requirement.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A compliance officer is asked to distinguish AML from CFT for a training deck. Which statement most accurately captures the distinction?

A) AML and CFT are identical programs required by the same statute with no meaningful difference
B) AML addresses concealment of proceeds from criminal activity; CFT addresses funds intended to support terrorism, which may originate from entirely legitimate sources
C) AML only applies to banks while CFT only applies to VASPs
D) CFT is a subset of AML that only covers large cash transactions

<details>
<summary>Answer</summary>

**Correct: B**

AML targets laundering proceeds of crime through placement/layering/integration; CFT targets financing of terrorism, where source funds can be legitimately obtained but the concern is their end use. This is the core conceptual distinction the exam tests.

**Why the others are wrong:**
- While often bundled together in 'AML/CFT' programs and frameworks, the underlying objectives and predicate concerns differ.
- Both AML and CFT obligations apply broadly across financial institutions and VASPs, not segmented by entity type.
- CFT is not defined by transaction size; it concerns the destination/purpose of funds regardless of amount.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** A VASP wants to design a compliant Travel Rule solution for cross-border transfers. Given inconsistent global implementation timelines, which approach BEST addresses the sunrise issue while remaining compliant in its home jurisdiction?

A) Collect and retain required originator/beneficiary information per home-jurisdiction rules, apply risk-based controls (e.g., enhanced monitoring or restricted counterparties) for transfers to VASPs in jurisdictions without reciprocal obligations
B) Refuse to collect any originator/beneficiary data until every counterparty jurisdiction has implemented the rule
C) Only apply the Travel Rule to transfers above $50,000
D) Rely solely on OFAC list screening in place of Travel Rule data collection

<details>
<summary>Answer</summary>

**Correct: A**

Best practice is to meet home-jurisdiction obligations regardless of counterparty jurisdiction maturity, and use a risk-based approach (enhanced due diligence, counterparty restrictions) to manage exposure where receiving VASPs cannot yet reciprocate — directly addressing the sunrise gap without halting compliant operations.

**Why the others are wrong:**
- Refusing to collect data entirely would violate the VASP's own home-jurisdiction Travel Rule obligations.
- There is no such arbitrary threshold in FATF or typical national Travel Rule frameworks; this invents a nonexistent rule.
- OFAC screening addresses sanctions risk only and does not substitute for the distinct Travel Rule information-sharing obligation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

