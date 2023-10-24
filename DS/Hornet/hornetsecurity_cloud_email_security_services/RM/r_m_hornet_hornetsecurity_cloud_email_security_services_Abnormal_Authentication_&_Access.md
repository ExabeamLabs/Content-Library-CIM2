Rules by Product and UseCase
============================
Vendor: Hornet
--------------
### Product: [Hornetsecurity Cloud Email Security Services](../ds_hornet_hornetsecurity_cloud_email_security_services.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         1          |       3        |    3    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-disabled        | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user |  • <b>AE-UA</b>: All activity for users |
| account-password-change | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user |  • <b>AE-UA</b>: All activity for users |
| account-unlocked        | <b>T1078 - Valid Accounts</b><br> ↳ <b>AE-UA-F</b>: First activity type for user    |  • <b>AE-UA</b>: All activity for users |