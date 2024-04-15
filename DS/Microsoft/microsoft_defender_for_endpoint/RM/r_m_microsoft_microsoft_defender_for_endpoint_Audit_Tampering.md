Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft Defender for Endpoint](../ds_microsoft_microsoft_defender_for_endpoint.md)
### Use-Case: [Audit Tampering](../../../../UseCases/uc_audit_tampering.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   2    |         7          |       2        |    8    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| audit-log-clear | <b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>WA-HA-F-1</b>: First audit log clearance on host<br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user<br> ↳ <b>A-WA-F</b>: Audit log has been cleared on this asset<br><br><b>T1562.002 - T1562.002</b><br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user    |  • <b>AE-UA</b>: All activity for users<br> • <b>WA-HA</b>: Hosts with audit policy/audit log changes |
| process-created | <b>T1546.003 - T1546.003</b><br> ↳ <b>A-WMI-Script-Event-Consumers</b>: Suspicious usage of WMI script event consumers on this asset.<br><br><b>T1562 - Impair Defenses</b><br> ↳ <b>A-Sysmon-Driver-Unload</b>: Possible Sysmon driver unloaded on this asset.<br><br><b>T1059 - Command and Scripting Interperter</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1070 - Indicator Removal on Host</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1562.006 - T1562.006</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-EventLog-Tamper</b>: EventLog has been tampered with on this asset |    |