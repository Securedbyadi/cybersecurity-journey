# Tcpdump

## Capture

| Flag | Meaning |
|---|---|
| `-i` | interface to capture on (`any` for all) |
| `-w` | save the capture to a .pcap file |
| `-r` | read a saved capture |
| `-c` | stop after N packets |
| `-n` / `-nn` | no name or port resolution |
| `-v` / `-vv` / `-vvv` | more detail |

## Filters

| Filter | Meaning |
|---|---|
| `host` | traffic to or from a host |
| `src host` / `dst host` | traffic from / to a host |
| `port` | traffic on a port |
| `src port` / `dst port` | traffic from / to a port |
| `ip`, `tcp`, `udp`, `icmp` | match a protocol |
| `and`, `or`, `not` | combine filters |

## Advanced filters

| Filter | Meaning |
|---|---|
| `greater` / `less` | match on packet length |
| `proto[expr:size]` | match bytes in a header |
| `tcp[tcpflags] == tcp-syn` | match TCP flags, here SYN |
| `&`, `\|`, `!` | combine flags |

## Display

| Flag | Meaning |
|---|---|
| `-q` | brief output |
| `-e` | add MAC addresses |
| `-A` | show payload as ASCII |
| `-xx` | show hex |
| `-X` | show hex and ASCII side by side |
