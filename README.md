# Threat Detection & Incident Response Lab with Splunk and SOAR

[![Splunk](https://img.shields.io/badge/Tool-Splunk-black?logo=splunk)](https://www.splunk.com/)
[![SOAR](https://img.shields.io/badge/Tool-Splunk%20SOAR-black?logo=splunk)](https://www.splunk.com/en_us/software/soar.html)
[![Python](https://img.shields.io/badge/Language-Python-blue?logo=python)](https://www.python.org/)
[![PowerShell](https://img.shields.io/badge/Scripting-PowerShell-blue?logo=powershell)](https://learn.microsoft.com/en-us/powershell/)
[![Sysmon](https://img.shields.io/badge/Tool-Sysmon-blue)](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
[![Winlogbeat](https://img.shields.io/badge/Tool-Winlogbeat-orange)](https://www.elastic.co/beats/winlogbeat)
[![MITRE ATT&CK](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-red)](https://attack.mitre.org/)
[![VirusTotal](https://img.shields.io/badge/Threat%20Intel-VirusTotal-black)](https://www.virustotal.com/)
[![AbuseIPDB](https://img.shields.io/badge/Threat%20Intel-AbuseIPDB-red)](https://www.abuseipdb.com/)

---

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Objectives](#objectives)
- [Key Achievements](#key-achievements)
- [Skills Demonstrated](#skills-demonstrated)
- [Lab Design Overview](#lab-design-overview)
- [Detection & Response Workflow](#detection--response-workflow)
- [Repository Structure](#repository-structure)
- [Recommendations for Future Enhancements](#recommendations-for-future-enhancements)
- [License](#license)

---

## Project Overview

This lab simulates real-world cybersecurity threats and demonstrates how to detect, investigate, and respond using **Splunk** as a SIEM and **SOAR** for automated workflows. Simulated attack scenarios generate rich host-level telemetry, while automated playbooks triage alerts and enrich findings using threat intelligence sources.

The project is designed to mirror real incident response operations and follows best practices aligned with frameworks like **MITRE ATT&CK** and **NIST**.

---

## Technologies Used

- **Splunk Enterprise (Trial)** – SIEM and log aggregation
- **Splunk SOAR (Community Edition)** – Automated playbook response
- **Sysmon + Winlogbeat** – Endpoint event generation and forwarding
- **Python / PowerShell** – Custom SOAR scripting and attack simulation
- **VirusTotal, AbuseIPDB** – Threat intelligence enrichment APIs
- **VirtualBox / VMs** – Windows and Linux virtual machines
- **MITRE ATT&CK Framework** – Attack mapping and detection planning

---

## Objectives

- Simulate real-world cyber attacks in a virtual lab
- Detect malicious behavior using Splunk dashboards and correlation rules
- Automate parts of the response process using SOAR playbooks
- Enrich indicators with threat intelligence sources
- Create reusable documentation and modular detection logic
- Map detection logic to ATT&CK tactics, techniques, and procedures (TTPs)
- Demonstrate compliance best practices (e.g., log retention policies)

---

## Key Achievements

- **Built a complete Splunk + SOAR detection and response pipeline**  
  *Aggregated logs using Winlogbeat and correlated them using custom queries and dashboards within Splunk.*

- **Mapped attack scenarios to MITRE ATT&CK TTPs**  
  *Simulated events like brute-force, lateral movement, and privilege escalation; each detection rule linked to corresponding ATT&CK tactics.*

- **Developed automated response playbooks using SOAR**  
  *Created modular Python and PowerShell scripts that enrich IPs, trigger alerts, and simulate containment.*

- **Integrated threat intelligence sources into investigation workflows**  
  *Connected SOAR actions to VirusTotal and AbuseIPDB for IOC reputation lookups.*

- **Documented detection logic and incident response workflows**  
  *Included markdown-based reports for each detection scenario, response logic, and playbook breakdown.*

---

## Skills Demonstrated

- **SIEM Engineering and Log Correlation**  
  *Built custom dashboards, detection queries, and alerting logic in Splunk.*

- **Incident Response and Attack Simulation**  
  *Manually triggered suspicious behavior in lab VMs and verified detection across Splunk and SOAR.*

- **Scripting and Automation**  
  *Developed scripts to perform lookups, isolate hosts, and generate structured responses.*

- **Security Documentation and Audit Readiness**  
  *Created detailed write-ups for detection methods, SOAR logic, and lab artifacts aligned with NIST controls.*

- **Threat Intelligence and IOC Enrichment**  
  *Queried reputation services to validate indicators and feed contextual data into alert workflows.*

- **Operating System Internals**  
  *Analyzed Sysmon logs for process execution, network connections, and file manipulations.*

---

## Lab Design Overview

- **Endpoint Logging**: Sysmon + Winlogbeat on Windows VMs, shipped to Splunk via HTTP Event Collector
- **SIEM**: Splunk queries and dashboards developed for detection scenarios (brute-force, suspicious logins, PowerShell abuse)
- **SOAR**: Splunk SOAR playbooks respond to specific alert types, with automated enrichment, tagging, and response simulation
- **Simulated Attacks**: Performed via PowerShell, Kali Linux, and native Windows tools
- **Threat Intelligence**: IOC lookups triggered via SOAR playbooks with external APIs

---

## Detection & Response Workflow

1. **Simulate Adversary Behavior**  
   - Brute-force, privilege escalation, and lateral movement via test scripts

2. **Log Forwarding and Ingestion**  
   - Winlogbeat sends data from endpoints to Splunk for indexing

3. **Correlation and Alerting**  
   - Splunk queries trigger alerts when suspicious patterns are observed

4. **SOAR Playbook Execution**  
   - Alerts forward to SOAR which enriches, logs, and simulates containment

5. **Documentation and Reporting**  
   - Manual or automated generation of incident reports and timelines

---

## Repository Structure
```
Threat-Detection-Lab/

├── detections/
│ ├── brute_force_detection.md
│ └── lateral_movement_query.md

├── playbooks/
│ ├── enrich_ip_playbook.py
│ └── isolate_host_playbook.ps1

├── attack-scenarios/
│ ├── simulate_brute_force.ps1
│ └── invoke_lateral_move.sh

├── threat-intel/
│ ├── virustotal_lookup.py
│ └── abuseipdb_check.py

├── documentation/
│ ├── incident_template.md
│ ├── MITRE_mapping.md
│ └── log_retention_policy.md

├── README.md
└── LICENSE
```

---

## Recommendations for Future Enhancements

- **Add full EDR telemetry** using Defender ATP or CrowdStrike Free Tier
- **Expand SOAR playbooks** for full incident lifecycle (containment, eradication, recovery)
- **Integrate alert ticketing** via ServiceNow or JIRA APIs
- **Automate IOC submissions** back to intelligence platforms
- **Build compliance dashboard** in Splunk for log retention and control alignment

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

