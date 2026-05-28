# Reconnaissance Methodology

## Passive Recon
- WHOIS Enumeration
- DNS Lookup
- Google Dorking
- Social Media Enumeration
- GitHub Recon
- Public Metadata Collection

---

## Active Recon
- Ping Sweep
- Port Scanning
- Service Enumeration
- Banner Grabbing
- Directory Enumeration
- Subdomain Discovery

---

## Tools Used
- Nmap
- theHarvester
- Amass
- Subfinder
- WhatWeb
- Whois
- Dig
- Shodan

---

## Recon Workflow
1. Identify target scope
2. Collect public information
3. Enumerate services
4. Identify technologies
5. Map attack surface
6. Document findings


---
# Recon-ng Enumeration

## Objective
Enumerate hosts and domains using Recon-ng.

## Tool Used
- Recon-ng

## Module
recon/domains-hosts/bing_domain_web

## Target
example.com

## Commands Executed

```bash
recon-ng
workspaces create week3
modules load recon/domains-hosts/bing_domain_web
options set SOURCE example.com
run
show hosts
```

## Findings

| Host | Notes |
|------|------|
| example.com | Base domain identified |

## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Search Open Websites/Domains | T1593 |

## Outcome
Recon-ng successfully performed passive reconnaissance against target domain.


## Security Notice
Recon activities should only be performed in authorized lab environments.

