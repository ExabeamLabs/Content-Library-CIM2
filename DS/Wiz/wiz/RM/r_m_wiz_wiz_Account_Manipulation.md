Rules by Product and UseCase
============================
Vendor: Wiz
-----------
### Product: [Wiz](../ds_wiz_wiz.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   2   |   1    |         2          |       1        |    0    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| account-deleted | <b>T1136 - Create Account</b><br> ↳ <b>A-ACCT-CR-DEL</b>: Account created and deleted on asset<br><br><b>T1531 - Account Access Removal</b><br> ↳ <b>AM-UA-AD-F</b>: First account deletion activity for user |  • <b>AE-UA</b>: All activity for users |