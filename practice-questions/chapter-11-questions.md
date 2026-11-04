## Chapter 11: Tracing Funds End to End, Wallet Risk Scoring, and Documenting Findings — Practice Questions

**Q1.** During fund-flow tracing, an analyst finds that a customer's wallet sent funds four hops downstream to an address currently on OFAC's SDN list. What is the BEST immediate action?

A) Close the account quietly and take no further action
B) Wait for a subpoena from law enforcement before doing anything
C) Block/freeze the transaction, file an OFAC blocking report within the required window, and file a SAR documenting the sanctions nexus
D) Monitor the account for 90 days before deciding whether to act

<details>
<summary>Answer</summary>

**Correct: C**

A confirmed SDN nexus triggers dual obligations: OFAC blocking/reporting and a BSA SAR — these are parallel, not alternative, requirements.

**Why the others are wrong:**
- Closing the account does not satisfy the mandatory blocking and reporting obligations under OFAC regulations
- Compliance obligations are proactive; the institution cannot wait for a subpoena to act on a confirmed sanctions hit
- A 90-day monitoring delay conflicts with the fixed OFAC blocking-report deadline and SAR filing deadlines

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A wallet received 3% of its total inbound volume, across three intermediary hops, from a known darknet marketplace address. How should this exposure be scored?

A) Identical to direct darknet exposure — score at maximum severity
B) As indirect exposure — weighted lower due to hop distance and volume percentage, but still flagged for review
C) Zero risk, since the wallet never transacted directly with the marketplace
D) Automatically escalate to a mandatory SAR regardless of dollar amount or context

<details>
<summary>Answer</summary>

**Correct: B**

Risk-scoring models weight exposure by both hop distance (direct vs. indirect) and proportion of volume — indirect, low-percentage exposure is material but scored lower than direct exposure.

**Why the others are wrong:**
- Treating indirect exposure identically to direct exposure inflates false positives and ignores hop-distance weighting used in real scoring models
- Indirect exposure still carries risk and must be documented, not dismissed as zero risk
- SAR filing is a disposition decision made after full risk assessment, not an automatic trigger from exposure percentage alone

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An analyst is building a case file that may eventually be referred to law enforcement. Which documentation practice BEST preserves evidentiary integrity of the blockchain trace?

A) A one-line email summary stating the final destination address
B) Timestamped screenshots, recorded transaction hashes, a hash-verified export of the full transaction path, and documented tracing methodology
C) A verbal briefing given to the compliance officer with no written record
D) Only the customer's KYC file, since the blockchain data is publicly available and doesn't need capture

<details>
<summary>Answer</summary>

**Correct: B**

Chain-of-custody standards require reproducible, tamper-evident evidence: transaction hashes, timestamps, methodology notes, and verifiable exports.

**Why the others are wrong:**
- A single summary line lacks the granular, verifiable detail needed for evidentiary use
- Verbal-only records cannot be authenticated or produced later; they fail chain-of-custody standards
- Public availability of blockchain data does not eliminate the need to capture and preserve it at the time of analysis, since data sources (mixers, exchanges) can remove or alter accessible information later

</details>

---

**Q4.** A wallet-clustering tool shows only 2% of a wallet's total inbound volume originated from an OFAC SDN address, three hops removed. Which exposure classification applies?

A) Direct sanctions exposure requiring automatic blocking
B) Darknet exposure
C) Mixer exposure
D) Indirect, low-percentage sanctions exposure requiring risk-weighted review rather than automatic blocking

<details>
<summary>Answer</summary>

**Correct: D**

Low-percentage, multi-hop contact with an SDN address is indirect exposure — it must be risk-weighted and reviewed, not automatically treated as a direct sanctions hit requiring blocking.

**Why the others are wrong:**
- Direct exposure requires the wallet to have transacted directly with the SDN address, which is not the case here
- The exposure source is a sanctioned address, not a darknet market — a different category with different scoring criteria
- Mixer exposure applies specifically to tumbling/mixing services, not a direct SDN-listed counterparty

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which factor is NOT part of standard wallet risk-scoring methodology?

A) Sanctions exposure (SDN list matches)
B) Darknet market exposure
C) The wallet interface's visual theme or branding
D) Mixer/tumbler exposure

<details>
<summary>Answer</summary>

**Correct: C**

Wallet risk scoring is based on transactional exposure factors (sanctions, darknet, mixer, jurisdiction) — cosmetic UI attributes have no bearing on risk.

**Why the others are wrong:**
- Sanctions exposure is a core, heavily tested scoring factor
- Darknet exposure is a core scoring factor for illicit marketplace connections
- Mixer exposure is a core scoring factor for obfuscation-related risk

</details>

---

**Q6.** Under BSA rules, if no suspect has been identified, what is the maximum total number of days a depository institution has to file a SAR from the date of initial detection?

A) 15 days
B) 60 days
C) 30 days
D) 90 days

<details>
<summary>Answer</summary>

**Correct: B**

The base filing window is 30 calendar days from initial determination; an additional 30-day extension is permitted when no suspect is identified, capping the total at 60 days.

**Why the others are wrong:**
- 15 days is shorter than the standard 30-day window and does not reflect BSA requirements
- 30 days is the standard window when a suspect IS identified, not the maximum extension scenario
- 90 days exceeds the regulatory maximum allowed even with the no-suspect-identified extension

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** How long must a financial institution retain a filed SAR and its supporting documentation?

A) 5 years
B) 2 years
C) 3 years
D) 7 years

<details>
<summary>Answer</summary>

**Correct: A**

BSA regulations require SARs and supporting documentation to be retained for 5 years from the date of filing.

**Why the others are wrong:**
- 2 years is shorter than the regulatory retention requirement
- 3 years is shorter than the regulatory retention requirement
- 7 years exceeds the standard BSA retention requirement (often confused with other recordkeeping rules)

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the primary purpose of documenting a fund-flow narrative within a case file?

A) To satisfy internal reporting metrics unrelated to compliance obligations
B) To create a reproducible, evidentiary record connecting the suspicious activity, transaction path, and risk factors for compliance decisions and potential legal use
C) To reduce the overall number of SARs an institution must file
D) To eliminate the need for separate wallet risk scoring

<details>
<summary>Answer</summary>

**Correct: B**

The fund-flow narrative ties together the trace, the risk factors identified, and the disposition rationale into a document that can support both internal compliance review and external referral.

**Why the others are wrong:**
- Documentation is a regulatory/evidentiary requirement, not an internal metrics exercise
- Proper documentation supports accurate SAR filing decisions; it is not designed to reduce filing volume
- The narrative complements wallet risk scoring by providing context — it does not replace the scoring process

</details>

---

