Rules by Product and UseCase
============================
Vendor: Cisco
-------------
### Product: [Cisco Remote Access Security](../ds_cisco_cisco_remote_access_security.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   5    |         4          |       1        |    3    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1555 - Credentials from Password Stores</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user. |  • <b>AS-PV-USize</b>: Count of password retrievals in a session for the user<br> • <b>AS-PV-GSize</b>: Count of password retrievals in a session for the peer group<br> • <b>AS-PV-OSize</b>: Count of password retrievals in a session for the organization<br> • <b>AS-PV-USCOUNT</b>: Count of safe values accessed in a session<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user. |