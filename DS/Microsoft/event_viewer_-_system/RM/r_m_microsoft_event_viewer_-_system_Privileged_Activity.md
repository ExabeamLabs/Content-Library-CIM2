Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - System](../ds_microsoft_event_viewer_-_system.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   3    |         7          |       4        |   86    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity    |  • <b>APP-AT-PRIV</b>: Privileged application activities    |
| process-created | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset    |    |
| security-alert  | <b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |    |
| service-created | <b>T1053 - Scheduled Task/Job</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1053.005 - Scheduled Task/Job: Scheduled Task</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543 - Create or Modify System Process</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset |  • <b>AL-HT-PRIV</b>: Privilege Users Assets<br> • <b>AL-HT-EXEC</b>: Executive Assets |