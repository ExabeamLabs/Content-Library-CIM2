Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Monitor](../ds_microsoft_azure_monitor.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   9   |   4    |         4          |       3        |    3    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| app-activity    | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions    |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions    |
| cloud-admin-activity    | <b>T1078.004 - Valid Accounts: Cloud Accounts</b><br> ↳ <b>CA-UniversalPolicy-F</b>: First time this user has created/attached a 'universal' resource/action policy<br> ↳ <b>CA-UniversalPolicy-A</b>: Abnormal for this user to create/attach a 'universal' resource/action policy<br> ↳ <b>CS-IAM-Enumeration</b>: Enumeration of Cloud account roles/users<br> ↳ <b>CS-Admin-Activty-F</b>: First time seeing this Cloud administrative operation<br><br><b>T1136.003 - Create Account: Create: Cloud Account</b><br> ↳ <b>CS-User-Creation-F</b>: First time for this user to create an account in the cloud |  • <b>CS-Admin-Activity</b>: Cloud administrative activities performed by user<br> • <b>CS-User-Creation</b>: Users who create users/accounts in the cloud<br> • <b>CS-Universal-Policy</b>: Users creating universal '*' policies |