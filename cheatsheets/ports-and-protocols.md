# Ports and protocols

| Protocol | Transport | Default port | Meaning |
|---|---|---|---|
| TELNET | TCP | 23 | remote text session (unencrypted) |
| DNS | UDP or TCP | 53 | name to IP |
| HTTP | TCP | 80 | request and serve web pages |
| HTTPS | TCP | 443 | HTTP with encryption |
| FTP | TCP | 21 | file transfer |
| SMTP | TCP | 25 | send mail |
| POP3 | TCP | 110 | fetch mail |
| IMAP | TCP | 143 | fetch and sync mail |

## In one line
- DNS = name to IP
- WHOIS = domain registration lookup
- SMTP = send mail
- POP3 = fetch mail
- IMAP = fetch and sync mail
- FTP = file transfer
- Telnet = remote text session (unencrypted)
- HTTPS = HTTP with encryption

## Secure versions

| Plain | Secure | Default port |
|---|---|---|
| HTTP 80 | HTTPS | 443 |
| Telnet 23 | SSH | 22 |
| FTP 21 | SFTP (over SSH) | 22 |
| FTP 21 | FTPS (FTP + TLS) | 990 (implicit) |
| SMTP 25 | SMTPS | 465 |
| POP3 110 | POP3S | 995 |
| IMAP 143 | IMAPS | 993 |

VPN = encrypted tunnel across a public network; TLS = the encryption layer under HTTPS and the secure email protocols.
