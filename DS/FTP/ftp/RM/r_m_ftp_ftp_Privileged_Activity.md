Rules by Product and UseCase
============================
Vendor: FTP
-----------
### Product: [FTP](../ds_ftp_ftp.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   4    |         2          |       7        |   12    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity        | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity<br> ↳ <b>APP-ObT-PRIV</b>: Non-privileged user accessing privileged application object    |  • <b>APP-ObT-PRIV</b>: Privileged application objects<br> • <b>APP-AT-PRIV</b>: Privileged application activities |
| app-activity-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| failed-app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| file-delete         | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |
| file-read    | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |
| file-write          | <b>T1083 - File and Directory Discovery</b><br> ↳ <b>FA-FT-EXEC</b>: Non-Executive user accessed executive folder<br> ↳ <b>FA-FT-PRIV</b>: Non-Privileged user accessed privileged folder<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |  • <b>FA-FT-PRIV</b>: Privileged Folders<br> • <b>FA-FT-EXEC</b>: Executive Folders    |