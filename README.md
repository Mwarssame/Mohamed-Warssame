
🧑‍🏫 About Me : Mohamed Warssame ( Hackney)

I'm a **Network | Cloud & Cybersecurity | Consultant |Technologist** with a passion for building resilient, secure systems and teaching what I learn.

 🛠️ Skills & Mindset:
 
Cybersecurity Fundamentals, Monitoring & Tooling (e.g., SolarWinds). Defensive Security & Cloud-First Security Architectures.
Access and Identity Management (IAM) – including  (RBAC), SSO, and MFA across hybrid and cloud environments.
Zero Trust Architecture, SASE, and Network Access Control.
Next-Generation Firewalls (NGFWs) and  Application-aware identity-based access control.
Routing & Switching, including OSPF, BGP and MPLS.**- Knowing the Network is Knowing What We Need to Secure -we can’t protect what we don’t understand.**
**"Don’t ask what an asset is — ask how to protect it.**
**Don’t ask what a risk is — ask how to prevent it.**
**Don’t ask what a threat is — ask how to stop it.** "Memorising the names doesn’t protect infrastructures — taking action does".

Infrastructure as Code (IaC) with Terraform, and CI/CD pipelines automation.
Automate Configuration Deployment with Ansible.
TLS (Transport Layer Security) for secure communications.802.1X Network Access Control for port-based authentication.
Data Protection in the Modern Era: GDPR, NIST Guidelines, and Best Practices. Including Data classification and inventory management
- Encryption, access controls-  data minimisation  and Data Anonymisation Strategiess. 
- Incident response and breach notification processes
- Employee training and awareness programs

I strive to learn what I do not know, and practice what I know — continuously evolving as a security technologist and network professional.
- 📚 Lifelong learner & mentor — active in tech communities since 2006
- 🧰 Vendors and tools I work with: Cisco, Meraki, F5, Juniper,  Palo Alto, Wireshark, AWS, Azure, Linux, Terraform and  Ansible
- 🌱 Currently learning: Kubernetes security & threat hunting on sensitive applications
  
- ✍️ I write articles on network defence and automation.
- Active since 2006 — never stepped away from the field
- Recognised as both a learner and teacher
- Passionate about knowledge sharing, automation, and resilient architecture
  
🚀 **Key Projects & Achievements (2021–2024)**

- **Mitigated Log4j vulnerability across production environments.**
- **Upgraded 54 Next-Generation Firewalls to strengthen perimeter security.**
- **Designed and tuned SOAR & XSIAM platforms for automated detection and response.**
-**Built incident response playbooks and integrated threat intelligence with live systems.**
- **Streamlined SIEM and SOC workflows for faster triage and resolution.**
- **Deployed SolarWinds for enterprise-grade cloud monitoring.**
- **Refreshed Cisco LAN infrastructure by deploying Cisco DNA Centre and Cisco SD-Access, replacing legacy switching for cloud readiness, automation, and  network segmentation.**
- **Deployed Meraki MS switches, MR access points, and MX security appliances across seven office locations.**.
- **Moved and migrated 120 sites to AWS cloud  and Azure environment, enabling scalable, secure, and modernised operations.**
- **Memory Forensics & Vulnerability Management.**
- **Prepared High-Level Design (HLD) and High-Level Planning (HLP) documentation, as well as knowledge articles..**

📫....---

📫 **Full Network and Cybersecurity Forensics toolkit coming soon..**  
Stay tuned for in-depth guides, real-world use cases, and hands-on tools.

🧪 For Now, Let Me Share a Little Project on Memory Forensics

# 🧠 Memory Forensics & Vulnerability Management Toolkit

This project is a curated quick-reference guide and hands-on toolkit that integrates **memory forensics** with core **vulnerability management** practices. It’s designed for security professionals, incident responders, and learners seeking to bridge practical forensics with risk reduction strategies.  The project that was successfully completed 

---


🛡️ Vulnerability Management Framework

Integrated forensics into a structured vulnerability management workflow:

Asset Discovery –  we started  with Inventory  hardware, software, and ended with  network assets listing.

Vulnerability Scanning –  we Identified and classified  vulnerabilities into categories.

Vulnerability Analysis & Ranking – We Prioritised based on severity and business impact.

Remediation Planning – Applied patches and recommended  mitigations.

