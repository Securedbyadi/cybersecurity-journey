# Wireshark: The Basics

**Completed:** 2026-10-20 · **Block:** CS101 · **Sessions:** 1

## What this covers
Wireshark is the standard tool for capturing and reading network traffic. This room covers the interface, reading a packet layer by layer, searching a capture, following a conversation, and pulling files out of a capture. An analyst uses it to see what actually crossed the wire.

## What I did
- Interface: the three panes (Packet List, Packet Details, Packet Bytes in hex/ASCII)
- Packet dissection: expanded a packet through its layers down to application-layer fields such as HTTP headers
- Searching: found strings across the panes and jumped to a packet by its number
- Following a stream: used Follow TCP/HTTP Stream to read a whole conversation in order
- Extraction: exported an embedded file from the captured bytes and hashed it to verify it

## What I learned
- The three panes show the same packet at different depths: the list for the overview, the details for each layer and the bytes for the raw data.
- Following a stream turns scattered packets into a readable conversation, which makes plain-text traffic easy to inspect.
- A file carried in a capture can be rebuilt from its packets, and a hash lets me verify or look up what it is.

## What confused me
- Telling the search options apart (which pane or field it searches).
- Packet number vs stream number: they are different counters.

## Where this shows up in a real SOC
Opening a capture from an alert to see exactly what a host sent and received, and pulling out any file or credential that travelled in plain text.
