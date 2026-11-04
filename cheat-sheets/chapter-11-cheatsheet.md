## Chapter 11 Cheat Sheet: Tracing, Wallet Risk Scoring, Documentation

### SAR Filing Timeline
| Scenario | Deadline |
|---|---|
| Suspect identified | 30 calendar days from initial determination |
| No suspect identified | Extendable to 60 days total (extra 30-day allowance) |
| SAR/support doc retention | 5 years from filing date |
| OFAC blocking report | Within 10 business days of freeze |

### SAR Dollar Thresholds
| Institution Type | Threshold (suspect known) | Threshold (no suspect) |
|---|---|---|
| Depository institution | $5,000 | $25,000 |
| MSB | $2,000 | $2,000 |

### Wallet Risk Exposure Types
| Factor | Definition | Scoring Note |
|---|---|---|
| Sanctions exposure | Contact with OFAC SDN address | Weighted by hop distance + % volume |
| Darknet exposure | Contact with marketplace/vendor address | Same weighting logic |
| Mixer exposure | Contact with tumbling/mixing service | Often raises composite score independent of amount |
| Direct exposure | Wallet transacts straight with illicit address | Highest weight |
| Indirect exposure | Illicit funds arrive via intermediary hops | Decays with hop distance, still material |
| Jurisdiction risk | Counterparty located in high-risk/non-cooperative jurisdiction | Additive factor, not standalone trigger |

### Investigation Lifecycle
1. Lead intake
2. Scoping (define question, gather KYC/on-chain data)
3. Fund-flow tracing (hop-by-hop, hash-documented)
4. Wallet risk scoring (aggregate sanctions/darknet/mixer/jurisdiction factors)
5. Documentation (narrative + evidence package)
6. Disposition (file SAR / close as non-suspicious)
7. Law enforcement referral (if warranted)

### Fund-Flow Narrative — Required Elements (the 5 W's)
- **Who**: parties/wallets involved
- **What**: nature of the suspicious activity
- **When**: chronological timestamps per hop
- **Where**: addresses, exchanges, jurisdictions
- **Why**: rationale for suspicion, tied to risk-scoring factors

### Chain of Custody Checklist
- Transaction hashes recorded
- Timestamped screenshots captured at time of analysis
- Hash-verified data export of full trace
- Documented tracing methodology and tools used
- Analyst attestation/sign-off

### Compliance ↔ Law Enforcement Handoff Points
- Grand jury subpoena received
- Formal law enforcement request for underlying records
- SAR shared under safe-harbor provision (SAR itself stays confidential — no tipping off the subject)

### Common Exam Traps
- Treating indirect exposure the same as direct exposure (over-scoring)
- Confusing the 30-day vs. 60-day SAR deadlines
- Assuming public blockchain data doesn't need to be independently captured/preserved
- Believing SAR filing eliminates the need for a separate OFAC blocking report when SDN exposure is confirmed
