# TryHackMe — Cybersecurity 101

**Path:** Cyber Security 101  
**Platform:** TryHackMe  
**Completed:** April 2025  
**Difficulty:** Beginner  

---

## Overview

Cybersecurity 101 is TryHackMe's foundational learning path covering both offensive and defensive security concepts, OSINT/search skills, and hands-on labs simulating real attacker and defender scenarios.

---

## Module 1 — Offensive Security Intro

**Concept:** Offensive security means thinking like an attacker — finding weaknesses before real threat actors do.

### What I did
- Used a browser-based lab to find a hidden admin page on a target website by guessing common paths (e.g. `/admin`, `/administrator`)
- Performed a simulated brute force attack against the admin login panel using a wordlist
- Successfully logged in as admin and retrieved the flag

### Key takeaways
- Admin pages are often left at default paths — directory enumeration is one of the first things real attackers do
- Weak or default credentials are still one of the most common initial access vectors
- Tools like **Gobuster** and **Dirb** automate this in real engagements

---

## Module 2 — Defensive Security Intro

**Concept:** Defensive security focuses on monitoring, detecting, and responding to attacks — the core of SOC work.

### What I did
- Reviewed simulated SIEM alerts and logs to identify suspicious activity
- Applied the **5 Ws framework** (What, When, Where, Who, Why) to triage an alert
- Identified the attack type from log patterns
- Escalated the incident appropriately and "stopped" the attack within the lab

### Key takeaways
- The 5 Ws framework is how real SOC Level 1 analysts structure their initial triage
- Not every alert is malicious — context (like a scheduled vulnerability scan) determines severity
- Detection without response is useless; both must work together

### SOC Analyst workflow practiced
```
Alert triggered → Review logs → Apply 5 Ws → Determine malicious/benign → Escalate or close
```

---

## Module 3 — Search Skills

This module covered how to find reliable technical information quickly — a critical skill for both attackers and defenders.

### Tools covered

**Shodan** — `shodan.io`  
Search engine for internet-connected devices. Used to find exposed services, open ports, and vulnerable systems without touching the target.  
Example use: Search `apache 2.4.49` to find servers running a specific vulnerable version.

**VirusTotal** — `virustotal.com`  
Scans files, URLs, IPs, and hashes against 70+ antivirus engines.  
Used by SOC analysts to quickly check if an indicator (hash, IP, domain) is known-malicious.

**CVE / NVD (Vulnerability Databases)**  
- CVE format: `CVE-YEAR-NUMBER` (e.g. `CVE-2024-3094`)
- CVEs standardize how vulnerabilities are identified across vendors, researchers, and defenders
- `nvd.nist.gov` provides CVSS scores and remediation guidance
- **Exploit-DB** hosts verified exploit code for known CVEs

**Man Pages (Technical Documentation)**  
- Linux/Unix: `man <command>` — the built-in manual for any tool
- Example: `man netstat` shows all flags including `-b` (shows executable per connection on Windows)
- Essential for understanding tool options without Googling every flag

**GitHub**  
- Used to find proof-of-concept (PoC) exploit code, security research, and tool documentation
- Also relevant for finding exposed credentials and secrets accidentally pushed to public repos (a common OSINT technique)

### Key takeaways
- Good search skills save hours — knowing where to look matters more than memorizing syntax
- `CVE` databases are the shared language of the security industry; every SOC analyst references them daily
- Shodan is passive recon — you're not touching the target, just querying public data
- VirusTotal is the fastest first check for any suspicious indicator

---

## Reflection

This path gave me a concrete feel for both sides of the attacker/defender divide. The offensive lab (finding and attacking the admin page) made the defensive module more meaningful — I understood exactly what attack patterns I was looking for in the logs because I had just simulated them.

The search skills module is underrated. Knowing how to use Shodan, NVD, and man pages efficiently is something I'll use in every investigation.

**Next rooms:** Linux Fundamentals 1 → Networking Fundamentals → Wireshark Basics → Intro to SIEM
