Rules by Product and UseCase
============================
Vendor: Barracuda
-----------------
### Product: [Barracuda Cloudgen Firewall](../ds_barracuda_barracuda_cloudgen_firewall.md)
### Use-Case: [Privilege Abuse](../../../../UseCases/uc_privilege_abuse.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  15   |   9    |         5          |       4        |    4    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>SEQ-UH-04</b>: Failed logon by a service account<br> ↳ <b>SEQ-UH-05</b>: Failed interactive logon by a service account<br> ↳ <b>SEQ-UH-12</b>: Logon attempt on a disabled account    |  • <b>AE-UA</b>: All activity for users    |
| remote-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UH-I</b>: Interactive logon using a service account<br> ↳ <b>SL-UH-A</b>: Abnormal access from asset for a service account<br> ↳ <b>AL-F-F-CS</b>: First logon to a critical system for user<br> ↳ <b>AL-F-A-CS</b>: Abnormal logon to a critical system for user<br> ↳ <b>AL-UH-CS-NC</b>: Logon to a critical system for a user with no information<br> ↳ <b>AL-OU-F-CS</b>: First logon to a critical system that user has not previously accessed<br> ↳ <b>AL-HT-PRIV</b>: Non-Privileged logon to privileged asset<br> ↳ <b>AL-HT-EXEC-new</b>: New user logon to executive asset<br> ↳ <b>DC18-new</b>: Account switch by new user<br><br><b>T1078.002 - T1078.002</b><br> ↳ <b>SL-UH-I</b>: Interactive logon using a service account<br> ↳ <b>SL-UH-A</b>: Abnormal access from asset for a service account |  • <b>AL-HT-EXEC</b>: Executive Assets<br> • <b>AL-HT-PRIV</b>: Privilege Users Assets<br> • <b>AL-OU-CS</b>: Logon to critical servers<br> • <b>RA-UH</b>: Assets accessed by this user remotely<br> • <b>AL-UsH</b>: Source hosts per User<br> • <b>IL-UH-SA</b>: Interactive logon hosts for service accounts |
| vpn-login    | <b>T1078 - Valid Accounts</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account<br><br><b>T1133 - External Remote Services</b><br> ↳ <b>SL-UA-F-VPN</b>: First VPN connection for service account    |    |
| vpn-logout   | <b>T1078 - Valid Accounts</b><br> ↳ <b>WPA-UACount</b>: Abnormal number of privilege access events for user<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.    |  • <b>WPA-UACount</b>: Count of admin privilege events for user<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user.    |