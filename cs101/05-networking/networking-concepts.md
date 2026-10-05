# Networking Concepts

**Completed:** 2026-10-05 · **Block:** CS101 · **Sessions:** 1

## What this covers
How data moves across networks: the OSI and TCP/IP models, IP addressing, TCP and UDP, and encapsulation.

## What I did
- OSI model: 7 layers (Application, Presentation, Session, Transport, Network, Data Link, Physical)
- TCP/IP model: 4 layers (Application, Transport, Internet, Link)
- IP addresses: public vs private ranges (`192.168.x.x`, `10.x.x.x`) and NAT
- Transport: UDP (connectionless, fast) vs TCP (reliable, three-way handshake: SYN, SYN-ACK, ACK), about 65,000 ports
- Encapsulation: each layer adds its own header; segments (TCP), datagrams (UDP), frames (link layer)
- Telnet: connecting to a listening service on a port from the command line

```bash
telnet <target-ip> <port>
```

## What I learned
- TCP/IP is the simplified real-world version of OSI; its Application layer covers OSI layers 5 to 7.
- TCP trades speed for reliability with a handshake; UDP skips it.
- Encapsulation adds a header at each layer, and the data unit changes name along the way.

## What confused me
- Mapping 7 OSI layers onto 4 TCP/IP layers.
- Remembering which data unit name belongs to which layer.

## Where this shows up in a real SOC
Alerts name IPs, ports and protocols; knowing the layer tells me what to check next, for example a TCP handshake that never completes.
