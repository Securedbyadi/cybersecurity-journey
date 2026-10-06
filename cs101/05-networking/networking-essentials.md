# Networking Essentials

**Completed:** 2026-10-06 · **Block:** CS101 · **Sessions:** 1

## What this covers
The protocols and mechanisms that make a local network work day to day: DHCP, ARP, ICMP, routing and NAT. A SOC analyst needs these to read network logs and spot traffic that doesn't fit.

## What I did
- DHCP: automatic assignment of IP address, subnet mask and DNS server (a phone joining home Wi-Fi)
- ARP: mapping an IP address (Layer 3) to a MAC address (Layer 2) on the local network
- ICMP: diagnostics and error reporting
- Routing: forwarding packets between separate networks using a routing table and default gateway
- NAT: translating private IPs to one public IP so several devices share an internet connection

```
# Windows
ipconfig /release
ipconfig /renew
arp -a
ping <ip>
tracert <ip>
route print

# Linux
dhclient
ping <ip>
traceroute <ip>
ip route
```

## What I learned
- DHCP hands out the whole network configuration automatically, not just the IP address.
- ARP is how a host finds the MAC of a local IP before it can send a frame, and `arp -a` shows what it has cached.
- NAT lets many private devices share one public IP, and `ping` and `traceroute`/`tracert` use ICMP to test reachability and show the path.

## What confused me
- ARP works at the link layer inside one network, while routing works between networks, so the two are easy to mix up.
- Keeping the Windows and Linux command names straight (`tracert` vs `traceroute`, `route print` vs `ip route`).

## Where this shows up in a real SOC
An unexpected ARP reply, an odd gateway in a routing table or unusual ICMP traffic can point to scanning or a man-in-the-middle attempt.
