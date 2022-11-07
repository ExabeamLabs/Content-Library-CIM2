Vendor: CDS
===========
### Product: [CDS](../ds_cds_cds.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   3   |   1    |     1      |       4        |    4    |

| Event Type       | Rules    | Models    |
| ---- | ---- | ---- |
| account-creation | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>NEW-USER-F</b>: User with no event history |    |
| account-switch   | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user  |  • <b>AE-UA</b>: All activity for users |