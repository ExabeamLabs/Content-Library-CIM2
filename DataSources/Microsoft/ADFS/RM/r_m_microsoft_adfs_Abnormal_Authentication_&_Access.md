Vendor: Microsoft
=================
### Product: [ADFS](../ds_microsoft_adfs.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   4   |   3    |     2      |       3        |    3    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-lockout       | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-01</b>: Account lockout on an asset that belongs to this user    |    |
| authentication-failed | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a new country<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which peer group has never had a successful activity |  • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-OC</b>: Countries for organization<br> • <b>UA-UC</b>: Countries for user activity |