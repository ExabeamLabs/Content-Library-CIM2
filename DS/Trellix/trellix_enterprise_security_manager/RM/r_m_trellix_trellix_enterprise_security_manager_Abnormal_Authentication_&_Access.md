Rules by Product and UseCase
============================
Vendor: Trellix
---------------
### Product: [Trellix Enterprise Security Manager](../ds_trellix_trellix_enterprise_security_manager.md)
### Use-Case: [Abnormal Authentication & Access](../../../../UseCases/uc_abnormal_authentication_&_access.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  21   |   10   |         4          |       3        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| authentication-failed | <b>T1133 - External Remote Services</b><br> ↳ <b>FA-UC-F</b>: Failed activity from a country from which there was no prior successful activity<br> ↳ <b>FA-GC-F</b>: First Failed activity in session from country in which group has never had a successful activity<br> ↳ <b>FA-OC-F</b>: First Failed activity in session from country in which organization has never had a successful activity    |  • <b>UA-OC</b>: Countries for organization<br> • <b>UA-GC</b>: Countries for peer groups<br> • <b>UA-UC</b>: Countries for user activity    |
| failed-logon          | <b>T1110 - Brute Force</b><br> ↳ <b>SEQ-UH-09</b>: Abnormal time of the week for a failed logon for user<br> ↳ <b>SEQ-UH-10</b>: Failed logons had multiple reasons<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-03</b>: Failed logon to a top failed logon asset by user<br> ↳ <b>SEQ-UH-06</b>: Abnormal failed logon to asset by user<br> ↳ <b>SEQ-UH-07</b>: Failed logon to an asset that user has not previously accessed    |  • <b>FL-UH</b>: All Failed Logons per user<br> • <b>FL-OH</b>: All Failed Logons in the organization    |
| ntlm-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>AL-HLocU-F</b>: First local user logon to this asset<br> ↳ <b>AL-HLocU-A</b>: Abnormal local user logon to this asset<br> ↳ <b>DORMANT-USER</b>: Dormant User<br> ↳ <b>AE-UA-F</b>: First activity type for user<br> ↳ <b>AL-UT-F</b>: Logon to New Asset Type<br> ↳ <b>AL-UT-A</b>: Logon to Abnormal asset type<br> ↳ <b>AL-UZ-F</b>: First logon to network zone<br> ↳ <b>AL-UZ-A</b>: Abnormal logon to network zone<br> ↳ <b>AL-F-MultiWs</b>: Multiple workstations in a single session<br> ↳ <b>NEW-USER-F</b>: User with no event history<br> ↳ <b>AL-GZ-F-new</b>: First logon to network zone for new user of group<br> ↳ <b>AL-GZ-A-new</b>: Abnormal logon to network zone for group of new user<br> ↳ <b>PA-IT-NoPA</b>: IT presence without badge access<br><br><b>T1078.003 - Valid Accounts: Local Accounts</b><br> ↳ <b>AL-HLocU-F</b>: First local user logon to this asset<br> ↳ <b>AL-HLocU-A</b>: Abnormal local user logon to this asset |  • <b>PA-OU</b>: Badge access by users in the organization<br> • <b>AL-GZ</b>: Network zones accessed by this peer group<br> • <b>AL-UT</b>: Types of hosts<br> • <b>AE-UA</b>: All activity for users<br> • <b>NKL-HU</b>: Users logging into this host remotely |