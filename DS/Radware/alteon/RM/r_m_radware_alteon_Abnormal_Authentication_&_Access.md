Rules by Product and UseCase
============================
Vendor: Radware
---------------
### Product: [Alteon](../ds_radware_alteon.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   3    |         1          |       1        |    1    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| failed-app-login | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a country from which there was no prior successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which group has never had a successful activity<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity |