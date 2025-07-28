# Information Security Practice

This repository contains small programs and sample code used for studying network programming and common security vulnerabilities. Each file can be compiled individually and demonstrates a specific concept.

## Contents

| File | Description |
| --- | --- |
| `buffer overflow foo` | Simple program vulnerable to a buffer overflow in `foo()` that reads an ID without length checks. |
| `heartbleed` | Proof‑of‑concept exploit for CVE‑2014‑0160 (Heartbleed). Generates custom heartbeat requests to leak memory from vulnerable OpenSSL implementations. |
| `inp-write` | Demonstrates overwriting a return address and writing raw bytes to stdout. |
| `inp-write3` | Minimal shellcode example that writes a character then exits. |
| `pcap` | Lists available network adapters using the `pcap` library. |
| `select client.c` | Client side of a simple file transfer program using `select()` for multiplexing. |
| `select server.c` | Server counterpart that manages multiple clients with `select()`. |
| `win-cli` | WinSock client example for Windows systems. |
| `windump-structure` | C structure definitions for Ethernet, IP and TCP headers used in packet analysis. |

## Building

All examples are written in C. They can be compiled with `gcc` (or `cl` on Windows for `win-cli`). For example:

```bash
gcc -o overflow "buffer overflow foo"
```

Some programs may require extra libraries such as OpenSSL (`heartbleed`) or libpcap (`pcap`). Refer to the comments inside each file for details.

These files are intended for educational purposes only.
