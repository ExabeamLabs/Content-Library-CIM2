Rules by Product and UseCase
============================
Vendor: F5
----------
### Product: [F5 Advanced Web Application Firewall](../ds_f5_f5_advanced_web_application_firewall.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   4    |         2          |       2        |    6    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-switch        | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users    |
| authentication-failed | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a country from which there was no prior successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which group has never had a successful activity<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity |