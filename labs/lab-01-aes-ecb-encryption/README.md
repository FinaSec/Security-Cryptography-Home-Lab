Lab: AES-128 ECB Encryption Analysis

Objective
This lab demonstrates AES-128 encryption and decryption using OpenSSL and highlights the security weaknesses of ECB mode when encrypting structured data such as images.

Tools Used
OpenSSL

Hex Fiend (hex editor)

CrypTool (online cryptographic analysis)

Lab Overview
An image file was encrypted using AES-128 in ECB mode and later decrypted using the same key. Hex editing was used to restore file headers and analyze how ECB mode preserves visual patterns in encrypted data.

Methodology
Encrypt a bitmap image using AES-128 in ECB mode.

Decrypt the image using the same encryption key.

Modify the encrypted file header using a hex editor.

Observe how patterns remain visible in the encrypted image.

Validate results using CrypTool analysis.

Key Observations

AES encryption and decryption correctly restore original data when the correct key is used.

ECB mode preserves structural patterns in encrypted images.

Weak or partially known keys significantly reduce cryptographic security.

Security Takeaway

ECB mode should not be used for sensitive or structured data because it leaks patterns that can reveal information about the original plaintext.

##  Evidence
Screenshots in the screenshots/ directory document:
- AES-128 key generation
- ECB encryption and decryption
- Pattern leakage in ECB-encrypted data
- Successful plaintext recovery using Cryptool




