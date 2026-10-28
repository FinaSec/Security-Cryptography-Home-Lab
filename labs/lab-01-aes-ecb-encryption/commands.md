# AES-128 ECB Command Record

[Lab walkthrough](README.md)

These commands describe the lab workflow. Supply the input image locally and use the same key for encryption and decryption. The commands were not rerun during this documentation update.

## Check OpenSSL

```bash
openssl version
```

## Generate a 128-bit key

```bash
openssl rand -hex 16
```

This produces 16 random bytes represented by 32 hexadecimal characters.

## Encrypt the image file

Replace YOUR_32_HEX_CHARACTER_KEY with the generated value before running:

```bash
openssl enc -aes-128-ecb -e -a \
  -in Lab2.1-DC3-Unencrypted.jpg \
  -out Lab2.1-DC3-Encrypted.b64 \
  -K YOUR_32_HEX_CHARACTER_KEY
```

The output name uses .b64 because -a produces Base64-encoded ciphertext. It is not a viewable JPEG.

## Decrypt the ciphertext

```bash
openssl enc -aes-128-ecb -d -a \
  -in Lab2.1-DC3-Encrypted.b64 \
  -out Lab2.1-DC3-Decrypted.jpg \
  -K YOUR_32_HEX_CHARACTER_KEY
```

## Optional byte-for-byte verification

```bash
cmp Lab2.1-DC3-Unencrypted.jpg Lab2.1-DC3-Decrypted.jpg
```

A successful cmp exits with status 0 and prints nothing. This is a suggested verification step, not a newly recorded lab result.

## Interpretation

- -K supplies a raw hexadecimal key rather than a password.
- ECB uses no initialization vector.
- Identical plaintext blocks produce identical ciphertext blocks under the same key.
- These commands demonstrate file encryption and decryption. A visual pattern-leakage demonstration needs suitable bitmap pixel data and separate header handling.
- The .b64 output name clarifies the encoding; the earlier lab record named this output with a .jpg extension.
