# Brute Force Analysis

## Objective
Identify potential brute force authentication activity using failed Windows logon events.

## SPL Query

```spl
source="WinEventLog:Security" EventCode=4625
| stats count by Account_Name src_ip host
| sort - count
```

## Investigation Notes
- Multiple failed authentication attempts may indicate brute force activity
- Query aggregates failed logons by username, source IP, and host
- Sorting by count helps prioritize suspicious activity for investigation

## Detection Logic
- High volume failed logins
- Repeated authentication attempts against user accounts
- Potential password spraying or brute force behavior

## Related MITRE ATT&CK Techniques
- T1110 — Brute Force
