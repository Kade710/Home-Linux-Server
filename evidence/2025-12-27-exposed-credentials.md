## Intentional Vulnerability – Exposed Sensitive File (v0.1)

### Description
A plaintext credentials file is intentionally exposed via Apache to establish an insecure baseline.

### Proof
```bash
curl http://192.168.12.227/credentials.txt
username: admin
password: admin123
