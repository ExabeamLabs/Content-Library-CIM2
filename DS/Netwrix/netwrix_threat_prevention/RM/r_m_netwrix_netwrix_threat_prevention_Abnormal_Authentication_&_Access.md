Rules by Product and UseCase
============================
Vendor: Netwrix
---------------
### Product: [Netwrix Threat Prevention](../ds_netwrix_netwrix_threat_prevention.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  11   |   4    |         1          |       1        |    1    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| kerberos-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user<br> ↳ <b>AL-UT-F</b>: Logon to New Asset Type<br> ↳ <b>AL-UT-A</b>: Logon to Abnormal asset type<br> ↳ <b>AL-UZ-F</b>: First logon to network zone<br> ↳ <b>AL-UZ-A</b>: Abnormal logon to network zone<br> ↳ <b>AL-F-MultiWs</b>: Multiple workstations in a single session<br> ↳ <b>NEW-USER-F</b>: User with no event history<br> ↳ <b>AL-GZ-F-new</b>: First logon to network zone for new user of group<br> ↳ <b>AL-GZ-A-new</b>: Abnormal logon to network zone for group of new user<br> ↳ <b>PA-IT-NoPA</b>: IT presence without badge access |  • <b>PA-OU</b>: Badge access by users in the organization<br> • <b>AL-GZ</b>: Network zones accessed by this peer group<br> • <b>AL-UT</b>: Types of hosts<br> • <b>AE-UA</b>: All activity for users |