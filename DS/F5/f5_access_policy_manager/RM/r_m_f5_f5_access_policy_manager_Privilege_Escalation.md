Rules by Product and UseCase
============================
Vendor: F5
----------
### Product: [F5 Access Policy Manager](../ds_f5_f5_access_policy_manager.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   9   |   5    |         5          |       3        |   16    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| app-activity | <b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions    |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| failed-logon | <b>T1210 - Exploitation of Remote Services</b><br> ↳ <b>A-Suspicious-Zerologon</b>: Failed authentication attempt on this asset.    |    |
| vpn-logout   | <b>T1555 - Credentials from Password Stores</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user. |  • <b>AS-PV-USize</b>: Count of password retrievals in a session for the user<br> • <b>AS-PV-GSize</b>: Count of password retrievals in a session for the peer group<br> • <b>AS-PV-OSize</b>: Count of password retrievals in a session for the organization<br> • <b>AS-PV-USCOUNT</b>: Count of safe values accessed in a session<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user. |