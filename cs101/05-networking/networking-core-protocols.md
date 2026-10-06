# Networking Core Protocols

**Completed:** 2026-10-06 · **Block:** CS101 · **Sessions:** 1

## What this covers
The core TCP/IP protocols that run behind everyday apps: DNS, WHOIS, HTTP/HTTPS, FTP and email (SMTP, POP3, IMAP). A SOC analyst sees these in nearly every log and alert.

## What I did
- DNS: resolving domain names to IP addresses
- WHOIS: querying domain registration records
- HTTP / HTTPS: requesting and serving web pages, and what changes when it is encrypted
- FTP: transferring files
- Email: SMTP (sending), POP3 (retrieving), IMAP (retrieving and syncing)

| Protocol | Transport | Default port |
|---|---|---|
| TELNET | TCP | 23 |
| DNS | UDP or TCP | 53 |
| HTTP | TCP | 80 |
| HTTPS | TCP | 443 |
| FTP | TCP | 21 |
| SMTP | TCP | 25 |
| POP3 | TCP | 110 |
| IMAP | TCP | 143 |

## What I learned
- Each everyday action maps to a protocol and a default port: browsing is HTTP/HTTPS, name lookups are DNS, file transfers are FTP.
- DNS usually runs over UDP but can use TCP.
- SMTP sends mail, while POP3 and IMAP retrieve it, and IMAP keeps mailboxes in sync across devices.

## What confused me
- POP3 vs IMAP: both fetch mail, but IMAP syncs the mailbox rather than just downloading it.
- Remembering the port numbers; the table is the quickest re-read.

## Where this shows up in a real SOC
Traffic on an unexpected port, or plain-text protocols like Telnet and FTP in the logs, is a quick sign that something needs a closer look.
