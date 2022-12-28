Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - Security](../ds_microsoft_event_viewer_-_security.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  27   |   12   |     9      |       87       |   87    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-switch         | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-UA-F-PRIV</b>: Account switch to a privileged or executive account    |    |
| app-activity    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity    |  • <b>APP-AT-PRIV</b>: Privileged application activities    |
| ds-access    | <b>T1207 - Rogue Domain Controller</b><br> ↳ <b>A-DS-DCShadow</b>: Possible DCShadow attack by asset detected.<br> ↳ <b>DS-DCShadow-E</b>: Possible DCShadow attack from Existing Machine<br> ↳ <b>DS-DCShadow-F</b>: First event for machine in possible DCShadow attack<br><br><b>T1484 - Group Policy Modification</b><br> ↳ <b>DS-UA</b>: First access to attribute for privileged user<br><br><b>T1003.006 - OS Credential Dumping: DCSync</b><br> ↳ <b>A-DCSync</b>: Possible DCSync Attack: New domain controller detected<br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host. |  • <b>DS-HOSTS</b>: Models hosts in an Active Directory environment<br> • <b>DS-UA</b>: Attributes per privileged user    |
| failed-logon    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account<br><br><b>T1068 - Exploitation for Privilege Escalation</b><br> ↳ <b>ALERT-EXEC</b>: Security violation by Executive    |    |
| file-delete    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-permission-change | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-read    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-write    | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| privileged-access      | <b>TA0002 - TA0002</b><br> ↳ <b>WPA-UP-F</b>: First privileged process for user<br> ↳ <b>WPA-UP-A</b>: Abnormal privileged process for user<br> ↳ <b>WPA-GP-F</b>: First privileged process for peer group<br> ↳ <b>WPA-GP-A</b>: Abnormal privileged process for peer group<br> ↳ <b>WPA-PD-F</b>: First directory for privileged process<br> ↳ <b>WPA-PD-A</b>: Abnormal directory for privileged process<br> ↳ <b>WPA-HP-F</b>: First privileged process for host<br> ↳ <b>WPA-HP-A</b>: Abnormal privileged process for host<br> ↳ <b>WPA-OP-F</b>: First privileged process for organization<br> ↳ <b>WPA-OP-A</b>: Abnormal privileged process for organization    |  • <b>WPA-OP</b>: Processes for organization<br> • <b>WPA-HP</b>: Processes for host<br> • <b>WPA-PD</b>: Directories per process<br> • <b>WPA-GP</b>: Privileged processes for peer group<br> • <b>WPA-GP-All</b>: Processes for peer group<br> • <b>WPA-UP</b>: Privileged processes for user<br> • <b>WPA-UP-All</b>: Processes for user |
| process-created        | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset<br> ↳ <b>Trickbot-Recon</b>: Trickbot malware domain recon activity    |    |
| service-created        | <b>T1053.005 - Scheduled Task/Job: Scheduled Task</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WTC-HT-EXEC</b>: Non-Executive user created a scheduled task/service on executive asset<br> ↳ <b>WTC-HT-PRIV</b>: Non-Privileged user created a scheduled task/service on privileged asset    |  • <b>AL-HT-PRIV</b>: Privilege Users Assets<br> • <b>AL-HT-EXEC</b>: Executive Assets    |