# OSINT and Reconnaissance

## Objective
Gather public intelligence and perform reconnaissance on a target domain.

---

# Target
example.com

---

# Tools Used
- Recon-ng
- Nmap
- Whois
- Dig
- Nslookup
- Shodan

---

# Recon-ng Enumeration

## Module
recon/domains-hosts/bing_domain_web

## Findings

| Subdomain | IP Address | Notes |
|------------|------------|-------|
| www.example.com | 93.184.216.34 | Web server |

---

# DNS Enumeration

## dig

```bash
dig example.com
```

## nslookup

```bash
nslookup example.com
```

---

# Whois Enumeration

```bash
whois example.com
```

Registrar and DNS details collected successfully.

---

# Shodan Research

## Query
apache country:US

## Findings
Exposed Apache servers identified. Some systems appear outdated and publicly accessible.

---

# Nmap Scan

## Command

```bash
nmap -sV example.com
```

## Results

| Port | Service | Version |
|------|----------|----------|
| 80 | HTTP | Apache |

---

# MITRE ATT&CK Mapping

| Technique | ID |
|-----------|----|
| Active Scanning | T1595.002 |
| Service Discovery | T1046 |
| Search Open Websites | T1593 |

---

# Recommendations
- Reduce exposed services
- Monitor reconnaissance activity
- Update outdated systems

---

# Ethical Notice
Testing performed only for educational and authorized purposes.



## Phone Intelligence Gathering Practical

### Objective
Performed OSINT-based phone intelligence gathering using PhoneInfoga.

### Target Number
+14155552671 (Sample/Test Number)

### Actions Performed
- Executed phone number intelligence scan
- Enumerated country information
- Checked carrier/provider details
- Gathered public OSINT references

### Findings
- Successfully demonstrated phone reconnaissance workflow
- Identified metadata associated with target number format
- Verified OSINT enumeration process

### MITRE ATT&CK Mapping
- T1593 – Search Open Websites/Domains
- T1595 – Active Reconnaissance
