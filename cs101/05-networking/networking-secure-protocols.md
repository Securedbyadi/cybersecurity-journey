# Networking Secure Protocols

**Completed:** 2026-10-08 · **Block:** CS101 · **Sessions:** 1

## What this covers
How everyday network traffic is encrypted: TLS and the secure versions of web, email, remote login, file transfer, plus VPNs. A SOC analyst needs this to tell normal encrypted traffic from plain-text traffic that should not be there.

## What I did
- TLS: the encryption layer that other secure protocols build on
- HTTPS: HTTP over TLS, so passwords and session tokens are not readable in transit
- SMTPS, POP3S, IMAPS: the TLS-protected versions of SMTP, POP3 and IMAP
- SSH: encrypted remote login and administration
- SFTP and FTPS: secure file transfer; SFTP runs over SSH, FTPS is FTP with TLS
- VPN: an encrypted tunnel that carries traffic across a public network

## What I learned
- TLS is the common layer under HTTPS and the secure email protocols.
- SSH replaces plain-text remote tools like Telnet, and SFTP rides on top of it.
- A VPN encrypts everything between me and the VPN endpoint, not only one application.

## What confused me
- SFTP and FTPS sound alike but work differently: SFTP uses SSH, FTPS uses TLS.
- Which secure protocol maps to which plain-text one (SMTPS/SMTP, POP3S/POP3, IMAPS/IMAP).

## Where this shows up in a real SOC
Plain-text protocols (Telnet, FTP, HTTP) where an encrypted one should be used are a finding, and encrypted traffic hides its content, so analysts lean on metadata like IPs, ports and volumes.
