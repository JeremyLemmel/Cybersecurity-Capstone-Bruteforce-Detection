# Cybersecurity Capstone – Brute Force Attack & Detection Lab

**Project Overview**  
Complete end-to-end cybersecurity capstone demonstrating a realistic attack chain from reconnaissance to detection and response.   
Built using Kali Linux, Windows Server 2022, Splunk Enterprise, and standard attack tools.

## Project Presentation

[View Slideshow](https://docs.google.com/presentation/d/1LjdieB9Yyt7OIYYlxTGCALNGnXVWld1dYYuKjPCw0Sw/edit?usp=sharing)

*(Google Slides - April 2026)*

## Technologies Used
- Kali Linux (Attacker + Splunk Server)
- Windows Server 2022 (Victim with Universal Forwarder)
- Splunk Enterprise 9.4.3
- Tools: netdiscover, nmap, Hydra, xfreerdp

## Lab Architecture

<img width="1536" height="1024" alt="lab enviro pic" src="https://github.com/user-attachments/assets/f0cfcc76-c148-4965-a46b-39f733fbba08" />

## Attack Chain Summary
1. Reconnaissance → netdiscover  
2. Scanning → nmap  
3. Exploitation → Hydra RDP brute-force  
4. Gaining Access → xfreerdp successful login  
5. Detection → Splunk SIEM real-time alerts  
6. Response → Block attacker IP in Windows Firewall

## Repository Contents

| Folder / File                              | Description |
|--------------------------------------------|-----------|
| `Lab-Rebuild-Guide/Lab-Rebuild-Guide.md`   | Step-by-step instructions to rebuild the entire lab environment after VM resets |
| `Recon/Netdiscover_nmap.md`                | Reconnaissance phase using netdiscover and nmap |
| `Attack-Chain/Attack-Chain.md`             | Overview of the full attack chain |
| `Attack-Chain/Hydra_commands.md`           | Detailed Hydra brute-force commands |
| `Attack-Chain/Xfreerdp_commands.md`        | Commands and usage for xfreerdp successful login |
| `Detection/Splunk-Dashboard.md`            | Real-time Splunk dashboard panels and visualizations |
| `Detection/Splunk_queries.md`              | All Splunk SPL searches used in the project |
| `Defense/Firewall_rules.md`                | Windows Defender Firewall rules and blocking procedures |
| `Reporting/Incident-Response-Report.md`    | Sample Tier 1 SIEM analyst incident report |
| `Evidence/`                                | Screenshots and visual evidence of the full attack chain |
| `Evidence/README.md`                       | Description of screenshots in the Evidence folder |



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
