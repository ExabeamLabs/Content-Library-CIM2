Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco IOS](../ds_cisco_cisco_ios.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   1    |         3          |       3        |    3    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity         |  • <b>APP-AT-PRIV</b>: Privileged application activities |
| failed-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive |    |
| process-created | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset<br> ↳ <b>Trickbot-Recon</b>: Trickbot malware domain recon activity    |    |