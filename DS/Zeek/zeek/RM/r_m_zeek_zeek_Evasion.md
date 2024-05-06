Rules by Product and UseCase
============================
Vendor: Zeek
------------
### Product: [Zeek](../ds_zeek_zeek.md)
### Use-Case: [Evasion](../../../../UseCases/uc_evasion.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   0    |         3          |       2        |   12    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| audit-log-clear | <b>T1070.001 - Indicator Removal on Host: Clear Windows Event Logs</b><br> ↳ <b>A-WA-F</b>: Audit log has been cleared on this asset    |        |
| registry-write  | <b>T1564.002 - T1564.002</b><br> ↳ <b>A-HiddenUser-UserList</b>: A user was hidden from the login screen on this asset.<br><br><b>T1564.001 - T1564.001</b><br> ↳ <b>A-HiddenFile-RegistryDisable</b>: 'Show hidden' setting disabled through the registry on this asset. |        |