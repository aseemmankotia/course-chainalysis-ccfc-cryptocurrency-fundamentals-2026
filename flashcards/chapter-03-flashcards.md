## Chapter 3: Public/Private Keys, Address Formats, and the UTXO vs Account Models — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Bitcoin private key size? | 256-bit integer (1 to secp256k1 curve order n−1, n ≈ 1.158×10^77). Exam tip: same curve (secp256k1) and key size used by Ethereum. |
| 2 | How is a public key derived from a private key? | Elliptic curve point multiplication: pubkey = privkey × G (generator point on secp256k1). One-way — cannot reverse pubkey to privkey. |
| 3 | Bitcoin P2PKH address prefix and derivation? | Starts with '1'. Derived via SHA-256 then RIPEMD-160 of pubkey (HASH160), version byte 0x00, Base58Check encoded. |
| 4 | Bitcoin P2SH address prefix? | Starts with '3'. Version byte 0x05, Base58Check encoded hash of a redeem script (not a raw pubkey). |
| 5 | Native SegWit (P2WPKH) mainnet address prefix? | 'bc1q' — Bech32 encoded, witness version 0. Introduced in BIP-173, 2017. |
| 6 | Taproot address prefix and encoding? | 'bc1p' — Bech32m encoded, witness version 1. Introduced in BIP-350, 2021. Exam tip: Bech32m ≠ Bech32 (different checksum algorithm). |
| 7 | How is an Ethereum address derived? | Keccak-256 hash of the 64-byte uncompressed public key, take last 20 bytes, prefix with 0x. EIP-55 adds mixed-case checksum. |
| 8 | UTXO model vs Account model — core difference? | UTXO (Bitcoin): spends discrete unspent outputs, creates new outputs + change. Account model (Ethereum): updates a single balance in global state, ordered by nonce. |
| 9 | What is the Ethereum 'nonce' and why does it matter? | Per-account transaction counter that increments with each sent tx. Prevents replay attacks; txs must be processed in nonce order. NOT the same as mining nonce or ECDSA signing nonce k. |
| 10 | Why does a Bitcoin transaction need a 'change' output? | UTXOs must be spent in full — if input value exceeds the payment amount, the remainder must be sent to a new (often self-owned) output as change, minus miner fee. |
| 11 | Why does Bitcoin address reuse hurt privacy? | Enables the common-input-ownership heuristic and address clustering by chain analysts, linking multiple transactions/balances to one real-world entity. |
| 12 | Private key vs public key — exam trap? | Private key SIGNS transactions (must stay secret). Public key VERIFIES signatures and derives the address (safe to share). Exam distractors often swap these roles. |
