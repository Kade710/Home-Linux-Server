# Attack 01 — Initial Reconnaissance

## Objective
Identify exposed services and information without authentication or exploitation.

## Target
Home-Linux-Server v0.1 (bare metal)

## Methods
- Service enumeration using `ss`
- OS fingerprinting using `uname` and `lsb_release`
- Web root inspection

## Findings

### Exposed Services
- SSH (TCP/22) listening on all interfaces
- HTTP (TCP/80) listening on all interfaces

### OS Identification
- Ubuntu 24.04.3 LTS
- Kernel 6.14.0-37-generic
- Architecture: x86_64

### Web Exposure
- World-writable web root (`/var/www/html`)
- Sensitive file exposed: `backup.txt`
- File accessible via HTTP
- File owned by root

## Impact
An attacker on the local network can:
- Enumerate OS and kernel version
- Access sensitive files via HTTP
- Attempt SSH password-based authentication
- Prepare targeted exploits based on known Ubuntu defaults

## Notes
No exploitation performed in this phase. This recon phase establishes sufficient attack surface for follow-on attacks.
