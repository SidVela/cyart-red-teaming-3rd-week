# Advanced Nmap Vulnerability Assessment

## Objective
Perform advanced service enumeration and vulnerability assessment using Nmap.

## Target
scanme.nmap.org

## Commands Executed

```bash
nmap -sV -sC scanme.nmap.org
nmap -A scanme.nmap.org
nmap --script vuln scanme.nmap.org
nmap -A scanme.nmap.org -oN Outputs/nmap/advanced_scan.txt
```

## Open Ports and Services

| Port | Service | Version |
|------|---------|---------|
| 22 | SSH | OpenSSH 6.6.1p1 Ubuntu |
| 80 | HTTP | Apache 2.4.7 Ubuntu |
| 9929 | nping-echo | Nping Echo |
| 31337 | tcpwrapped | Elite Service |

## OS Detection

- Linux Kernel 5.x
- Ubuntu Linux Environment

## Vulnerability Findings

| Vulnerability | CVE | Severity | Description |
|--------------|-----|----------|-------------|
| Slowloris DoS | CVE-2007-6750 | Medium | Apache susceptible to Slowloris denial-of-service attack |

## Additional Findings

- Apache version disclosure detected
- HTTP headers exposed
- Possible directory enumeration findings
- CSRF forms identified
- Network path identified through traceroute

## MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Network Service Scanning | T1046 |
| Vulnerability Scanning | T1595 |
| Gather Victim Host Information | T1592 |

## Security Risks

- Public service exposure
- Service version disclosure
- Potential denial-of-service exposure
- Information leakage through banners

## Recommendations

- Upgrade Apache services
- Disable unnecessary banner disclosure
- Implement rate limiting
- Use WAF protections
- Restrict unnecessary public services
- Monitor suspicious scans with IDS/SIEM

## Conclusion

Advanced Nmap enumeration successfully identified exposed services, operating system information, and potential vulnerabilities on the target host. NSE vulnerability scripts detected a Slowloris denial-of-service exposure and multiple information disclosure findings.
