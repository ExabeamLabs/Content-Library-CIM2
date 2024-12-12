Rules by Product and UseCase
============================
Vendor: Netwrix
---------------
### Product: [Netwrix Threat Prevention](../ds_netwrix_netwrix_threat_prevention.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   3    |         2          |       1        |    0    |

| Event Type     | Rules    | Models    |
| ---- | ---- | ---- |
| kerberos-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>AL-F-F-DC-G</b>: First logon to a Domain Controller for peer group<br> ↳ <b>AL-F-A-DC-G</b>: Abnormal logon to a Domain Controller for Peer Group<br> ↳ <b>AL-UH-F-DC</b>: First logon to this Domain Controller for user<br> ↳ <b>AL-UH-A-DC</b>: Abnormal logon to a Domain Controller that user has not accessed often previously<br> ↳ <b>AL-UH-DC-NC</b>: Logon to a Domain Controller for user with no information<br> ↳ <b>AL-HT-EXEC-new</b>: New user logon to executive asset<br><br><b>T1078.002 - T1078.002</b><br> ↳ <b>AL-F-F-DC-G</b>: First logon to a Domain Controller for peer group<br> ↳ <b>AL-F-A-DC-G</b>: Abnormal logon to a Domain Controller for Peer Group<br> ↳ <b>AL-UH-F-DC</b>: First logon to this Domain Controller for user<br> ↳ <b>AL-UH-A-DC</b>: Abnormal logon to a Domain Controller that user has not accessed often previously<br> ↳ <b>AL-UH-DC-NC</b>: Logon to a Domain Controller for user with no information |  • <b>AL-HT-EXEC</b>: Executive Assets<br> • <b>RA-UH</b>: Assets accessed by this user remotely<br> • <b>AL-UH-DC</b>: Logons to Domain Controllers |