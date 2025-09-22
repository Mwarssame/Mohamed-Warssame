
🧑‍🏫 About Me
I'm a **Network & Security Technologist** with a passion for building resilient, secure systems and teaching what I learn.

- 🔐 Cybersecurity, Cloud Security, Zero Trust Architectures
- 🛠️ Skilled in firewalls, IDS/IPS, automation tools, and cloud infrastructure 
- 📚 Lifelong learner & mentor — active in tech communities since 2020
- 🧰 Tools I work with: Cisco, Palo Alto, Wireshark, AWS, Linux, Ansible
- 🌱 Currently learning: Kubernetes security & threat hunting
- ✍️ I write articles on network defense and automation.
- Active since 2020 — never stepped away from the field
- Recognised as both a learner and teacher
- Passionate about knowledge sharing, automation, and resilient architecture

📫....---

📫 **Full Network and Cybersecurity Forensics toolkit coming soon...**  
Stay tuned for in-depth guides, real-world use cases, and hands-on tools.

🧪 For Now, Let Me Share a Little Project on Memory Forensics

# 🧠 Memory Forensics & Vulnerability Management Toolkit

This project is a curated quick-reference guide and hands-on toolkit that integrates **memory forensics** with core **vulnerability management** practices. It’s designed for security professionals, incident responders, and learners seeking to bridge practical forensics with risk reduction strategies.  The project that was successfuly completed 

---


🛡️ Vulnerability Management Framework

Integrated forensics into a structured vulnerability management workflow:

Asset Discovery – Inventory all hardware, software, and network assets.

Vulnerability Scanning – Identify and classify vulnerabilities.

Vulnerability Analysis & Ranking – Prioritize based on severity and business impact.

Remediation Planning – Apply patches or mitigations.

Patch Testing & Deployment – Verify patch safety and stability.

Verification & Monitoring – Continuous scanning and tracking over time.

🔐 Aligned with information security principles:

Confidentiality, Integrity, Availability

Non-repudiation: Ensuring origin and integrity of forensic data


 🔍 Memory Forensics Highlights

I Used and documented key tools for memory analysis and live acquisition:
Examples:

- **Volatility** – Extract processes, DLLs, drivers, registry, and network data from memory dumps.
- **Rekall** – Fast, plugin-based memory analysis; useful for timeline generation and malware hunting.
- **FTK Imager** – GUI-based imaging tool that captures live RAM.
- **LiME** – Linux kernel module for acquiring physical RAM dumps.
- **Redline (FireEye)** – GUI-based forensics tool for IOC scanning and malware detection.
- **WinDbg** – Microsoft debugger for user and kernel-mode memory dump analysis.
- **Belkasoft RAM Capturer**, **DumpIt**, **Memdump** – Lightweight tools for field memory acquisition.

### 🧪 PowerShell & CLI Integration
```powershell
# Top memory-consuming processes
Get-Process | Sort-Object -Property WorkingSet -Descending | Select-Object -First 10 Name, Id, CPU, WorkingSet

examplea only!

Name                Id         CPU WorkingSet
----                --         --- ----------
chrome           20256  1382.84375  300109824
chrome            7348  2320.40625  248123392
firefox           7204   94.609375  242147328
explorer         11632  5119.34375  204382208
firefox           9436  578.953125  204263424
chrome           26396  115.015625  188690432
firefox          16120    50.21875  178356224
chrome           15308    2953.125  161460224
chrome           13848   303.90625  151748608


# Get executable path of a process and Retrieves the process with the Process ID (PID) 7204 for FireFox

Get-Process -Id 7204 | Select-Object Path

Path
----
C:\Program Files\Mozilla Firefox\firefox.exe

Get-Process -Name firefox | Select-Object Id, Name, Path, CPU, StartTime
**Id        : 7204**
Name      : firefox
Path      : C:\Program Files\Mozilla Firefox\firefox.exe
CPU       : 103.6875
StartTime : 21/09/2023 19:00:51

**Volatility Example**

volatility -f memory.dmp --profile=Win10x64 pslist
volatility -f memory.dmp --profile=Win10x64 malfind
volatility -f memory.dmp --profile=Win10x64 netscan
volatility -f memory.dmp --profile=Win10x64 netscan


