Rules by Product and UseCase
============================
Vendor: Dell
------------
### Product: [EMC Isilon](../ds_dell_emc_isilon.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   4    |         4          |       4        |    2    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| file-delete   | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |
| file-read     | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |
| file-write    | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |
| remote-access | <b>T1021 - Remote Services</b><br> ↳ <b>RA-UH-CS-NC</b>: Remote access  to a critical system for user with no information<br> ↳ <b>RA-F-F-CS</b>: First remote access to critical system for user<br> ↳ <b>RA-F-A-CS</b>: Abnormal remote access to critical system for user<br> ↳ <b>RA-HT-EXEC-new</b>: New user remote access to executive asset<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>RA-UH-CS-NC</b>: Remote access  to a critical system for user with no information<br> ↳ <b>RA-F-F-CS</b>: First remote access to critical system for user<br> ↳ <b>RA-F-A-CS</b>: Abnormal remote access to critical system for user<br> ↳ <b>RA-HT-EXEC-new</b>: New user remote access to executive asset<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive |  • <b>AL-HT-EXEC</b>: Executive Assets<br> • <b>RA-UH</b>: Assets accessed by this user remotely |