# PowerShell Hunting Analysis

## Objective
Detect suspicious PowerShell execution activity within Windows event logs.

## SPL Query

```spl
source="WinEventLog:*" powershell.exe
```

## Investigation Notes
- PowerShell is commonly abused by attackers for execution and persistence
- Query searches for PowerShell-related process activity across Windows logs
- Useful for identifying suspicious scripts, encoded commands, or attacker tooling

## Detection Logic
- Monitor PowerShell execution frequency
- Investigate unusual parent/child process relationships
- Review suspicious command-line activity

## Related MITRE ATT&CK Techniques
- T1059.001 — PowerShell
