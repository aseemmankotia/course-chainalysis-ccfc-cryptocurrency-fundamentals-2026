## Chapter 8: KYC/CDD, Know Your Transaction (KYT), and the Regulatory Landscape — Practice Questions

**Q1.** A crypto exchange onboards a customer who is later identified as a senior government official from a foreign country. Which action should the compliance team take?

A) Apply Enhanced Due Diligence (EDD) due to the customer's PEP status
B) Continue with standard CDD since the account has had no suspicious activity
C) File a Currency Transaction Report immediately regardless of transaction amount
D) Terminate the account immediately without further review

<details>
<summary>Answer</summary>

**Correct: A**

PEP status is a classic EDD trigger requiring source-of-funds verification and ongoing enhanced monitoring.

**Why the others are wrong:**
- Standard CDD is insufficient risk mitigation for a PEP profile.
- CTR filing is triggered by cash transaction thresholds, not PEP status alone.
- Account termination is not required simply due to PEP designation; EDD is the correct first response.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An on-chain monitoring system flags a customer wallet for receiving multiple small deposits from different addresses within minutes, followed by a single large withdrawal to an unhosted wallet. What compliance concept does this scenario illustrate?

A) Know Your Transaction (KYT) detecting a potential structuring/layering pattern
B) Know Your Customer identity verification failure
C) A routine Currency Transaction Report filing
D) A FATF Travel Rule violation

<details>
<summary>Answer</summary>

**Correct: A**

KYT is designed to detect real-time behavioral patterns like structuring and layering at the transaction level.

**Why the others are wrong:**
- KYC concerns identity verification at onboarding, not transaction pattern analysis.
- CTR filing applies only to specific cash thresholds, not this behavioral pattern.
- The Travel Rule concerns information-sharing on transfers, not detection of the layering pattern itself.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Which U.S. government entity maintains the Specially Designated Nationals (SDN) list used for sanctions screening?

A) FinCEN
B) OFAC
C) FATF
D) SEC

<details>
<summary>Answer</summary>

**Correct: B**

OFAC administers U.S. sanctions programs and publishes the SDN list.

**Why the others are wrong:**
- FinCEN enforces BSA/AML reporting obligations (SARs, CTRs), not the sanctions list.
- FATF is an international standard-setting body with no list-maintenance or enforcement authority.
- The SEC regulates securities markets, unrelated to sanctions screening.

</details>

---

**Q4.** A VASP's risk-based approach assigns customer due diligence tiers based on risk level. A customer opening a low-value account with a capped transaction limit and no cross-border activity would typically fall under which tier?

A) Enhanced Due Diligence (EDD)
B) No due diligence required
C) Standard due diligence with mandatory PEP screening
D) Simplified Due Diligence (SDD)

<details>
<summary>Answer</summary>

**Correct: D**

Low-risk, capped, domestic-only profiles qualify for the simplified CDD tier requiring minimal customer information.

**Why the others are wrong:**
- EDD is reserved for high-risk customers, not low-risk capped accounts.
- Some level of due diligence is always required under AML frameworks; none is not an option.
- Mandatory PEP screening as a baked-in standard-tier requirement overstates what a low-risk profile needs; PEP screening is normally triggered by EDD, not applied universally.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** During onboarding, a customer's name partially matches an entry on the OFAC SDN list. What is the BEST next step for the compliance team?

A) Automatically reject the customer with no further review
B) Ignore the match since it may be a common name
C) File a Suspicious Activity Report immediately without verification
D) Conduct a manual review to confirm or rule out a true match before taking action

<details>
<summary>Answer</summary>

**Correct: D**

Screening tools generate potential matches that require human review to confirm true positives before any rejection or reporting action.

**Why the others are wrong:**
- Automatic rejection without verification risks incorrectly denying legitimate customers due to false positives.
- Ignoring a potential sanctions match violates compliance screening obligations.
- SAR filing should follow a confirmed suspicious finding, not an unverified name match.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which organization is responsible for setting the global standard requiring VASPs to share originator and beneficiary information on virtual asset transfers (the 'Travel Rule')?

A) FATF
B) FinCEN
C) OFAC
D) IRS

<details>
<summary>Answer</summary>

**Correct: A**

FATF Recommendation 16 established the international Travel Rule standard, which member jurisdictions implement into national law.

**Why the others are wrong:**
- FinCEN implements and enforces the rule domestically in the U.S. but did not create the global standard.
- OFAC administers sanctions programs, unrelated to the Travel Rule.
- The IRS handles tax reporting, unrelated to the Travel Rule.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** What is the primary difference between standard Customer Due Diligence (CDD) and Enhanced Due Diligence (EDD)?

A) CDD is optional while EDD is mandatory for all customers
B) EDD requires deeper investigation, such as source-of-funds verification and ongoing monitoring, applied to higher-risk customers
C) EDD applies only to institutional customers, CDD only to retail
D) CDD is performed by regulators, EDD is performed by the institution

<details>
<summary>Answer</summary>

**Correct: B**

EDD adds deeper scrutiny layers for higher-risk customer profiles beyond baseline CDD identity checks.

**Why the others are wrong:**
- CDD is a mandatory baseline requirement for nearly all customers, not optional.
- The CDD/EDD distinction is risk-based, not strictly tied to institutional vs. retail customer type.
- Both CDD and EDD are performed by the regulated institution, not by regulators.

</details>

---

**Q8.** A transaction monitoring system generates a risk score for an alert. Which combination of inputs is MOST relevant to that score?

A) Customer's favorite cryptocurrency and account creation date only
B) Customer's marketing preferences and app login frequency
C) Customer's social media activity only
D) Transaction size/velocity, counterparty risk (e.g., mixer or sanctioned address exposure), and geographic risk

<details>
<summary>Answer</summary>

**Correct: D**

These are core risk-scoring factors used by KYT systems to flag anomalous or high-risk transactions.

**Why the others are wrong:**
- Account creation date alone provides little transactional risk signal.
- Marketing preferences are irrelevant to AML risk scoring.
- Social media activity alone is not a standard AML risk input.

</details>

---

