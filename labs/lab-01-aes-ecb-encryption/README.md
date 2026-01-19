# Lab 01: AES Encryption and ECB Mode Analysis

## Objective
This lab demonstrates AES-128 encryption and decryption using OpenSSL and highlights
the security weaknesses of ECB mode when encrypting structured data such as images.

## Tools Used
- OpenSSL
- Hex Fiend (hex editor)
- Cryptool (online analysis)

## Lab Summary
An image file was encrypted using AES-128 in ECB mode and later decrypted using the same
key. Hex editing was used to restore file headers and analyze how ECB preserves patterns
in encrypted data.

## Key Observations
- AES encryption and decryption successfully restore original data when the correct key is used
- ECB mode preserves structural patterns in encrypted images
- Weak or partially known keys significantly reduce cryptographic security

## Status
Screenshots and encrypted artifacts will be added after validation across multiple systems.
