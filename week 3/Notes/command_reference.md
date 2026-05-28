# Command Reference

## Reconnaissance

### Nmap
nmap -sV <target>
nmap -A <target>
nmap -Pn <target>

### Whois
whois <domain>

### DNS Enumeration
dig <domain>
nslookup <domain>

---

## Web Enumeration

### Gobuster
gobuster dir -u http://target -w /usr/share/wordlists/dirb/common.txt

### Nikto
nikto -h http://target

---

## Exploitation

### Metasploit
msfconsole
search <service>
use <module>

---

## Packet Analysis

### Tcpdump
tcpdump -i eth0

### Wireshark
wireshark

---

## Git Operations

git status
git add .
git commit -m "message"
git push

---

## Docker

docker ps
docker images
docker compose up

---

## Logging Format

[DATE] [ACTIVITY] [STATUS]

Example:
2026-05-27 Recon Started

---

## Ethical Notice
Commands used only in authorized lab environments.
