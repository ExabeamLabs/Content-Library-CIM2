Rules by Product and UseCase
============================
Vendor: LiquidFiles
-------------------
### Product: [LiquidFiles](../ds_liquidfiles_liquidfiles.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   6   |   2    |         4          |       3        |    8    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-deleted        | <b>T1136 - Create Account</b><br> ↳ <b>A-ACCT-CR-DEL</b>: Account created and deleted on asset<br><br><b>T1531 - Account Access Removal</b><br> ↳ <b>AM-UA-AD-F</b>: First account deletion activity for user    |  • <b>AE-UA</b>: All activity for users    |
| account-password-reset | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| app-activity    | <b>T1098 - Account Manipulation</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions<br><br><b>T1098.002 - Account Manipulation: Exchange Email Delegate Permissions</b><br> ↳ <b>EM-InB-Ex</b>: A user has been given mailbox permissions for an executive user<br> ↳ <b>EM-InB-Perm-N-F</b>: First time a user has given mailbox permissions on another mailbox that is not their own<br> ↳ <b>EM-InB-Perm-N-A</b>: Abnormal for user to give mailbox permissions |  • <b>EM-InB-Perm-N</b>: Models users who give mailbox permissions |