# Network-Defense

# 🛡️ Cybersecurity Blue Team Lab

## Overview

This lab is designed to simulate **realistic cyber attacks** on both **endpoints** and **network environments** in order to develop and demonstrate **Blue Team detection, analysis, and response skills**. It provides a hands-on platform to practice identifying, investigating, and mitigating threats using industry-standard tools and frameworks.

---

## 🎯 Objectives

- Simulate endpoint-based attacks (e.g., privilege escalation, process injection, credential access)
- Simulate network-based attacks (e.g., port scanning, man-in-the-middle, data exfiltration)
- Use security tools to detect and respond to threats in real-time
- Build and tune detection rules, dashboards, and alerts
- Gain hands-on experience with logs, events, and forensic data

---

## 🧰 Tools & Technologies Used

| Category        | Tools/Technologies                  |
|----------------|--------------------------------------|
| Endpoint Security | Sysmon, Wazuh Agent, Windows Event Logs |
| Network Monitoring | Wireshark, Suricata, tcpdump       |
| SIEM/Log Analysis | Wazuh, ELK Stack (Elasticsearch, Logstash, Kibana) |
| Offensive Simulation | Kali Linux, Metasploit, mimikatz, PowerSploit |
| Detection Frameworks | MITRE ATT&CK, Sigma Rules         |
| Virtualization | VMware Workstation / Fusion          |

---

## 🔬 Lab Topology

- **Ubuntu VM**: Wazuh Manager + ELK Stack
- **Windows 10/11 VM**: Victim endpoint with Wazuh agent
- **Kali Linux VM**: Attacker machine for red team simulations
- **Optional Router**: Isolated lab environment, no internet access

---

## 📌 Example Simulated Attacks

| Category | Technique | MITRE ID |
|---------|-----------|----------|
| Privilege Escalation | `runas`, `whoami`, `mimikatz.exe` | T1055, T1003 |
| Reconnaissance | `netstat`, `systeminfo`, `arp -a` | T1087, T1016 |
| Network Discovery | `nmap`, `arp-scan` | T1046 |
| Lateral Movement | RDP login attempts, shared folder access | T1021 |
| Malware Execution | `nc.exe`, obfuscated PowerShell scripts | T1059 |
| File Integrity | Create/edit/delete sensitive files | N/A |

---

## ✅ Blue Team Focus Areas

- **Log Collection & Analysis**: Forward logs to Wazuh and analyze alerts
- **Detection Engineering**: Write custom rules for suspicious processes and behavior
- **Alert Tuning**: Reduce false positives, increase detection accuracy
- **Forensics & Investigation**: Examine Sysmon, Event Logs, PCAPs
- **Dashboards**: Create visualizations in Kibana for SOC-style monitoring

---

## 🛠️ Getting Started

1. Clone this repository and review lab documentation
2. Deploy VMs and set up networking (bridge or host-only)
3. Install and configure Wazuh Manager + agent
4. Run simulated attacks from Kali to Windows
5. Review alerts, logs, and detection outputs in Kibana

---

## 📂 Folder Structure

```bash
cyber-blue-team-lab/
├── configs/                  # Wazuh and Sysmon config files
├── rules/                    # Custom detection rules
├── scripts/                  # Attack simulation scripts (PowerShell, batch)
├── logs/                     # Sample logs and PCAPs
├── dashboards/               # Kibana dashboards (JSON exports)
├── reports/                  # Summary of exercises and detections
└── README.md
