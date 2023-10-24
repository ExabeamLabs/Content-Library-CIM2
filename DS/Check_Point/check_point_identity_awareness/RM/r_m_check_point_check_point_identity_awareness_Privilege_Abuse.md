Rules by Product and UseCase
============================
Vendor: Check Point
-------------------
### Product: [Check Point Identity Awareness](../ds_check_point_check_point_identity_awareness.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   2    |         3          |       2        |    2    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-login  | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account    |    |
| vpn-logout | <b>T1078 - Valid Accounts</b><br> ↳ <b>WPA-UACount</b>: Abnormal number of privilege access events for user<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user. |  • <b>WPA-UACount</b>: Count of admin privilege events for user<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user. |