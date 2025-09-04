````markdown
# 🐧 Linux Notes – Fundamentals

These are my personal notes while learning Linux basics. I’m writing them down to keep concepts fresh and to build a quick reference for myself.  

---

## 📌 What is Linux?
- Linux = an **open-source operating system kernel** created by Linus Torvalds (1991).  
- Distributions (Ubuntu, Fedora, Kali, Arch, etc.) are built on top of the Linux kernel.  
- It powers servers, cloud infrastructure, mobile devices (Android), and security tools.  

---

## 🖥️ The Linux Structure
1. **Kernel** – the core of the OS (handles CPU, memory, devices).  
2. **Shell** – interface between user and kernel (Bash is the most common).  
3. **File System** – organized like a tree (`/` = root).  
4. **Utilities** – commands and tools (`ls`, `cd`, `cat`, etc.).  

---

## 📂 File System Basics
- `/` → root directory (everything starts here)  
- `/home` → personal user files  
- `/etc` → system configuration  
- `/bin` → essential binaries (commands)  
- `/var` → logs and variable data  
- `/tmp` → temporary files  

---

## ⚙️ Common Commands
```bash
pwd          # print working directory
ls -l        # list files in long format
cd /path     # change directory
cp file1 file2   # copy file
mv old new   # move/rename file
rm file      # remove file
cat file     # view file contents
man ls       # manual page for ls
````

---

## 🔑 Permissions

```bash
ls -l
```

Example output:
`-rw-r--r-- 1 user group 1234 Sep 4 file.txt`

* First character = type (`-` = file, `d` = directory).
* Next 3 = owner permissions (read, write, execute).
* Next 3 = group permissions.
* Last 3 = others.

Change permissions:

```bash
chmod 755 script.sh
```

---

## 🐚 Shell vs Kernel

* **Kernel** = the heart of Linux, controls hardware.
* **Shell (Bash)** = the tool we use to talk to the kernel.
* Commands → Shell → Kernel → Action on hardware.

---

## 📦 Package Management

* Ubuntu/Debian → `apt install package`
* Fedora/RedHat → `dnf install package`
* Arch → `pacman -S package`

---

## 🛠 Useful Notes

* Linux is **case-sensitive** (`File.txt` ≠ `file.txt`).
* Everything is a **file** (even devices and processes).
* Use `tab` for auto-completion and `history` to see past commands.
* Always check `man command` for documentation.

```
