Rules by Product and UseCase
============================
Vendor: Password Manager Pro
----------------------------
### Product: [Password Manager Pro](../ds_password_manager_pro_password_manager_pro.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         3          |       3        |    4    |

| Event Type    | Rules    | Models    |
| ---- | ---- | ---- |
| account-deleted         | <b>T1136 - Create Account</b><br> ↳ <b>A-ACCT-CR-DEL</b>: Account created and deleted on asset<br><br><b>T1531 - Account Access Removal</b><br> ↳ <b>AM-UA-AD-F</b>: First account deletion activity for user |  • <b>AE-UA</b>: All activity for users |
| account-password-change | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |
| account-password-reset  | <b>T1098 - Account Manipulation</b><br> ↳ <b>AM-UA-APLocU-F</b>: First account password change for local user    |    |