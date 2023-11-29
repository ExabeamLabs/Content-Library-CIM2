Rules by Product and UseCase
============================
Vendor: Apple
-------------
### Product: [macOS](../ds_apple_macos.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  16   |   7    |         2          |       1        |    1    |

| Event Type  | Rules    | Models    |
| ---- | ---- | ---- |
| local-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user<br> ↳ <b>AL-UT-F</b>: Logon to New Asset Type<br> ↳ <b>AL-UT-A</b>: Logon to Abnormal asset type<br> ↳ <b>AL-F-F-CS</b>: First logon to a critical system for user<br> ↳ <b>AL-F-A-CS</b>: Abnormal logon to a critical system for user<br> ↳ <b>AL-UH-CS-NC</b>: Logon to a critical system for a user with no information<br> ↳ <b>AL-OU-F-CS</b>: First logon to a critical system that user has not previously accessed<br> ↳ <b>AL-UZ-F</b>: First logon to network zone<br> ↳ <b>AL-UZ-A</b>: Abnormal logon to network zone<br> ↳ <b>AL-GZ-F</b>: First logon to network zone for group<br> ↳ <b>AL-GZ-A</b>: Abnormal logon to network zone for group<br><br><b>T1078.003 - Valid Accounts: Local Accounts</b><br> ↳ <b>AL-HLocU-F</b>: First local user logon to this asset<br> ↳ <b>AL-HLocU-A</b>: Abnormal local user logon to this asset<br> ↳ <b>LL-UH-F</b>: First local logon to asset<br> ↳ <b>LL-UH-A</b>: Abnormal local logon to asset |  • <b>AL-GZ</b>: Network zones accessed by this peer group<br> • <b>LL-UH</b>: Local logons<br> • <b>AL-OU-CS</b>: Logon to critical servers<br> • <b>RA-UH</b>: Assets accessed by this user remotely<br> • <b>AL-UT</b>: Types of hosts<br> • <b>AE-UA</b>: All activity for users<br> • <b>NKL-HU</b>: Users logging into this host remotely |