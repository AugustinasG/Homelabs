# Lab 01 – Windows 10 “No Internet” (NCSI) Troubleshooting

**Goal:** Diagnose and fix a Windows client that shows “No Internet” while browsing still works.

**Environment:**
- Windows 10 22H2 VM (Hyper-V)
- Test DNS server (Pi-hole) and router VM

**Repro Steps:**
1. Change NCSI active probe DNS to a non-resolving host (or block msftncsi.com).
2. Flush DNS, reboot; observe “No Internet access” icon.

**Troubleshooting:**
- `ipconfig /all` – OK (IP/DNS/gateway present)
- `nslookup msftconnecttest.com` – fails
- `Get-DnsClientNrptPolicy` – checked for overrides
- Checked Windows Event Viewer → NCSI errors

**Fix:**
- Restored DNS settings to router; allowed msftconnecttest domains.
- `ipconfig /flushdns` and `netsh winsock reset`.

**Result:** NCSI back to “Internet access”.  
**What I learned:** Windows uses NCSI HTTP/DNS probes; false negatives are common with DNS blockers; how to validate network stack.

_Screenshots:_
![NCSI error](screenshots/ncsi-error.png)
![Fix verified](screenshots/ncsi-ok.png)
