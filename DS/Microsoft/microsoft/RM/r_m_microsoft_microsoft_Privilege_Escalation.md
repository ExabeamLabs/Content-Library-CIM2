Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Microsoft](../ds_microsoft_microsoft.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   3    |         2          |       2        |    2    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity    | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| service-created | <b>T1543.003 - Create or Modify System Process: Windows Service</b><br> ↳ <b>WSC-GH-F</b>: First service installation on host in the peer group<br> ↳ <b>WSC-GS-A</b>: Unusual service name in the peer group    |  • <b>WSC-GS</b>: Services that are installed in the peer group<br> • <b>WSC-GH</b>: Hosts on which a new service is installed in the peer group |