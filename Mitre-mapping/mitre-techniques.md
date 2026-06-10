# MITRE ATT&CK Technique Mapping

## Overview

This document maps observed activity and SPL hunting techniques from the lab environment to relevant MITRE ATT&CK tactics and techniques.

The objective of this mapping is to improve threat visibility, detection engineering alignment, and investigation context.

---

# Mapped Techniques

## T1110 — Brute Force

### Description
Attackers attempt to gain unauthorized access through repeated authentication attempts using multiple password combinations.

### Detection Method
- Failed login event monitoring
- Authentication anomaly investigation
- Windows Security Event Log analysis

### Related SPL Query

```spl
source="WinEventLog:Security" failed password
```

---

## T1059.001 — PowerShell

### Description
Attackers abuse PowerShell for execution, persistence, and malicious automation.

### Detection Method
- PowerShell process hunting
- Encoded command detection
- Windows process telemetry analysis

### Related SPL Query

```spl
source="WinEventLog:*" powershell.exe
```

---

## T1059.003 — Windows Command Shell

### Description
Attackers utilize CMD execution to perform administrative actions, execute malware, or launch secondary payloads.

### Detection Method
- CMD process execution monitoring
- Suspicious command-line activity investigation

### Related SPL Query

```spl
source="WinEventLog:*" cmd.exe
```

---

## T1087 — Account Discovery

### Description
Attackers attempt to enumerate user accounts and authentication information within a target environment.

### Detection Method
- Authentication event analysis
- User account activity review
- Correlation of suspicious login behavior

---

# Investigation Benefits

- Improved threat classification
- Better detection engineering alignment
- Structured incident analysis methodology
- Enhanced SOC investigation workflow visibility

---

# Skills Demonstrated

- MITRE ATT&CK Mapping
- Threat Hunting
- Detection Engineering
- SPL Query Development
- Windows Log Analysis
- Security Event Correlation
