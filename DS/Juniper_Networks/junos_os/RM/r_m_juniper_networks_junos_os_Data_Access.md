Rules by Product and UseCase
============================
Vendor: Juniper Networks
------------------------
### Product: [Junos OS](../ds_juniper_networks_junos_os.md)
### Use-Case: [Data Access](../../../../UseCases/uc_data_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         2          |       2        |    3    |

| Event Type       | Rules    | Models |
| ---- | ---- | ------ |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-F-FL</b>: Failed login to application    |        |
| process-created  | <b>T1003 - OS Credential Dumping</b><br> ↳ <b>A-CP-Sensitive-Files</b>: Copying sensitive files with credential data on this asset |        |