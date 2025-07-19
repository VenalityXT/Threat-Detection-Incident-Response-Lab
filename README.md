# Threat Detection & Incident Response Lab with Splunk and SOAR

[![Splunk](https://img.shields.io/badge/Tool-Splunk-black?logo=splunk)](https://www.splunk.com/)
[![SOAR](https://img.shields.io/badge/Tool-Splunk%20SOAR-black?logo=splunk)](https://www.splunk.com/en_us/software/soar.html)
[![Python](https://img.shields.io/badge/Language-Python-blue?logo=python)](https://www.python.org/)
[![PowerShell](https://img.shields.io/badge/Scripting-PowerShell-blue?logo=powershell)](https://docs.microsoft.com/en-us/powershell/)
[![Sysmon](https://img.shields.io/badge/Tool-Sysmon-blue)](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
[![Winlogbeat](https://img.shields.io/badge/Tool-Winlogbeat-orange)](https://www.elastic.co/beats/winlogbeat)
[![MITRE ATT&CK](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-red)](https://attack.mitre.org/)
[![VirusTotal](https://img.shields.io/badge/Threat%20Intel-VirusTotal-black)](https://www.virustotal.com/)
[![AbuseIPDB](https://img.shields.io/badge/Threat%20Intel-AbuseIPDB-red)](https://www.abuseipdb.com/)

---

## 📘 Overview

This project simulates real-world cyber threats in a controlled lab environment and demonstrates how to detect, investigate, and respond to them using **Splunk (SIEM)** and **SOAR (Security Orchestration, Automation, and Response)** tools. The lab incorporates endpoint logging, scripted automation, threat intelligence enrichment, and compliance alignment with security frameworks.

Each phase—from attack simulation to automated remediation—is supported by modular scripts and visualizations. A series of detailed sub-READMEs accompany this repository to explain the configurations, detection logic, and scripting methodologies used throughout the project.

---

## 🎯 Objectives

- Deploy a realistic detection and response environment.
- Simulate cyber attacks against Windows/Linux hosts.
- Correlate logs and detect malicious behaviors using Splunk.
- Automate investigation and response with SOAR playbooks.
- Enrich threat context via external intelligence sources.
- Map activities to the MITRE ATT&CK framework.
- Document procedures for reporting and compliance reviews.

---

## 🛠️ Skills Demonstrated

- **SIEM Monitoring & Log Correlation**  
  *Built dashboards and detection rules in Splunk using event correlation from Sysmon and Winlogbeat data.*

- **Incident Response & Threat Detection**  
  *Simulated adversary behaviors and manually triaged logs to identify indicators and alert patterns.*

- **Scripting & Automation**  
  *Developed Python and PowerShell-based SOAR playbooks to automate threat enrichment, ticketing, and response tasks.*

- **Security Documentation & Reporting**  
  *Generated incident response write-ups, detection signatures, and remediation workflows.*

- **Governance, Risk & Compliance**  
  *Applied mock retention policies and NIST-aligned compliance controls across the lab environment.*

- **MITRE ATT&CK Mapping**  
  *Mapped detection rules and alerting logic to relevant ATT&CK TTPs.*

- **Threat Intelligence Integration**  
  *Used VirusTotal and AbuseIPDB APIs to enrich indicators and confirm malicious activity.*

- **Operating System Internals**  
  *Executed and analyzed host-based attacks on both Windows and Linux to generate meaningful logs.*

---

## 🧭 Repository Structure
Threat-Detection-Lab/
├── detections/ # Custom correlation rules and search queries
│ ├── brute_force_detection.md
│ └── suspicious_login_alert.md
├── playbooks/ # SOAR playbooks (Python / PowerShell)
│ ├── enrich_ip_playbook.py
│ └── isolate_host_playbook.ps1
├── documentation/ # Reports, compliance artifacts, MITRE mappings
│ ├── incident_report_template.docx
│ └── log_retention_policy.md
├── attack-scenarios/ # Steps/scripts to simulate attacks on endpoints
│ ├── brute_force_simulation.sh
│ └── lateral_movement_scenario.ps1
├── threat-intel/ # Scripts and integrations for enrichment
│ └── virustotal_lookup.py
├── assets/ # [Insert Image Here] Diagrams, screenshots
│ └── splunk_dashboard_example.png
├── README.md # Project overview (this file)
└── detections/README.md # Detailed detection logic and rationale

---

## 🔎 Tools Used

- **SIEM**: Splunk Free or Splunk Cloud Trial  
- **SOAR**: Splunk SOAR Community Edition, Shuffle (optional)  
- **Endpoint Logging**: Sysmon + Winlogbeat  
- **Automation**: Python, PowerShell  
- **Threat Intelligence APIs**: VirusTotal, AbuseIPDB  
- **Compliance Frameworks**: NIST 800-53, MITRE ATT&CK

---

## 📌 Recommendations for Future Enhancements

- Integrate endpoint EDR solutions like CrowdStrike or Microsoft Defender ATP for enhanced telemetry.
- Expand SOAR playbooks to cover containment and recovery phases.
- Include phishing simulation and email log analysis.
- Deploy multi-tier attack chains to test kill chain detection in full.
- Add a Splunk dashboard for compliance auditing and control health status.

---

> 🔍 Each major folder includes its own `README.md` explaining setup, logic, and configuration decisions in depth. This main README provides a high-level summary for recruiters, collaborators, and project reviewers.


