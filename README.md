# 🔍 Nmap Commands Cheat Sheet

A beginner-friendly reference of Nmap commands — what they do and when to use them.

> **⚠️ Only scan networks and devices you own or have written permission to scan.** Unauthorized scanning is illegal and can result in criminal charges.

---

## 📂 Contents

- [Nmap Installation](Nmap%20Installation)
- [Nmap Basic Scans](Nmap%20Basic%20Scans)
- [Host Discovery Scans](Host%20Discovery%20Scans)
- [Nmap Scan Types](Nmap%20Scan%20Types)
- [Nmap Detection](Nmap%20Detection)
- [Nmap Timming & Speed Scans](Nmap%20Timing%20%26%20Speed%20Scans)
- [Nmap Scripts (NSE)](Nmap%20Scripts%20(NSE))
- [Nmap Output & Saving](Nmap%20Output%20%26%20Saving)
- [Nmap Targeting Scans](Nmap%20Targeting%20Scans)
- [Other Useful Options](Other%20Useful%20Options)

---

## 🚀 Quick Start

**Scan yourself:**
```bash
nmap localhost
```

**Find all devices on your network:**
```bash
nmap -sn 192.168.1.0/24
```

**Fast scan a device:**
```bash
nmap -F 192.168.1.1
```

**Full info scan (needs sudo):**
```bash
sudo nmap -A -T4 192.168.1.1
```

**Check web server ports:**
```bash
nmap -p 80,443 -sV example.com
```

**Vulnerability check:**
```bash
nmap --script vuln 192.168.1.1
```

**Complete scan saved to file:**
```bash
nmap -A -oA my_scan 192.168.1.1
```

---

## 🔧 Common Fixes

**"Permission denied"**
```bash
sudo nmap -sS 192.168.1.1
```
Use `sudo` before the command.

---

**"Host seems down"**
```bash
nmap -Pn 192.168.1.1
```
Add `-Pn` to skip ping check.

---

**Scan is too slow**
```bash
nmap -T4 -F 192.168.1.1
```
Use `-T4` for faster timing and `-F` for fewer ports.

---

**Can't understand the output**
```bash
nmap -vv --reason 192.168.1.1
```
Add `-vv` for verbose and `--reason` to explain port states.

---

**UDP scan is stuck**
```bash
sudo nmap -sU -F -p 53,161 192.168.1.1
```
Use `-F` or specify exact ports to speed it up.

---

## ⚖️ Legal Reminder

✅ Your own devices · ✅ Your home network · ✅ With written permission · ✅ Lab/test environments

❌ Other people's networks · ❌ Public servers without permission · ❌ Anything with malicious intent

---

## 📚 Resources

- [Official Nmap Docs](https://nmap.org/book/man.html)
- [NSE Script Library](https://nmap.org/nsedoc/)
- [Practice legally on HackTheBox](https://www.hackthebox.com/)

---

## 🤝 Contributing

Found a mistake or want to add a command? Open a PR!

## 📄 License

MIT License — feel free to use and share.
