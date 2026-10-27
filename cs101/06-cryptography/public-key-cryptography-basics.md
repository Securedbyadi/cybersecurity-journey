# Public Key Cryptography Basics

**Completed:** 2026-10-26 · **Block:** CS101 · **Sessions:** 1

## What this covers
How asymmetric encryption works and where it is used: RSA, Diffie-Hellman key exchange, SSH keys, digital signatures and certificates, and PGP/GPG.

## What I did
- Common uses: confidentiality, authenticity and integrity, shown with the open-padlock analogy for the public key
- RSA: key pairs built from two large primes (p and q) and Euler's totient
- Diffie-Hellman: two parties agree a shared secret over an insecure channel using modulo maths
- SSH: a private key proves a client's identity to a server
- Certificates: a server proves its identity to a client, with providers such as Let's Encrypt building the trust chain for HTTPS
- PGP / GPG: importing a public key and decrypting a message

## What I learned
- The public key can be shared freely, while the private key never leaves its owner.
- Diffie-Hellman solves the problem of agreeing a secret key over a channel anyone can watch.
- Certificates are how a browser knows a server is who it claims to be, which is what makes HTTPS trustworthy.

## What confused me
- Which key encrypts and which decrypts, and how that flips for signatures versus confidentiality.
- Why RSA depends on factoring large numbers being hard.

## Where this shows up in a real SOC
Checking certificates on alerts, spotting expired or self-signed ones, and knowing a leaked private key (SSH or TLS) means the identity it protects is compromised.
