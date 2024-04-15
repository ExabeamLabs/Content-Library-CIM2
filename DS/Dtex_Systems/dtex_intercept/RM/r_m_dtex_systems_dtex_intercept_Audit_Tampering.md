Rules by Product and UseCase
============================
Vendor: Dtex Systems
--------------------
### Product: [DTEX InTERCEPT](../ds_dtex_systems_dtex_intercept.md)
### Use-Case: [Audit Tampering](../../../../UseCases/uc_audit_tampering.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   0    |         6          |       1        |    1    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| process-created | <b>T1546.003 - T1546.003</b><br> ↳ <b>A-WMI-Script-Event-Consumers</b>: Suspicious usage of WMI script event consumers on this asset.<br><br><b>T1562 - Impair Defenses</b><br> ↳ <b>A-Sysmon-Driver-Unload</b>: Possible Sysmon driver unloaded on this asset.<br><br><b>T1059 - Command and Scripting Interperter</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1070 - Indicator Removal on Host</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1562.006 - T1562.006</b><br> ↳ <b>A-ETW-Trace-Disable</b>: Event tracing has been disabled, possible logging evasion on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-EventLog-Tamper</b>: EventLog has been tampered with on this asset |        |