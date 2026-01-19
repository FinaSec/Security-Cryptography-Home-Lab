# AES-128 ECB Encryption Commands

This document captures the exact OpenSSL commands used during the AES-128 ECB encryption lab.

## Verify OpenSSL Installation
```bash
openssl version
```

## Generate Random AES Key (128-bit)
```bash
openssl rand 16 -hex
```

## Encrypt Image Using AES-128 ECB
```bash
openssl enc -aes-128-ecb -e -a \
-in Lab2.1-DC3-Unencrypted.jpg \
-out Lab2.1-DC3-Encrypted.jpg \
-K <hexadecimal_key>
```

## Decrypt Image Using AES-128 ECB
```bash
openssl enc -aes-128-ecb -d -a \
-in Lab2.1-DC3-Encrypted.jpg \
-out Lab2.1-DC3-Decrypted.jpg \
-K <hexadecimal_key>
```

## Notes
- ECB mode encrypts identical blocks independently.
- Encryption succeeds, but structural patterns remain visible in encrypted images.
- Decryption restores the original image when the correct key is used.

> 🔐 Using `<hexadecimal_key>` instead of your real key is best practice for public repositories.
