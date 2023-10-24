Rules by Product and UseCase
============================
Vendor: AVI Networks
--------------------
### Product: [AVI Networks Software Load Balancer](../ds_avi_networks_avi_networks_software_load_balancer.md)
### Use-Case: [Audit Tampering](../../../../UseCases/uc_audit_tampering.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   2    |         2          |       1        |    1    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| audit-log-clear | <b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>WA-HA-F-1</b>: First audit log clearance on host<br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user<br> ↳ <b>A-WA-F</b>: Audit log has been cleared on this asset<br><br><b>T1562.002 - T1562.002</b><br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user |  • <b>AE-UA</b>: All activity for users<br> • <b>WA-HA</b>: Hosts with audit policy/audit log changes |