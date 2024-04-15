Rules by Product and UseCase
============================
Vendor: Trend Micro
-------------------
### Product: [OfficeScan](../ds_trend_micro_officescan.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   1    |         5          |       5        |   16    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| dlp-email-alert-in       | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| dlp-email-alert-out      | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| privileged-object-access | <b>T1059.003 - T1059.003</b><br> ↳ <b>WPA-OH-F</b>: First execution of critical windows command using privileged access on this host in the organization    |  • <b>WPA-OH</b>: Assets on which critical windows commands are executed in the organization |
| security-alert    | <b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |    |
| web-activity-allowed     | <b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity<br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1102 - Web Service</b><br> ↳ <b>A-WEB-DC</b>: Web activity event on a Domain Controller<br><br><b>T1078 - Valid Accounts</b><br> ↳ <b>WEB-ALERT-EXEC</b>: Security violation by Executive in web activity |    |