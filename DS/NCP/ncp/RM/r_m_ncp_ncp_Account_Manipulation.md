Rules by Product and UseCase
============================
Vendor: NCP
-----------
### Product: [NCP](../ds_ncp_ncp.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   7   |   7    |         3          |       1        |    1    |

| Event Type | Rules    | Models    |
| ---------- | ---- | ---- |
| vpn-logout | <b>T1484 - Group Policy Modification</b><br> ↳ <b>FDS-Count</b>: Abnormal number of failed directory service events in the organization<br> ↳ <b>FDS-GCount</b>: Abnormal number of failed directory service events in the peer group<br> ↳ <b>FDS-UCount</b>: Abnormal number of failed directory service events in the user<br> ↳ <b>DS-Count</b>: Abnormal number of directory service events in the organization<br> ↳ <b>DS-GCount</b>: Abnormal number of directory service events in the peer group<br> ↳ <b>DS-UCount</b>: Abnormal number of directory service events in the user<br><br><b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user.<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Perm-A</b>: Abnormal number of mailbox permission given by user. |  • <b>DS-UCount</b>: Count of directory service activity events in the user<br> • <b>DS-GCount</b>: Count of directory service activity events in the peer group<br> • <b>DS-Count</b>: Count of directory service activity events in the organization<br> • <b>FDS-UCount</b>: Count of failed directory service activity events in the user<br> • <b>FDS-GCount</b>: Count of failed directory service activity events in the peer group<br> • <b>FDS-Count</b>: Count of failed directory service activity events in the organization<br> • <b>EM-InB-Perm</b>: Models the number of mailbox permissions given by this user. |