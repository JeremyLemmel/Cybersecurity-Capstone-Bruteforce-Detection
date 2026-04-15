# Cybersecurity Capstone – Brute Force Attack & Detection Lab

**Project Overview**  
Complete end-to-end cybersecurity capstone demonstrating a realistic attack chain from reconnaissance to detection and response.   
Built using Kali Linux, Windows Server 2022, Splunk Enterprise, and standard attack tools.

## Technologies Used
- Kali Linux (Attacker + Splunk Server)
- Windows Server 2022 (Victim with Universal Forwarder)
- Splunk Enterprise 9.4.3
- Tools: netdiscover, nmap, Hydra, xfreerdp

## Lab Architecture

```ascii
┌─────────────────────────────────────────────────────────────┐
│                     Lab Environment                         │
│                                                             │
│   ┌──────────────────┐          ┌──────────────────────────┐  │
│   │   Kali Linux     │◄─────────│ Windows Server 2022      │  │
│   │ (Attacker + SIEM)│   Logs   │       (Victim)           │  │
│   │                  │          │                          │  │
│   │ • Splunk 9.4.3   │          │ • RDP (3389)             │  │
│   │ • Netdiscover    │          │ • SMB (445)              │  │
│   │ • Nmap           │          │ • Universal Forwarder    │  │
│   │ • Hydra          │          │   (port 9997)            │  │
│   │ • xfreerdp       │          └────────────┬─────────────┘  │
│   └──────────────────┘                       │                │
│                                              │                │
│                                   Security Logs                │
│                                              │                │
│                                              ▼                │
│                               ┌──────────────────────────┐  │
│                               │      Splunk Enterprise    │  │
│                               │       (on Kali)           │  │
│                               │   • index=main            │  │
│                               │   • Real-time Dashboard   │  │
│                               └──────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
````
## Attack Chain Summary
1. Reconnaissance → netdiscover  
2. Scanning → nmap  
3. Exploitation → Hydra RDP brute-force  
4. Gaining Access → xfreerdp successful login  
5. Detection → Splunk SIEM real-time alerts  
6. Response → Block attacker IP in Windows Firewall

## Repository Contents
- **Lab-Rebuild-Guide.md** – Full daily rebuild instructions
- **Attack-Chain.md** – Detailed attack walkthrough
- **Splunk-Dashboard.md** – All searches and dashboard panels
- **Incident-Response-Report.md** – Sample Tier 1 analyst report
- **Evidence/** – Screenshots of attacks and Splunk dashboard

## Key Learnings

- Built a full SIEM environment from scratch including log forwarding pipeline
- Simulated real-world attack techniques across the full kill chain
- Created real-time Splunk dashboards and automated threshold alerts
- Practiced both Red Team offensive techniques and Blue Team detection/response
- Developed hands-on experience with EventID correlation (4625 → 4624 pattern)


## Quick Start
See `Lab-Rebuild-Guide.md` for complete setup instructions.

**Demo Video:** [Link will go here]


**Project completed April 2026**  

---

## ⚠️ Disclaimer

> All attacks were performed in an **isolated virtual machine environment** for **educational purposes only**. No real systems were targeted. This project is intended to demonstrate SOC analyst skills in a controlled lab setting.
