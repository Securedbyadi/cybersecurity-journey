# Hashing Basics

**Completed:** 2026-10-27 · **Block:** CS101 · **Sessions:** 1

## What this covers
How hash functions work, why passwords are stored as salted hashes, how to recognise common hash types, how dictionary cracking works, and how hashes verify file integrity. A SOC analyst uses this to judge how exposed leaked credentials are and to check whether a file was altered. Only crack hashes I own or have permission to test.

## What I did
- Hash functions: one-way algorithms that turn any input into a fixed-length value
- Insecure storage: plain-text or reversibly encrypted passwords and why they are risky
- Secure storage: hashing with a salt, which defeats precomputed attacks such as rainbow tables
- Recognising hashes: algorithm by length, character set and prefix (for example MD5, SHA-256, bcrypt, and the `$6$` prefix for SHA-512)
- Cracking: dictionary attacks with a wordlist, CPU vs GPU speed, VM limits, using Hashcat and John the Ripper
- Integrity: comparing hashes to confirm a file was not corrupted or changed in transfer

```bash
sha256sum <file>
john --wordlist=<wordlist> <hashfile>
hashcat -m <mode> <hashfile> <wordlist>
```

## What I learned
- A hash cannot be reversed, so cracking means guessing inputs and comparing results.
- A salt makes identical passwords produce different hashes, which breaks rainbow tables.
- The same hash on both sides of a transfer shows the file is unchanged.

## What confused me
- Identifying a hash type from its length alone when several algorithms share a length.
- Hashing vs encryption: one is one-way, the other is reversible with a key.

## Where this shows up in a real SOC
Judging the impact of a leaked password database (salted and slow vs unsalted and fast), and using file hashes to verify a sample or look up what it is.
