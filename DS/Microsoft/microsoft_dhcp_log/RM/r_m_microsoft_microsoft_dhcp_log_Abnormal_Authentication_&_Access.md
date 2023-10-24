Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft DHCP Log](../ds_microsoft_microsoft_dhcp_log.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   4   |   4    |         2          |       2        |    2    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| audit-log-clear  | <b>T1078 - Valid Accounts</b><br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users    |
| failed-app-login | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a country from which there was no prior successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which group has never had a successful activity<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity |