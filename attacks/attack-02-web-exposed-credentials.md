# Attack 02 — Web-Based Credential Exposure

## Objective
Exploit exposed web-accessible files to obtain sensitive credentials without authentication.

## Target
Home-Linux-Server v0.1 (bare metal)

## Preconditions
- HTTP service exposed on TCP/80
- World-writable web root
- Sensitive file present in web directory
- No access controls on web content

## Attack Steps
1. Accessed exposed file via HTTP:
   - `http://192.168.12.227/backup.txt`
2. Retrieved plaintext credentials from web-accessible file
3. Correlated credentials with enabled SSH password authentication

## Findings
- Sensitive credentials stored in web root
- No authentication or access controls
- File permissions set to 777
- File owned by root

## Impact
An attacker can:
- Exfiltrate credentials without detection
- Attempt SSH authentication using exposed password
- Pivot from web access to system-level access
- Escalate the incident beyond simple data exposure

## Notes
No authentication attempts were performed in this phase. Credential exposure alone represents a critical security failure.
