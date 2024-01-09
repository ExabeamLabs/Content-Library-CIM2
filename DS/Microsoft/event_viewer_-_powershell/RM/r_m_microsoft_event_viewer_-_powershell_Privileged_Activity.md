Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - PowerShell](../ds_microsoft_event_viewer_-_powershell.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   0    |         2          |       2        |   23    |

| Event Type      | Rules    | Models |
| ---- | ---- | ------ |
| app-login       | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account    |        |
| process-created | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset |        |