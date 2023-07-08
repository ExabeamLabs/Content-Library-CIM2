Rules by Product and UseCase
============================
Vendor: Wiz
-----------
### Product: [Wiz](../ds_wiz_wiz.md)
### Use-Case: [Audit Tampering](../../../../UseCases/uc_audit_tampering.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         2          |       1        |    1    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| audit-policy-change | <b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user<br><br><b>T1562.002 - T1562.002</b><br> ↳ <b>WA-HA-F-2</b>: First audit policy change on host<br> ↳ <b>AE-UA-FA</b>: First audit activity type for user<br> ↳ <b>WA-CS</b>: Audit activity on a critical system for user |  • <b>AE-UA</b>: All activity for users<br> • <b>WA-HA</b>: Hosts with audit policy/audit log changes |