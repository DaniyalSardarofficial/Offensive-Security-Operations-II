# 🛡️ Offensive Security Operations II (CIP-A105)
### Summative Competency Examination Portfolio · ICDFA Academy

<p align="center">
  <img src="https://img.shields.io/badge/Student-Daniyal_Ahmed-blue?style=for-the-badge" alt="Student"/>
  <img src="https://img.shields.io/badge/Reg_No-C11%2F26%2FEHIT%2F17331-navy?style=for-the-badge" alt="Reg No"/>
  <img src="https://img.shields.io/badge/Course-CIP--A105-informational?style=for-the-badge" alt="Course"/>
  <img src="https://img.shields.io/badge/Classification-Training_Use_Only-critical?style=for-the-badge" alt="Classification"/>
</p>

---

## 📌 Repository Overview

This repository contains the complete, authoritative assessment deliverables for **Offensive Security Operations II (CIP-A105)** at the **ICDFA Academy**. 

The coursework entails two independent, black-box penetration testing operations conducted in strictly isolated virtual laboratory segments (VirtualBox / VMware Host-Only networks with zero internet routability). Each engagement progressed from unauthenticated host discovery to full administrative (`root`) system compromise, accompanied by comprehensive technical reporting, risk registers, executive briefings, and photographic evidence.

---

## ⚔️ Operations Matrix & Summary

| Operational Area | CTF 1: Operation Iron Raven | CTF 2: Operation Black Forge |
|:-----------------|:-----------------------------|:------------------------------|
| **Target Host** | `OPFOR-01` (192.168.233.129) | `OPFOR-02` (192.168.233.130) |
| **Operating System** | Debian Jessie Linux | PCLinuxOS 2011 (Linux 2.6.38) |
| **Primary Vectors** | PHPMailer 5.2.16 RCE (CVE-2016-10033) | OpenEMR 4.1.0 Blind SQLi (EDB-49742) |
| **Foothold Service** | Apache 2.4.10 / WordPress / Contact Form | Apache 2.2.17 / OpenEMR Healthcare Portal |
| **Credential Vectors** | MySQL Database Hash Extraction | SQLi Dump `openemr.users` & MD5 Cracking |
| **Code Execution** | Python Exploit (EDB-40974) \u2192 Web Shell | OpenEMR `config.php` Admin File Editor \u2192 Reverse Shell |
| **Privilege Escalation**| MySQL User-Defined Function (UDF) & SUID `find` | SUID Binary Relative Call (PATH Environment Hijacking) |
| **Compromise Level** | **Full Root Shell (`root@raven`)** | **Full Root Shell (`root@localhost`)** |
| **Mission Proofs** | 4/4 Flags Captured (`flag1` \u2013 `flag4`) | Root Proof Hash (`eaff25eaa9ffc8b62e3dfebf70e83a7b`) |
| **Folder Link** | [📂 View CTF-01 Directory](./CTF-01_Operation-Iron-Raven/) | [📂 View CTF-02 Directory](./CTF-02_Operation-Black-Forge/) |

---

## 🗂️ Project Directory Structure

```text
Offensive-Security-Operations-II/
│
├── 📁 CTF-01_Operation-Iron-Raven/
│   ├── 📄 Operation_Iron_Raven_Report.pdf     # 83-Page Full Technical Report (12 Sections)
│   ├── 📊 Executive_Report.pdf                # Executive Leadership Briefing
│   ├── 📋 Risk_Register.pdf                   # 7 Confirmed Findings (Card-per-finding format)
│   ├── 📝 Lessons_Learned.pdf                 # Reflective Technical & Operational Analysis
│   ├── 📜 ROE_Acknowledgement.pdf             # Signed Rules of Engagement Compliance Record
│   ├── 🖼️ network_topology.jpg                # Isolated VMnet1 Subnet Architecture
│   ├── 🖼️ attack_chain.jpg                    # 7-Phase Attack Kill Chain Diagram
│   └── 📖 README.md                           # Detailed CTF-01 Technical Overview & Flags
│
├── 📁 CTF-02_Operation-Black-Forge/
│   ├── 📄 Operation_Black_Forge_Report.pdf    # 50-Page Full Technical Report (12 Sections)
│   ├── 📊 Executive_Report.pdf                # Executive Leadership Briefing
│   ├── 📋 Risk_Register.pdf                   # 6 Confirmed Findings (Card-per-finding format)
│   ├── 📝 Lessons_Learned.pdf                 # Reflective Technical & Operational Analysis
│   ├── 🖼️ network_topology.jpg                # Isolated VirtualBox Host-Only Subnet Architecture
│   ├── 🖼️ attack_chain.jpg                    # 7-Phase Attack Kill Chain Diagram
│   └── 📖 README.md                           # Detailed CTF-02 Technical Overview & Root Proof
│
└── 📖 README.md                               # Master Repository Index & Course Portfolio
```

---

## 🎯 Core Competencies Demonstrated

- **Disciplined Network Enumeration**: Host discovery and port fingerprinting using `nmap`, `arp-scan`, `fping`, and custom protocol probes within strict network boundaries.
- **Web Application Penetration Testing**: Deep directory enumeration (`dirb`, `gobuster`), parameter vulnerability testing, and exploitation of both remote code execution (PHPMailer) and structured injection (Blind SQL Injection via `sqlmap`).
- **Cryptanalytic Assessment**: Offline hash identification, parsing using Unix pipeline utilities (`awk`, `column`), and dictionary/rainbow-table decryption of password digests.
- **Post-Exploitation & Linux Internal Auditing**: File system permission auditing, administrative portal pivoting, weaponisation of built-in application configuration utilities, and environment profiling.
- **Privilege Escalation**: Exploitation of misconfigured SUID binaries via Unix `PATH` variable manipulation and shared object injection (MySQL UDF dynamic libraries).
- **Professional Reporting & Risk Management**: Publication of executive briefings, technical write-ups, and risk registers aligned with industry standards (CVSS scoring, actionable remediation roadmaps).

---

## ⚖️ Academic Integrity & Disclaimer

All testing conducted and documented within this repository was performed strictly under an authorised Academic Rules of Engagement (ROE) charter issued by the **Directorate of Training, ICDFA Academy**. 

- All target appliances operated within private, non-routable virtual segments (`192.168.233.0/24`).
- No public networks, production infrastructures, or unapproved third-party systems were engaged.
- Sensitive authentication secrets and user hashes have been redacted in public report documentation where appropriate.

```text
"Think before you act. Verify before you claim. Preserve evidence. Remain inside scope. Complete the mission without being given the path."
```

---

<p align="center">
  <b>Daniyal Ahmed</b> · Registration: <code>C11/26/EHIT/17331</code><br/>
  Offensive Security Operations II · CIP-A105 · September 2026
</p>
