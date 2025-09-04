# 🌐 Nmap Notes – Network Scanning Basics

These are my notes while learning **Nmap (Network Mapper)**, one of the most widely used tools for network discovery and security auditing.  

---

## 📌 What is Nmap?
- Nmap = **Network Mapper**  
- Open-source tool used for:
  - Discovering hosts and services on a network  
  - Detecting open ports  
  - Identifying OS, versions, and vulnerabilities  

---

## ⚙️ Basic Usage
```bash
nmap <target>
````

* Scans the target IP/domain with default options.

Examples:

```bash
nmap 192.168.1.1      # scan a single host
nmap 192.168.1.0/24   # scan a whole subnet
nmap example.com      # scan a domain
```

---

## 🔎 Common Options

```bash
-sS   # TCP SYN scan (stealth scan)
-sT   # TCP connect scan
-sU   # UDP scan
-p    # specify port(s), e.g. -p 80,443 or -p 1-1000
-A    # aggressive scan (OS detection, version detection, scripts, traceroute)
-O    # detect operating system
-v    # verbose output
```

---

## 📂 Examples

```bash
nmap -p 22 192.168.1.10
# Scan only port 22 (SSH) on target

nmap -p 1-1000 192.168.1.10
# Scan first 1000 ports

nmap -A example.com
# Aggressive scan: OS detection, version, scripts, traceroute

nmap -sU 192.168.1.10
# UDP scan (slower but useful for DNS, SNMP, etc.)
```

---

## 🛠 Useful Notes

* Default Nmap scan checks the **most common 1000 ports**.
* Always check permissions — scanning networks you don’t own/authorize can be **illegal**.
* Combine Nmap with tools like **Wireshark** for deeper analysis.
* Use `man nmap` for the full list of options (it’s huge!).

```
