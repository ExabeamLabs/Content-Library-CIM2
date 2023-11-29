Rules by Product and UseCase
============================
Vendor: Swift
-------------
### Product: [SAP](../ds_swift_sap.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   9   |   4    |         3          |       5        |    5    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| account-creation | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User    |    |
| account-deleted  | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users    |
| account-lockout  | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-01</b>: Account lockout on an asset that belongs to this user    |    |
| account-unlocked | <b>T1078 - Valid Accounts</b><br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users    |
| app-activity     | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user<br> ↳ <b>UA-GC-F</b>: First activity from country for group<br> ↳ <b>UA-GC-A</b>: Abnormal activity from country for group<br> ↳ <b>UA-OC-F</b>: First activity from country for organization<br> ↳ <b>UA-OC-A</b>: Abnormal activity from country for organization<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>UA-UC-F</b>: First activity from country for user<br> ↳ <b>UA-UC-A</b>: Abnormal activity from country for user<br> ↳ <b>UA-GC-F</b>: First activity from country for group<br> ↳ <b>UA-GC-A</b>: Abnormal activity from country for group<br> ↳ <b>UA-OC-F</b>: First activity from country for organization<br> ↳ <b>UA-OC-A</b>: Abnormal activity from country for organization |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity<br> • <b>AE-UA</b>: All activity for users |