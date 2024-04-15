Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [MSSQL](../ds_microsoft_mssql.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         2          |       3        |    4    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| failed-app-login         | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| privileged-object-access | <b>T1059.003 - T1059.003</b><br> ↳ <b>WPA-OH-F</b>: First execution of critical windows command using privileged access on this host in the organization |  • <b>WPA-OH</b>: Assets on which critical windows commands are executed in the organization |