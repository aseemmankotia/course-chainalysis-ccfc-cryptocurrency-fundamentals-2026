## Chapter 8 Cheat Sheet: KYC/CDD, KYT, and the Regulatory Landscape

### Due Diligence Tiers
| Tier | Applies To | Requirements |
|---|---|---|
| Simplified (SDD) | Low-risk, capped, domestic-only accounts | Minimal identity data |
| Standard (CDD) | Baseline for all customers | Identity, address, DOB verification |
| Enhanced (EDD) | High-risk: PEPs, high-risk jurisdictions, unusual volume/patterns | Source-of-funds verification, ongoing enhanced monitoring |

**Exam note:** EDD is triggered by risk factors, not customer type (retail vs institutional).

### KYC vs KYT
| | KYC | KYT |
|---|---|---|
| Timing | Onboarding (point-in-time) | Continuous / real-time |
| Focus | Who the customer is | What the transaction is doing |
| Detects | Identity fraud | Structuring, layering, mixer/sanctioned exposure |

### Regulator Roles (Conceptual)
| Body | Role | Power |
|---|---|---|
| FinCEN | U.S. Treasury bureau; enforces BSA; SAR/CTR filing | Domestic enforcement |
| OFAC | Administers sanctions; maintains SDN list | Domestic enforcement |
| FATF | Global AML/CFT standard-setter (e.g., Travel Rule, Rec. 16) | No direct enforcement — sets standards for members to adopt |

**Common mistake:** Choosing FATF as an enforcement body — it sets standards only; FinCEN/OFAC enforce.

### Key Numbers
| Item | Value |
|---|---|
| CTR threshold | $10,000 cash/day |
| SAR threshold (typical) | $5,000 suspected illicit activity |
| U.S. Travel Rule recordkeeping threshold | $3,000 |
| FATF Travel Rule origin | Recommendation 16 |

### EDD Triggers Checklist
- PEP (politically exposed person)
- High-risk jurisdiction
- Unusual transaction volume/velocity
- Cash-intensive business
- Private banking / high-net-worth relationship

### Sanctions Screening Flow
1. Screen name/wallet against OFAC SDN list
2. Partial match → manual review (do NOT auto-reject or auto-file SAR)
3. Confirmed match → block transaction, file required reports, escalate

**Common mistake:** Treating any name-match hit as a confirmed positive without human review.

### KYT Risk Scoring Inputs
- Transaction size and velocity
- Counterparty risk (mixer, darknet market, sanctioned address exposure)
- Geographic/jurisdictional risk
- Deviation from customer's baseline behavior

**Exam note:** Irrelevant inputs (social media, marketing prefs) are common distractors — exclude them.
