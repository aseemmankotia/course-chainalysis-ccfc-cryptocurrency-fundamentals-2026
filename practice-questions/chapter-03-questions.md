## Chapter 3: Public/Private Keys, Address Formats, and the UTXO vs Account Models — Practice Questions

**Q1.** A blockchain analyst sees a Bitcoin transaction with 3 inputs and 2 outputs. All 3 inputs come from addresses that have never appeared together in any other transaction. What can the analyst reasonably conclude using the common-input-ownership heuristic?

A) The transaction is invalid because inputs don't match
B) All 3 input addresses are controlled by the same entity
C) One of the outputs must be a coinbase reward
D) The addresses belong to a mining pool

<details>
<summary>Answer</summary>

**Correct: B**

The common-input-ownership heuristic assumes that if multiple UTXOs are spent as inputs in a single transaction, the same private key holder authorized all of them, since each input requires a valid signature from its owner.

**Why the others are wrong:**
- Input/output value mismatch relates to fees, not validity — inputs and outputs rarely need to 'match' exactly
- Coinbase transactions have exactly one input (no previous output) — this tx has 3 real inputs so it's not coinbase
- Nothing about input count or address history indicates mining pool activity specifically

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** In the same 3-input, 2-output transaction, the analyst wants to identify which output is likely the 'change' returned to the sender. Which heuristic is MOST commonly used for this?

A) The output with the larger BTC value is always the change
B) The change output is always listed first in the transaction
C) The change output typically has an uneven/non-round value and often reuses an address format matching the input addresses
D) The change output always has a value of exactly zero

<details>
<summary>Answer</summary>

**Correct: C**

Change amounts are calculated as leftover value (inputs minus payment minus fee), producing non-round numbers, and wallets often generate change addresses in the same format as the inputs — both are used in real chain analysis.

**Why the others are wrong:**
- Payment amounts are frequently larger than change — value size alone is not reliable
- Bitcoin transactions have no required output ordering that signals purpose
- A zero-value output would be non-standard and is not how change works

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An Ethereum user submits two transactions from the same account within the same block, both with nonce = 5. What happens?

A) Both transactions execute because Ethereum allows duplicate nonces per block
B) The account is automatically locked for security
C) Only one transaction with nonce 5 is accepted; the other is rejected or replaces it depending on gas price and pending pool rules
D) The transactions are merged into a single transaction by the EVM

<details>
<summary>Answer</summary>

**Correct: C**

Ethereum's account model requires nonces to increment sequentially per account. Only one transaction per nonce value can ever be included; a second transaction with the same nonce either fails as underpriced/duplicate or replaces the pending one if it offers a higher gas price.

**Why the others are wrong:**
- Duplicate nonces are explicitly disallowed — this is the mechanism that prevents replay attacks
- Ethereum has no automatic account-locking security feature tied to nonce collisions
- The EVM does not merge transactions; each is a distinct signed object

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A wallet developer needs to support the OLDEST Bitcoin address format for maximum compatibility with legacy software from 2012. Which format should they use?

A) P2PKH (starts with '1')
B) Bech32 (bc1q...)
C) P2SH (starts with '3')
D) Bech32m (bc1p...)

<details>
<summary>Answer</summary>

**Correct: A**

P2PKH ('Pay to Public Key Hash') addresses starting with '1' were the original Bitcoin address format available since the genesis block and supported by all software, including 2012-era wallets.

**Why the others are wrong:**
- Bech32 (SegWit v0) was introduced with BIP-173 in 2017 and is not compatible with pre-2017 software
- P2SH was introduced via BIP-16 in 2012, later than the original P2PKH format
- Bech32m (Taproot, segwit v1) was introduced in 2021 with BIP-350 — the newest format

</details>

---

**Q5.** Which key is used to CREATE a valid digital signature authorizing a cryptocurrency transaction?

A) The public key
B) The private key
C) The address
D) The block hash

<details>
<summary>Answer</summary>

**Correct: B**

The private key is the secret input to the signing algorithm (ECDSA on secp256k1 for Bitcoin/Ethereum). Only someone holding the private key can produce a signature that the public key can verify.

**Why the others are wrong:**
- The public key is used to VERIFY a signature, not create it
- The address is a derived hash used for receiving funds — it plays no role in signing
- Block hashes relate to mining/consensus, not transaction authorization

</details>

---

**Q6.** What is the standard human-readable prefix for a mainnet Bitcoin native SegWit (P2WPKH, witness version 0) address?

A) 1
B) bc1q
C) 3
D) bc1p

<details>
<summary>Answer</summary>

**Correct: B**

Bech32-encoded native SegWit v0 addresses on Bitcoin mainnet use the human-readable part 'bc' plus separator, rendering as addresses beginning with 'bc1q'.

**Why the others are wrong:**
- '1' prefix denotes legacy P2PKH (Base58Check, version byte 0x00)
- '3' prefix denotes P2SH (Base58Check, version byte 0x05)
- 'bc1p' denotes Bech32m-encoded witness version 1 (Taproot) addresses, not version 0

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** How is an Ethereum address derived from a key pair?

A) SHA-256 hash of the private key, truncated to 20 bytes
B) Base58Check encoding of the public key with a version byte
C) RIPEMD-160 hash of the private key with a checksum appended
D) Keccak-256 hash of the uncompressed public key, taking the last 20 bytes

<details>
<summary>Answer</summary>

**Correct: D**

Ethereum computes Keccak-256 over the 64-byte uncompressed public key (excluding the 0x04 prefix) and takes the rightmost 20 bytes as the address, optionally applying EIP-55 mixed-case checksumming for display.

**Why the others are wrong:**
- SHA-256 of the private key is never used — hashing the private key directly would leak no verifiable link to the public key and is not the Ethereum spec
- Base58Check with version bytes is the Bitcoin legacy address scheme, not Ethereum's
- RIPEMD-160 combined with SHA-256 (HASH160) is the Bitcoin P2PKH derivation method, not Ethereum's

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement BEST describes the core structural difference between Bitcoin's UTXO model and Ethereum's account model?

A) UTXO uses account balances while Ethereum uses discrete coin outputs
B) Both models are functionally identical, differing only in naming convention
C) UTXO tracks discrete unspent outputs consumed as inputs, requiring change outputs; the account model tracks a single running balance per address, updated with each transaction
D) The account model requires more computational power to validate than UTXO

<details>
<summary>Answer</summary>

**Correct: C**

Bitcoin transactions consume specific unspent transaction outputs (UTXOs) as inputs and create new outputs, needing a change output for leftover value. Ethereum instead maintains a global state trie of account balances directly decremented/incremented by transactions, using a nonce for ordering.

**Why the others are wrong:**
- This reverses the definitions — UTXO is Bitcoin's model, account/balance is Ethereum's
- The two models have fundamentally different data structures (unspent output sets vs. state trie) and are not interchangeable in implementation
- Validation cost depends on implementation details, not model type — this is not a defining structural difference tested on the exam

</details>

---

