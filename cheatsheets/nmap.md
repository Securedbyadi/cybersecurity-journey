# Nmap

Only scan systems I own or have permission to test.

## Discovery

| Flag | Meaning |
|---|---|
| `-sL` | list targets only |
| `-sn` | find live hosts without a port scan |
| `-Pn` | skip discovery and treat every host as up |

## Ports

| Flag | Meaning |
|---|---|
| `-sT` | full TCP connect scan |
| `-sS` | SYN scan (needs `sudo`) |
| `-sU` | UDP scan |
| `-F` | 100 most common ports |
| `-p` | custom port range (`-p-` for all 65,535) |

## Detection

| Flag | Meaning |
|---|---|
| `-O` | OS detection |
| `-sV` | service and version detection |
| `-A` | OS, version, scripts and traceroute together |

## Timing

| Flag | Meaning |
|---|---|
| `-T0` to `-T5` | timing templates, from slow and stealthy to fast |
| `--min-parallelism` / `--max-parallelism` | minimum / maximum parallel probes |
| `--min-rate` / `--max-rate` | minimum / maximum packets per second |
| `--host-timeout` | give up on a host after this long |

## Output

| Flag | Meaning |
|---|---|
| `-v` / `-d` | verbosity / debugging |
| `-oN` | normal output to a file |
| `-oX` | XML output |
| `-oG` | grepable output |
| `-oA` | all three formats at once |
