# Nmap: The Basics

**Completed:** 2026-10-22 · **Block:** CS101 · **Sessions:** 1

## What this covers
Nmap is the standard tool for finding live hosts, open ports and the services behind them. It is used to map a network and to check what a host exposes. Only scan systems I own or have permission to test.

## What I did
- Host discovery: `-sL` (list targets only), `-sn` (find live hosts without a port scan), `-Pn` (skip discovery and treat every host as up)
- Port scanning: `-sT` (full TCP connect), `-sS` (SYN scan, needs `sudo`), `-sU` (UDP), `-F` (100 most common ports), `-p` (custom range, `-p-` for all 65,535)
- Detection: `-O` (OS), `-sV` (service and version), `-A` (OS, version, scripts and traceroute together)
- Timing: `-T0` to `-T5`, `--min-parallelism` / `--max-parallelism`, `--min-rate` / `--max-rate`, `--host-timeout`
- Output: `-v` / `-d` (verbosity and debugging), `-oN` (normal), `-oX` (XML), `-oG` (grepable), `-oA` (all three)

```bash
nmap -sn <network>
sudo nmap -sS -p- <target>
nmap -sV -O <target>
nmap -oA scan-results <target>
```

## What I learned
- Without `sudo`, Nmap falls back to a full connect scan; a SYN scan needs root because it crafts its own packets.
- Host discovery and port scanning are separate steps, and `-Pn` is for hosts that do not answer ping.
- `-A` bundles OS detection, version detection, scripts and traceroute, which is thorough but noisy.

## What confused me
- The difference between `-sT` and `-sS`, and why one needs root.
- How the timing templates (`-T0` to `-T5`) trade stealth against speed.

## Where this shows up in a real SOC
Port scans are a common first step in an attack, so recognising scan patterns in logs matters, and defenders run the same scans to check what their own hosts expose.
