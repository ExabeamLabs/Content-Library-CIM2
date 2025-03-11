Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Sysmon](../ds_microsoft_sysmon.md)
### Use-Case: [Privileged Activity](../../../../UseCases/uc_privileged_activity.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  11   |   3    |         6          |       5        |   45    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity    | <b>T1078 - Valid Accounts</b><br> ↳ <b>APP-Account-deactivated</b>: Activity from a de-activated user account<br> ↳ <b>APP-AT-PRIV</b>: Non-privileged user performing privileged application activity    |  • <b>APP-AT-PRIV</b>: Privileged application activities    |
| ds-access       | <b>T1207 - Rogue Domain Controller</b><br> ↳ <b>DS-DCShadow-E</b>: Possible DCShadow attack from Existing Machine<br> ↳ <b>DS-DCShadow-F</b>: First event for machine in possible DCShadow attack<br> ↳ <b>A-DS-DCShadow</b>: Possible DCShadow attack by asset detected.<br><br><b>T1003 - OS Credential Dumping</b><br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host.<br> ↳ <b>A-DCSync</b>: Possible DCSync attack detected<br><br><b>T1003.006 - OS Credential Dumping: DCSync</b><br> ↳ <b>DCSync-ExistHost</b>: Possible DCSync attack - existing host has replicated Active Directory.<br> ↳ <b>DCSync-FirstDS</b>: Possible DCSync attack - first DS access event from host.<br> ↳ <b>A-DCSync</b>: Possible DCSync attack detected<br><br><b>T1484 - Group Policy Modification</b><br> ↳ <b>DS-UA</b>: First access to attribute for privileged user |  • <b>DS-HOSTS</b>: Models hosts in an Active Directory environment<br> • <b>DS-UA</b>: Attributes per privileged user |
| file-delete     | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| file-write      | <b>T1078 - Valid Accounts</b><br> ↳ <b>FA-Account-deactivated</b>: File Activity from a de-activated user account    |    |
| process-created | <b>T1482 - Domain Trust Discovery</b><br> ↳ <b>A-Trickbot-Recon</b>: Trickbot malware domain recon activity on this asset    |    |