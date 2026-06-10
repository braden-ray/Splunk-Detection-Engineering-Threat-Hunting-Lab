# Encoded PowerShell Hunting

## Objective
Hunt for encoded or suspicious PowerShell command activity within Windows event logs.

## SPL Query

```spl
source="WinEventLog:*" encodedcommand
