# Failed Logon Detection Query

## Objective
Detect failed Windows authentication attempts using Splunk Security Event logs.

## SPL Query

```spl
source="WinEventLog:Security" EventCode=4625
| table _time Account_Name Failure_Reason host
```

## Investigation Notes
- EventCode 4625 represents failed logon attempts
- Query extracts timestamps, usernames, failure reasons, and host information
- Useful for identifying brute force attempts and suspicious authentication behavior

## Related MITRE ATT&CK Techniques
- T1110 — Brute Force
