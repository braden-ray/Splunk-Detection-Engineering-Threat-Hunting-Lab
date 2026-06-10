# Suspicious Process Analysis

## Objective
Investigate potentially suspicious Windows process activity using Splunk SPL queries.

## SPL Query

```spl
source="WinEventLog:*" (powershell.exe OR cmd.exe)
```

## Investigation Notes
- Investigated PowerShell and CMD process activity within Windows logs
- Reviewed process execution events and command-line artifacts
- Correlated suspicious process behavior with authentication activity
- Combined process telemetry with threat hunting methodology

## Detection Logic
- Monitor administrative scripting activity
- Identify suspicious shell execution behavior
- Correlate process execution with other security events

## Related MITRE ATT&CK Techniques
- T1059 — Command and Scripting Interpreter
- T1059.001 — PowerShell
- T1059.003 — Windows Command Shell
