Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft DHCP Log](../ds_microsoft_microsoft_dhcp_log.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         1          |       2        |    2    |

| Event Type       | Rules    | Models |
| ---- | ---- | ------ |
| failed-app-login | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account     |        |
| file-write       | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |        |