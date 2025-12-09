# 🛡️ SecTool-Rules: Windows Threat Detection Library

![Category](https://img.shields.io/badge/Category-Blue%20Team-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Splunk%20%7C%20Sysmon-orange)
![Status](https://img.shields.io/badge/Status-Active-success)

## 📋 Project Overview
This repository contains a curated collection of **System Monitor (Sysmon) configurations** and **Splunk Search Processing Language (SPL)** queries designed to detect Advanced Persistent Threats (APT), Living-off-the-Land (LOLBAS) attacks, and persistence mechanisms in Windows environments.

These rules were engineered to move beyond default alerts, focusing on high-fidelity detection of specific adversarial behaviors mapped to the **MITRE ATT&CK** framework.

---

## 📂 Repository Structure

```text
SecTool-Rules/
├── SPL-detection-rules/       # Custom Splunk queries for standard Windows Logs
│   ├── auditlogclearing.spl   # Detects Event ID 1102 (Anti-Forensics)
│   ├── bruteforce.spl         # Detects high-volume failed logins (Event ID 4625)
│   ├── ghostaccount.spl       # Detects unauthorized user creation (Event ID 4720)
│   └── timealteration.spl     # Detects system time modification (Event ID 4616)
│
├── sysmon/                    # Modular XML configuration snippets for Sysmon
│   ├── rule1.xml              # Ransomware file extension detection
│   ├── rule2.xml              # Ncat/Reverse shell tool detection
│   ├── rule3.xml              # PowerShell hidden window detection
│   └── rule4.xml              # Reconnaissance detection (Whoami) with noise filtering
│
└── LICENSE