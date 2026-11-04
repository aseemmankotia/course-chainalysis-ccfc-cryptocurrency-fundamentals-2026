# Chapter 7 Cheat Sheet: AML/CFT, VASPs & the Travel Rule

## AML vs CFT
| | AML | CFT |
|---|---|---|
| Focus | Concealing proceeds of crime | Funding terrorism |
| Source of funds | Illicit | Can be entirely legitimate |
| Process stages | Placement → Layering → Integration | Collection → Transfer → Use |
| Common overlap | Both bundled in 'AML/CFT' programs, SAR filing, KYC |

## VASP Definition (FATF)
A VASP conducts, **as a business, on behalf of another person**, one or more of:
1. Exchange between virtual assets and fiat currencies
2. Exchange between one or more forms of virtual assets
3. Transfer of virtual assets
4. Safekeeping/administration of virtual assets or instruments enabling control
5. Participation in/provision of financial services related to an issuer's offer/sale of a virtual asset

**Not a VASP:** pure non-custodial software wallet providers, protocol developers, hardware manufacturers (no on-behalf-of activity).

## Travel Rule (FATF Recommendation 16 + 2019 Interpretive Note)
| Threshold | Info required |
|---|---|
| Below USD/EUR 1,000 | Originator name, account number, VA wallet address |
| Above USD/EUR 1,000 | + originator physical address/national ID/DOB+POB + beneficiary name & account number |

**US-specific:** FinCEN Recordkeeping/Travel Rule threshold = **$3,000** (31 CFR 1010.410) — do not conflate with FATF's $1,000 figure.

## Sunrise Issue
Gap created when counterparty jurisdictions implement Travel Rule at different times. Mitigate via: home-jurisdiction compliance regardless of counterparty status + risk-based controls (EDD, counterparty restrictions) for non-compliant corridors.

## Risk-Based Approach (RBA)
Allocate controls by risk factor:
- Customer risk (PEPs, high-risk industries)
- Product/service risk (privacy coins, mixers)
- Geographic risk (FATF grey/black-listed jurisdictions)
- Delivery channel risk (non-face-to-face onboarding)

## Regulatory Bodies
| Body | Role | Enforcement? |
|---|---|---|
| FATF | Sets international AML/CFT standards (soft law), mutual evaluations, grey/black lists | No direct enforcement |
| FinCEN | US Treasury bureau; administers BSA, MSB registration, SARs | Yes (US) |
| OFAC | Administers/enforces US sanctions (SDN List), strict liability | Yes (US) |

## Exam Traps
- FATF $1,000 vs FinCEN $3,000 — commonly confused thresholds
- Non-custodial ≠ automatic VASP status — activity-based test matters
- AML ≠ CFT — don't treat as interchangeable on exam questions
- Sunrise issue is about *jurisdictional timing gaps*, not sanctions or structuring