Patch Testing & Deployment – Verified and  patched instances in pre-production environment and  applied stable versions to productions

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
```Powershell
# Top memory-consuming processes
Get-Process | Sort-Object -Property WorkingSet -Descending | Select-Object -First 10 Name, Id, CPU, WorkingSet

example only!

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

live DNS traffic captured by tshark on a live endpoint.
 tshark -i 6 -f "udp port 53" -Y "dns"
  1   0.000000 172.20.10.41 → 8.8.8.8  DNS 90 Standard query 0x2094 A self.events.data.microsoft.com
    2   0.027596 8.8.8.8 → 172.20.10.41 1 DNS 213 Standard query response 0x2094 A self.events.data.microsoft.com CNAME self-events-data.trafficmanager.net CNAME onedscolprdneu04.northeurope.cloudapp.azure.com A 20.50.73.10    [ a none production test machine to simulate production environment]

what about BBC.

 tshark -i 6 -Y "dns.qry.name contains bbc.co.uk"
Capturing on 'WiFi'
 1670  49.724700 172.20.10.41 → 208.67.222.222 DNS 69 Standard query 0xe04f A bbc.co.uk
 1671  49.745723 8.8.8.8 → 172.20.10.41 DNS 133 Standard query response 0xe04f A bbc.co.uk A 151.101.64.81 A 151.101.128.81 A 151.101.192.81 A 151.101.0.81
The DNS server replies with a DNS response:
We see  several IP addresses for bbc.co.uk (there are multiple IPs for load balancing right as shown below

= 151.101.64.81
- 151.101.128.81
- 151.101.192.81
- 151.101.0.8

We applied the same method used for the BBC to Google and captured the results using:
tshark -i 6 -Y "dns.qry.name contains google.com"

IPv6 (AAAA) addresses for www.google.com
:
2a00:1450:4009:c15::63
2a00:1450:4009:c15::67
2a00:1450:4009:c15::6a
2a00:1450:4009:c15::93
IPv4 (A) addresses for google.com:

142.250.129.101
142.250.129.102
142.250.129.113
142.250.129.138
142.250.129.139
142.250.129.10

Capture Traffic for a Single IP Address Using TShark
> tshark -i 6 -f "host 142.250.129.101"

    1   0.000000 172.20.10.41 → 142.250.129.101 TCP 66 9485 → 80 [SYN] Seq=0 Win=64240 Len=0 MSS=1460 WS=256 SACK_PERM (Client → Server: SYN to port 80 (start connection))
    2   0.000288 172.20.10.41 → 142.250.129.101 TCP 66 9486 → 80 [SYN] Seq=0 Win=64240 Len=0 MSS=1460 WS=256 SACK_PERM (Client → Server: SYN to port 80 (another attempt/similar)
    3   0.003591 172.20.10.41 → 142.250.129.101 TCP 66 9487 → 443 [SYN] Seq=0 Win=64240 Len=0 MSS=1460 WS=256 SACK_PERM (Client → Server: SYN to port 443 (HTTPS connection start)
    4   0.021059 142.250.129.101 → 172.20.10.41 TCP 66 80 → 9485 [SYN, ACK] Seq=0 Ack=1 Win=65535 Len=0 MSS=1412 SACK_PERM WS=256  (Server → Client: SYN, ACK acknowledging connection)
    5   0.021262 172.20.10.41 → 142.250.129.101 TCP 54 9485 → 80 [ACK] Seq=1 Ack=1 Win=66304 Len=0  Client → Server: ACK (connection established)

Tips: 

The TCP connection was successfully established (you saw the 3-way handshake complete).
But no actual data was transferred yet, as indicated by **Len=0** in all packets shown.

**Volatility Example**

volatility -f memory.dmp --profile=Win10x64 pslist
volatility -f memory.dmp --profile=Win10x64 malfind
volatility -f memory.dmp --profile=Win10x64 netscan
volatility -f memory.dmp --profile=Win10x64 netscan

**BGP Troubleshooting Command Reference – CLI tools for verifying BGP behaviour when rolling out new projects or making changes in existing network environments.**


*Show detailed info for a specific BGP neighbor.*
show ip bgp neighbors <neighbor-IP> advertised-routes | include <prefix>
*Show routes advertised to a neighbor filtered by prefix.*
show ip bgp neighbors <neighbor-IP> received-routes | include <prefix>

*Show routes received from a neighbor filtered by prefix.*
show ip bgp neighbors <neighbor-IP> advertised-routes | include *>
*Show advertised active BGP paths to a neighbor.*
show ip bgp <prefix> | include AS_PATH|Next Hop

*Display BGP path attributes for a prefix.*
show ip prefix-list | include <prefix or permit|deny>
*Filter BGP prefix-lists by prefix or action.*
show route-map | section <route-map-name>

*Show route-map entries relevant to BGP policies.*
show ip bgp neighbors | include Idle|Active|Estab
*Filter BGP neighbor session states.*
show ip bgp neighbors | include update
*Check BGP neighbors’ update counts.*


# 🔐 **Cisco 802.1X + ISE Troubleshooting Commands (with `|` Pipes)**

**Useful CLI commands on Cisco switches integrated with Cisco ISE to diagnose and monitor 802.1X authentication issues.**


## 1. Show all active authentication sessions  
show authentication sessions | include Gi|Dot1x

View all authenticated interfaces and methods (802.1X, MAB).

## 2. Detailed session info for a specific port  
show authentication sessions interface Gi1/0/5 | include Authc|VLAN|Status

Check authentication method, VLAN assignment, and status on a port.


## 3. Check ISE dynamic VLAN assignment  
show authentication sessions interface Gi1/0/5 | include VLAN

Verify if ISE dynamically assigned a VLAN after authentication.

## 4. Check method used (MAB vs Dot1X)  
show authentication sessions interface Gi1/0/5 | include Method

Ensure correct authentication method was applied.


## 5. Filter logs for ISE/RADIUS-related events  
show logging | include RADIUS|DOT1X|ISE

Quickly spot issues related to 802.1X and ISE in the log buffer.

## 6. Check interface state and port control config  
show run interface Gi1/0/5 | include auth|mab|switchport
Audit interface for correct dot1x, MAB, and switchport config.

## 7. See MAC address learned on interface  
show mac address-table interface Gi1/0/5 | include DYNAMIC

Confirm whether the endpoint's MAC address was learned post-auth.

## 8. Display radius-server configuration  
show run | section radius-server

Ensure correct ISE IP address, key, and config are applied.
## 9. Check session authorization results  
show authentication sessions interface Gi1/0/5 details | include Server

See what result the RADIUS server (ISE) returned to the switch.

## 10. View authentication failures in logs  
show logging | include FAIL|REJECT

Identify failed authentications for fast troubleshooting.
## Bonus Tips but Warning!!

- Use `debug dot1x all`but DO NOT run during ther busy business hours  on production devices.
