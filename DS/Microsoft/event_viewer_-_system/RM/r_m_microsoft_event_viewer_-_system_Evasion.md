Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - System](../ds_microsoft_event_viewer_-_system.md)
### Use-Case: [Evasion](../../../../UseCases/uc_evasion.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         4          |       2        |    4    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| audit-log-clear | <b>T1070 - Indicator Removal on Host</b><br> ↳ <b>A-WA-F</b>: Audit log has been cleared on this asset<br><br><b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-WA-F</b>: Audit log has been cleared on this asset    |        |
| service-created | <b>T1543 - Create or Modify System Process</b><br> ↳ <b>A-WSC-RANDOM-SERVICE</b>: Random service name for the asset<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>A-WSC-RANDOM-SERVICE</b>: Random service name for the asset |        |