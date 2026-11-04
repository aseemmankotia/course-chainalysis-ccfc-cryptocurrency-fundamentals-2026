## Chapter 10 Cheat Sheet — Hacks, Sanctions Evasion, Money Laundering

### ML Stages
| Stage | What Happens | Crypto Example |
|---|---|---|
| Placement | Illicit funds first enter the system | Stolen tokens leave exploited contract/wallet |
| Layering | Obscure origin via multiple hops | Mixer, chain-hopping, peel chain |
| Integration | Funds re-enter legit economy | CEX cash-out, real estate, goods |

### Layering Techniques
| Technique | Definition | Chain Scope |
|---|---|---|
| Peel chain | Sequential UTXO splitting, small peel-offs from one large source | Single chain |
| Chain-hopping | Convert value across multiple chains/assets via bridges/DEXs | Cross-chain |
| Mixer/tumbler | Custodial/contract pooling breaks direct linkage (e.g., Tornado Cash, Blender.io) | Single chain, one hop |
| CoinJoin | Trustless multi-party merge in one Bitcoin tx (Wasabi, Samourai Whirlpool) | Bitcoin only |
| Nesting | Sub-broker hides behind one VASP account | Any |

### Sanctioned Mixers/Exchanges (know dates)
| Entity | Designated | Notes |
|---|---|---|
| Blender.io | May 2022 | First-ever sanctioned mixer; Ronin hack laundering |
| Tornado Cash | Aug 2022 | Delisted from SDN March 21, 2025 (Van Loon ruling) |
| Garantex | Apr 2022 | Russian exchange; seized by law enforcement Mar 2025 |
| Sinbad.io | Nov 2023 | Blender.io successor, Lazarus-linked |
| Bitzlato | Jan 2023 | Tied to Hydra darknet market proceeds |

### Major Hacks (fund-flow references)
| Hack | Amount | Date | Attribution | Method |
|---|---|---|---|---|
| Poly Network | $611M | Aug 2021 | Unknown/white-hat return | Contract exploit |
| Ronin Bridge | $625M | Mar 2022 | Lazarus Group (DPRK) | 5-of-9 validator key compromise |
| Harmony Bridge | $100M | Jun 2022 | Lazarus Group (DPRK) | Multisig key compromise |
| Bybit | ~$1.46B | Feb 2025 | Lazarus/TraderTraitor (DPRK) | Cold wallet signing compromise; rapid dispersal |

### Key Thresholds
| Rule | Value |
|---|---|
| FATF Travel Rule (VASP) | USD/EUR 1,000 |
| Traditional wire Travel Rule (BSA) | $3,000 |
| Cash reporting (CTR) | $10,000 |

### Post-Hack Behavioral Signature
Speed + fragmentation = rapid dispersal (funds split across many addresses within minutes/hours) → mixer → chain-hop → nested/unhosted wallet layer → attempted CEX/OTC cash-out.

### Sanctions Jurisdiction Nexus Points
U.S. person involved • U.S.-issued stablecoin • U.S.-based settlement/validator infrastructure • USD-denominated clearing — any one can trigger OFAC jurisdiction even without a direct U.S. counterparty.
