Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - AzureADPasswordProtection-DCAgent](../ds_microsoft_event_viewer_-_azureadpasswordprotection-dcagent.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         2          |       3        |    9    |

| Event Type    | Rules    | Models |
| ---- | ---- | ------ |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user     |        |
| account-password-reset  | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user     |        |
| file-write    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account |        |