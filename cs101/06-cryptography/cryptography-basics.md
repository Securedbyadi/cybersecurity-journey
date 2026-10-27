# Cryptography Basics

**Completed:** 2026-10-23 · **Block:** CS101 · **Sessions:** 1

## What this covers
The vocabulary and building blocks of encryption: plaintext, ciphertext, keys, symmetric and asymmetric ciphers, and the basic maths behind them. A SOC analyst needs this to understand what encrypted traffic and stored data do and do not protect.

## What I did
- Why it matters: standards such as PCI DSS require encryption for sensitive data like card details
- Vocabulary: plaintext, ciphertext, cipher, key, encryption, decryption
- Historical ciphers: the Caesar cipher, a fixed shift of the alphabet
- Symmetric algorithms: DES, 3DES and AES; asymmetric encryption with a public and private key pair
- Maths: XOR (⊕) and the modulo operation (%)

## What I learned
- A cipher is the method and the key is the secret, so strong encryption relies on the key staying secret, not the method.
- DES is no longer trusted, and AES is the standard symmetric choice today.
- XOR and modulo are the simple operations that modern ciphers build on.

## What confused me
- Symmetric vs asymmetric: one shared key, or a public and private pair.
- Why the Caesar cipher is so easy to break even though it uses a key.

## Where this shows up in a real SOC
Knowing which data should be encrypted, spotting weak or outdated algorithms in configs and alerts, and understanding why encrypted traffic hides its content.
