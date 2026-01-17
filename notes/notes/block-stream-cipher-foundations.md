Title
Block and Stream Cipher Foundations

Scope
These notes capture core concepts needed for secure cryptography implementations and for recognizing real world failure patterns during security reviews.

Core Concepts

Block cipher security requirement
A secure block cipher should behave like a PseudoRandom Permutation PRP. Without the key, it should be computationally indistinguishable from a random permutation.

Stream cipher vs DRBG
A stream cipher uses a key and a nonce to produce a keystream. The nonce ensures uniqueness across encryptions under the same key. A DRBG typically expands output from a single seeded internal state.

Padding oracle condition
Padding oracle attacks become possible when a system behaves differently depending on whether CBC padding is valid. Differences in errors response codes or timing can leak information.

Nonce and IV terminology
Nonce is often treated as an Initialization Vector IV in practice. The key property is uniqueness for each encryption under the same key.

Why ECB is insecure
ECB mode produces identical ciphertext blocks for identical plaintext blocks. This leaks patterns and can reveal structure in the underlying data.

Security Relevance
Strong ciphers can still fail when used with insecure modes or leaky error handling. These concepts guide safe configuration and help explain common cryptographic incidents.

Next Experiments
Compare ECB CBC and GCM outputs with the same input using OpenSSL and document pattern leakage
Demonstrate why nonce reuse breaks confidentiality in stream cipher style encryption
Build a small toy example to understand how padding validation differences leak information
