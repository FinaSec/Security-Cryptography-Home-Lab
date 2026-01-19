# Block and Stream Cipher Foundations

## Purpose
These notes capture core cryptographic concepts required to understand modern encryption
systems and common implementation failures observed in real-world security incidents.

## Block Ciphers
A secure block cipher must behave like a PseudoRandom Permutation (PRP), meaning that
without the key it is computationally indistinguishable from random output.

AES is the most widely used block cipher and supports multiple modes of operation, each
with different security properties.

## Stream Ciphers
Stream ciphers generate a keystream using a key and a nonce. The nonce ensures uniqueness
so the same key can be reused safely across multiple encryptions.

Nonce reuse breaks confidentiality and is a common source of cryptographic failure.

## ECB Mode Weakness
Electronic Code Book (ECB) mode encrypts identical plaintext blocks into identical
ciphertext blocks. This causes pattern leakage and allows structural information
to remain visible in encrypted data such as images.

## CBC Mode Improvement
Cipher Block Chaining (CBC) mode incorporates the previous ciphertext block and an
initialization vector (IV), preventing identical plaintext blocks from producing
identical ciphertext.

## Security Takeaway
Cryptographic algorithms are often mathematically sound, but insecure modes, weak keys,
and poor implementation decisions frequently lead to real-world compromises.








