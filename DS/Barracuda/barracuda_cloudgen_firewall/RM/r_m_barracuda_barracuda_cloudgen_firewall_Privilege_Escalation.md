Rules by Product and UseCase
============================
Vendor: Barracuda
-----------------
### Product: [Barracuda Cloudgen Firewall](../ds_barracuda_barracuda_cloudgen_firewall.md)
### Use-Case: [Privilege Escalation](../../../../UseCases/uc_privilege_escalation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   6    |         6          |       3        |    3    |

| Event Type   | Rules    | Models    |
| ---- | ---- | ---- |
| failed-logon | <b>T1210 - Exploitation of Remote Services</b><br> ↳ <b>A-Suspicious-Zerologon</b>: Failed authentication attempt on this asset.    |    |
| remote-logon | <b>T1078 - Valid Accounts</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user<br> ↳ <b>DC18-new</b>: Account switch by new user<br><br><b>T1555 - Credentials from Password Stores</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-UHWoPC</b>: Access to Password Vault managed asset with no password checkout for user    |  • <b>AS-PV-OA</b>: Password retrieval based accounts    |
| vpn-logout   | <b>T1555 - Credentials from Password Stores</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1555.005 - T1555.005</b><br> ↳ <b>AS-PV-USCOUNT-A</b>: Abnormal number of password safes used by user<br> ↳ <b>AS-PV-OSize-A</b>: Abnormal number of password retrievals in the organization<br> ↳ <b>AS-PV-GSize-A</b>: Abnormal number of password retrievals in the peer group<br> ↳ <b>AS-PV-USize-A</b>: Abnormal number of password retrievals in the user<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user. |  • <b>AS-PV-USize</b>: Count of password retrievals in a session for the user<br> • <b>AS-PV-GSize</b>: Count of password retrievals in a session for the peer group<br> • <b>AS-PV-OSize</b>: Count of password retrievals in a session for the organization<br> • <b>AS-PV-USCOUNT</b>: Count of safe values accessed in a session<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user. |