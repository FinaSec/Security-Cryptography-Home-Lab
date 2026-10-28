# Lab 01: AES-128 ECB Encryption Analysis

[Back to the lab index](../README.md) · [OpenSSL commands](commands.md)

## Objective

Explore AES-128 encryption and decryption using OpenSSL, and examine why ECB mode can expose patterns in structured plaintext.

## Tools

- OpenSSL
- Hex Fiend for hexadecimal file inspection
- CrypTool for cryptographic analysis

## Lab activities

The lab record describes image-file encryption and decryption, file-header inspection and modification, and CrypTool analysis. The command record uses an image named with a JPEG extension, while the header-restoration exercise concerns bitmap data. These should be interpreted as separate parts of the work.

1. Generate a 128-bit AES key.
2. Encrypt an image file using AES-128 in ECB mode.
3. Decrypt the ciphertext using the same key.
4. Inspect file structure and explore header restoration with a hex editor.
5. Review ECB behavior and plaintext recovery in CrypTool.

## Observations and interpretation

- The lab records encryption and decryption using the same AES key.
- Under a fixed key, ECB maps identical plaintext blocks to identical ciphertext blocks. This can reveal repeated structure.
- A visual image demonstration requires suitable uncompressed pixel data and a valid image header. Compressed JPEG data or Base64-encoded ciphertext does not automatically produce a recognizable encrypted image.
- Restoring an image header is a visualization step, not decryption.
- Plaintext recovery in a constrained teaching exercise does not establish that a randomly generated AES-128 key can be feasibly brute-forced.

## Supporting evidence

The [screenshot collection](../screenshots) contains records of key generation, encryption, decryption, header editing, and CrypTool work.

| Evidence | Screenshot |
| --- | --- |
| AES key generation | [Key generation](../screenshots/02-generate-aes-128-key.p.png) |
| ECB text analysis | [Encrypted text patterns](../screenshots/04-ecb-encrypted-text-patterns.png) |
| OpenSSL decryption | [Decryption result](../screenshots/05-aes-128-ecb-decryption-success.png) |
| Header editing | [Bitmap header restoration](../screenshots/05-ecb-bmp-header-restored-hex.png) |
| File verification | [Verification after decryption](../screenshots/06_ecb_file_verification_after_decryption.png) |
| CrypTool analysis | [Decrypted text](../screenshots/07-cryptool-ecb-decrypted-text.png) · [Recovered plaintext](../screenshots/08-cryptool-ecb-plaintext-recovered.png) |

## Lessons learned

The mode of operation affects what encryption reveals about plaintext. ECB is useful here for studying repeated-block behavior. File format, output encoding, and verification steps must also be documented to interpret an experiment correctly.

## Limitations

This page summarizes the existing lab record and screenshots. The original input file and ciphertext are not included alongside the walkthrough, so reproducing the commands requires supplying a local input file. The encryption experiment was not rerun during this documentation update.
