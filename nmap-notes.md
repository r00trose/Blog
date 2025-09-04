# 🌐 Nmap Notes – My Learning Journal

These are my detailed notes while learning **Nmap (Network Mapper)**. I use this as a personal reference to remember commands, options, and scanning techniques.  

---

## 📌 What is Nmap?
- **Network Mapper**, an open-source tool for network discovery and security auditing.  
- Main uses:
  - Host discovery  
  - Port scanning  
  - Service/version detection  
  - OS fingerprinting  
  - Vulnerability scanning with NSE scripts  

---

## ⚙️ Basic Scans
```bash
nmap <target>               # default scan (top 1000 TCP ports)
nmap 192.168.1.1            # single host
nmap 192.168.1.0/24         # subnet
nmap example.com            # domain
````

---

## 🔎 Scan Techniques

```bash
-sS   # TCP SYN scan (stealth scan)
-sT   # TCP connect scan (less stealthy)
-sU   # UDP scan
-sA   # TCP ACK scan
-sW   # TCP Window scan
-sM   # TCP Maimon scan
```

---

## 🎯 Port Selection

```bash
-p 80              # scan only port 80
-p 22,80,443       # scan multiple ports
-p 1-1000          # scan range
-p-                # scan all 65535 ports
```

---

## 🛠 Service & Version Detection

```bash
-sV                 # detect service version
--version-intensity # adjust intensity (0–9)
```

Example:

```bash
nmap -sV example.com
```

---

## 🖥️ OS Detection

```bash
-O     # detect operating system
-A     # aggressive scan (OS, version, traceroute, NSE scripts)
```

---

## 🏃 Speed & Timing

```bash
-T0    # paranoid (slowest, stealthy)
-T1    # sneaky
-T2    # polite
-T3    # normal
-T4    # aggressive (faster, less stealth)
-T5    # insane (fastest, noisy)
```

---

## 📂 Output Options

```bash
-oN scan.txt    # normal output
-oG scan.gnmap  # grepable output
-oX scan.xml    # XML output
-oA results     # all formats
```

---

## 📦 NSE (Nmap Scripting Engine)

* Extend Nmap with built-in or custom scripts.
* Categories: `auth`, `vuln`, `discovery`, `brute`, `malware`, etc.

Examples:

```bash
nmap --script vuln example.com
nmap --script http-title -p 80 example.com
```

---

## 🔐 Firewall & Evasion

```bash
-f           # fragment packets
--mtu 24     # custom packet size
-D RND:10    # decoy scan
-S <IP>      # spoof source IP
--data-length 200 # add random payload
```

---

## 🧰 Host Discovery

```bash
-sn                 # ping scan (host discovery only, no ports)
-PE                 # ICMP echo request
-PP                 # ICMP timestamp request
-PU                 # UDP ping
-PS80,443           # TCP SYN ping to ports 80 and 443
-Pn                 # skip host discovery (assume host is up)
```

---

## 🧾 Useful Examples

```bash
nmap -p- -T4 example.com
# full port scan, faster timing

nmap -sV -sC example.com
# default scripts + service/version detection

nmap -A 192.168.1.100
# aggressive scan: OS, services, traceroute

nmap -p 22 --script ssh-brute 192.168.1.50
# brute force SSH with NSE script (for labs, not real targets!)
```

---

## 🌍 Top Ports & Services

* **21** → FTP
* **22** → SSH
* **23** → Telnet
* **25** → SMTP
* **53** → DNS
* **80** → HTTP
* **110** → POP3
* **143** → IMAP
* **443** → HTTPS
* **3389** → RDP

---

## 🛠 Notes to Remember

* Default: scans the top 1000 TCP ports.
* Use `-p-` to scan **all ports**.
* Use `-vv` for very verbose output.
* Always scan **your own lab / authorized targets only**.
* Combine Nmap with **Wireshark** or **TCPDump** for deeper analysis.


ister misin ben sana bunun için ayrıca **küçük bir “mindmap-style görsel” taslağı** da çıkarayım (ör. “Scan Types → Port Selection → Output → NSE” diye dallanan)?
```
