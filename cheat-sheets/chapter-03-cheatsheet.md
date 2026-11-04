## Chapter 3 Cheat Sheet: Keys, Addresses, UTXO vs Account

### Key Pair Roles
| Key | Role | Shared? |
|---|---|---|
| Private key | Signs transactions | NEVER shared |
| Public key | Verifies signatures; source of address | Derived, can be shared |
| Address | Hash of public key; receives funds | Publicly shared |

**Derivation flow:** Private key → (EC multiplication, secp256k1) → Public key → (hash function) → Address

### Bitcoin Address Formats
| Format | Prefix | Version/Encoding | Introduced |
|---|---|---|---|
| P2PKH (legacy) | `1` | Base58Check, version 0x00, HASH160(pubkey) | Original (2009) |
| P2SH | `3` | Base58Check, version 0x05, HASH160(script) | BIP-16 (2012) |
| Bech32 (P2WPKH, SegWit v0) | `bc1q` | Bech32, witness v0 | BIP-173 (2017) |
| Bech32m (Taproot, SegWit v1) | `bc1p` | Bech32m, witness v1 | BIP-350 (2021) |

### Ethereum Address
- Single format: `0x` + 40 hex chars (20 bytes)
- Derivation: Keccak-256(uncompressed pubkey)[last 20 bytes]
- EIP-55: mixed-case checksum for typo detection (not a separate address type)

### UTXO Model (Bitcoin)
- Transactions consume existing UTXOs as **inputs**
- Create new UTXOs as **outputs**
- Leftover value returned as a **change output**
- No account balances — wallet balance = sum of owned UTXOs
- Enables parallel validation; harder to track 'account state' directly

### Account Model (Ethereum)
- Global state = balances + storage per address (Merkle Patricia trie)
- Each transaction updates sender/receiver balance directly
- **Nonce**: per-account counter, must increment sequentially — prevents replay
- ⚠️ Don't confuse with: mining/PoW nonce (block header field) or ECDSA signing nonce `k` (per-signature random value)

### Analysis & Privacy Gotchas
- **Common-input-ownership heuristic**: all inputs to one tx assumed same owner
- **Change output identification**: often non-round value; may match input address type
- **Address reuse**: undermines privacy, enables clustering — best practice is generating a fresh address per transaction (HD wallets, BIP-32/44)

### Exam Traps
- Swapping private/public key roles (signing vs verifying)
- Confusing Bech32 vs Bech32m checksum algorithms
- Assuming Ethereum has multiple address formats (it has one)
- Treating 'nonce' as a single universal term across PoW, ECDSA, and account model contexts
