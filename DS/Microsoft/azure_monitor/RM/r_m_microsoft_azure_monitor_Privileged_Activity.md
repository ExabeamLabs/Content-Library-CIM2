Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor](../ds_microsoft_azure_monitor.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   1    |         5          |       12       |   94    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity         | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity    |  • <b>APP-AT-PRIV</b>: Privileged application activities |
| app-activity-failed  | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| failed-app-login     | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| file-delete          | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-download        | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-read    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-upload          | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-write    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| security-alert       | <b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |    |
| web-activity-allowed | <b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity |    |
| web-activity-denied  | <b>T1071 - Application Layer Protocol</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity |    |