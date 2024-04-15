Rules by Product and UseCase
============================
Vendor: Unix
------------
### Product: [Auditbeat](../ds_unix_auditbeat.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   2    |         3          |       4        |    0    |

| Event Type          | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity        | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity<br> ↳ <b>APP-ObT-PRIV</b>: Non-privileged user accessing privileged application object |  • <b>APP-ObT-PRIV</b>: Privileged application objects<br> • <b>APP-AT-PRIV</b>: Privileged application activities |
| app-activity-failed | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| app-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |    |
| process-created     | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset<br><br><b>T1059.003 - T1059.003</b><br> ↳ <b>EPA-OH-CS</b>: First execution of critical windows command on a Domain Controller/Critical System    |    |