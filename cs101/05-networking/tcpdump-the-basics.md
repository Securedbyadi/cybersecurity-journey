# Tcpdump: The Basics

**Completed:** 2026-10-21 · **Block:** CS101 · **Sessions:** 1

## What this covers
Tcpdump is a command-line packet analyser. It captures, filters, saves and displays network traffic, so it works on servers with no GUI where Wireshark is not available.

## What I did
- Capture: `-i` (interface, or `any`), `-w` (save to a .pcap), `-r` (read a saved capture), `-c` (stop after N packets), `-n` / `-nn` (no name or port resolution), `-v` / `-vv` / `-vvv` (more detail)
- Filters: `host`, `src host`, `dst host`, `port`, `src port`, `dst port`, protocol names (`ip`, `tcp`, `udp`, `icmp`), combined with `and`, `or`, `not`
- Advanced filters: `greater` / `less` for packet length, `proto[expr:size]` for header bytes, TCP flag filters such as `tcp[tcpflags] == tcp-syn`, with `&`, `|` and `!` for flag combinations
- Display: `-q` (brief), `-e` (adds MAC addresses), `-A` (ASCII), `-xx` (hex), `-X` (hex and ASCII side by side)

```bash
sudo tcpdump -i any -nn -c 20
sudo tcpdump -i eth0 -w capture.pcap
tcpdump -r capture.pcap -nn 'tcp port 80 and host <ip>'
tcpdump -r capture.pcap 'tcp[tcpflags] == tcp-syn'
```

## What I learned
- Saving with `-w` and reading back with `-r` lets me capture once and filter many times.
- `-nn` stops DNS and port-name lookups, which keeps output fast and shows the real IPs and ports.
- Filters can be combined with `and`, `or` and `not`, and can match inside headers, for example on TCP flags.

## What confused me
- The `proto[expr:size]` syntax for header bytes and how it relates to the flag filters.
- Choosing between `-A`, `-xx` and `-X` for reading payloads.

## Where this shows up in a real SOC
Capturing and filtering traffic on a server during an incident, then opening the saved capture in Wireshark for a closer look.
