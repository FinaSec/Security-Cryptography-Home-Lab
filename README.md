# Security Cryptography Home Lab

**Francisca Tupkeyi | AES encryption, ECB analysis, and cryptographic foundations**

## Overview

This repository documents my cryptography experiments using OpenSSL, Hex Fiend, and CrypTool on macOS. The published lab explores AES-128 encryption and decryption, key handling, and the limitations of ECB mode.

## Explore the work

| Resource | Contents |
| --- | --- |
| [Lab 01: AES-128 ECB analysis](labs/lab-01-aes-ecb-encryption/README.md) | Lab objectives, methodology, observations, and evidence |
| [OpenSSL command record](labs/lab-01-aes-ecb-encryption/commands.md) | Encryption and decryption commands with usage notes |
| [Cryptography foundations](notes/README.md) | Block ciphers, stream ciphers, ECB, and CBC |
| [Evidence collection](labs/screenshots) | Screenshots from the encryption, decryption, and analysis work |

## Published work and scope

Lab 01 has a written walkthrough, command record, and supporting screenshots. The notes cover additional concepts, including CBC and stream ciphers; those topics do not yet have separate published experiment walkthroughs.

The lab includes an image-file encryption exercise and a discussion of pattern leakage in structured data. Base64-encoded ciphertext is not a directly viewable encrypted image; the walkthrough distinguishes the command exercise from the conditions needed for a visual ECB demonstration.

## Lab environment

- Operating system: macOS
- Tools: OpenSSL, Hex Fiend, and CrypTool
- Materials: image files, ciphertext, and hexadecimal file inspection

## Skills demonstrated

- Recording OpenSSL encryption and decryption workflows
- Distinguishing raw keys from passwords
- Examining file structure with a hex editor
- Explaining how ECB exposes repeated plaintext blocks
- Documenting experimental observations and limitations

## Repository guide

- [labs/](labs/README.md): lab index and walkthroughs
- [labs/screenshots/](labs/screenshots): supporting evidence
- [notes/](notes/README.md): conceptual foundations

## Key takeaway

Encryption security depends on the mode of operation, key handling, and implementation choices as well as the underlying cipher. This repository uses ECB as a learning exercise to examine those choices.
