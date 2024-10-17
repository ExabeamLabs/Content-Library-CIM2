Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Event Viewer - System](../ds_microsoft_event_viewer_-_system.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  10   |   3    |         9          |       3        |    2    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity    | <b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions    |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| service-created | <b>T1053 - Scheduled Task/Job</b><br> ↳ <b>WSC-GS-A</b>: Unusual service name in the peer group<br><br><b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WSC-GH-F</b>: First service installation on host in the peer group<br> ↳ <b>WSC-GS-A</b>: Unusual service name in the peer group<br><br><b>T1543 - Create or Modify System Process</b><br> ↳ <b>WSC-GH-F</b>: First service installation on host in the peer group    |  • <b>WSC-GS</b>: Services that are installed in the peer group<br> • <b>WSC-GH</b>: Hosts on which a new service is installed in the peer group |
| share-access    | <b>T1484 - Group Policy Modification</b><br> ↳ <b>SA-Bloodhound-Main-1</b>: Possible Bloodhound Tool Usage by this user accessing srcsvc folder.<br> ↳ <b>SA-Bloodhound-Main-2</b>: Possible Bloodhound Tool Usage by this user accessing lsarpc folder.<br> ↳ <b>SA-Bloodhound-Main-3</b>: Possible Bloodhound Tool Usage by this user accessing samr folder.<br><br><b>T1021 - Remote Services</b><br> ↳ <b>SA-Bloodhound-3</b>: ADMIN IPC Share srcsvc accessed<br> ↳ <b>SA-Bloodhound-2</b>: ADMIN IPC Share samr folder accessed<br><br><b>T1021.002 - Remote Services: SMB/Windows Admin Shares</b><br> ↳ <b>SA-Bloodhound-3</b>: ADMIN IPC Share srcsvc accessed<br> ↳ <b>SA-Bloodhound-2</b>: ADMIN IPC Share samr folder accessed<br><br><b>T1087 - Account Discovery</b><br> ↳ <b>SA-Bloodhound-3</b>: ADMIN IPC Share srcsvc accessed<br> ↳ <b>SA-Bloodhound-2</b>: ADMIN IPC Share samr folder accessed |    |