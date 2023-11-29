Rules by Product and UseCase
============================
Vendor: HP
----------
### Product: [HP Virtual Connect Enterprise Manager](../ds_hp_hp_virtual_connect_enterprise_manager.md)
### Use-Case: [Compromised Credentials](../../../../UseCases/uc_compromised_credentials.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   1   |   1    |         2          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| app-login  | <b>T1078 - Valid Accounts</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UI-F</b>: First activity from ISP |  • <b>UA-UI-new</b>: ISP of users during application activity |