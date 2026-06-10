# Threat Hunting Investigation Report

## Investigation Summary

This project focused on detecting and analyzing suspicious authentication and process activity within Windows event logs using Splunk Enterprise.

The investigation simulated a blue team threat hunting workflow involving failed login analysis, PowerShell activity monitoring, suspicious process investigation, and MITRE ATT&CK correlation.

Custom SPL queries were developed to identify potentially malicious behavior and improve visibility across Windows telemetry sources.

---

# Investigation Objectives

- Detect failed authentication activity
- Investigate suspicious PowerShell execution
- Analyze CMD and process activity
- Develop custom SPL hunting queries
- Correlate events across multiple Windows log sources
- Map findings to MITRE ATT&CK techniques

---

# Tools Used

- Splunk Enterprise
- Windows Event Logs
- SPL (Search Processing Language)
- Windows 11 Virtual Machine
- Oracle VirtualBox

---

# Investigation Workflow

## 1. Log Ingestion Validation

Validated successful ingestion of Windows Security Event Logs into Splunk.

## 2. Failed Login Investigation

Reviewed failed authentication events to identify suspicious login behavior and potential brute force activity.

## 3. PowerShell Activity Analysis

Investigated PowerShell execution artifacts within Windows event logs to identify suspicious scripting behavior.

## 4. Suspicious Process Analysis

Correlated CMD and PowerShell activity across log sources to identify potentially malicious process execution patterns.

## 5. MITRE ATT&CK Correlation

Mapped identified activity to relevant MITRE ATT&CK techniques to improve detection engineering visibility.

---

# Key Findings

- Failed login activity was successfully identified within Windows Security logs
- PowerShell execution artifacts were detected and analyzed
- Custom SPL queries successfully correlated suspicious process activity
- Event correlation improved visibility across authentication and process telemetry
- MITRE ATT&CK mapping provided structured threat classification

---

# Related MITRE ATT&CK Techniques

- T1110 — Brute Force
- T1059.001 — PowerShell
- T1059.003 — Windows Command Shell
- T1087 — Account Discovery

---

# Skills Demonstrated

- Threat Hunting
- SIEM Investigation
- SPL Query Development
- Detection Engineering
- IOC Correlation
- Windows Log Analysis
- Security Event Investigation
- MITRE ATT&CK Mapping
- Incident Documentation

---

# Conclusion

This project demonstrated practical SOC analyst and detection engineering workflows using Splunk Enterprise within a Windows lab environment. The investigation strengthened hands-on experience in log analysis, event correlation, PowerShell hunting, and threat detection methodology.
