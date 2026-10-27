# Hashing

Only crack hashes I own or have permission to test.

## Commands

| Command | Meaning |
|---|---|
| `sha256sum <file>` | SHA-256 hash of a file, to verify integrity |
| `john --wordlist=<wordlist> <hashfile>` | dictionary attack with John the Ripper |
| `hashcat -m <mode> <hashfile> <wordlist>` | dictionary attack with Hashcat (`-m` sets the hash type) |

## Hash prefixes

| Prefix | Hash |
|---|---|
| `$1$` | MD5 crypt |
| `$2a$` / `$2b$` | bcrypt |
| `$5$` | SHA-256 crypt |
| `$6$` | SHA-512 crypt |
