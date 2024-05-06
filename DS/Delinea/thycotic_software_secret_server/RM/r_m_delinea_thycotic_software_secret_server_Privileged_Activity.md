Rules by Product and UseCase
============================
Vendor: Delinea
---------------
### Product: [Thycotic Software Secret Server](../ds_delinea_thycotic_software_secret_server.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         1          |       4        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| account-switch   | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account    |    |
| app-activity     | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity |  • <b>APP-AT-PRIV</b>: Privileged application activities |
| app-login        | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |