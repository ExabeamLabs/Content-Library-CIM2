Rules by Product and UseCase
============================
Vendor: Microsoft
-----------------
### Product: [Azure Active Directory](../ds_microsoft_azure_active_directory.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   4   |   1    |     2      |       5        |    5    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| account-password-reset  | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| app-activity    | <b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions |