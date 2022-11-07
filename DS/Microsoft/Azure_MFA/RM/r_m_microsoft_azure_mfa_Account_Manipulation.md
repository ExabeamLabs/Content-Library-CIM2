Vendor: Microsoft
=================
### Product: [Azure MFA](../ds_microsoft_azure_mfa.md)
### Use-Case: [Account Manipulation](../../../../UseCases/uc_account_manipulation.md)

| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|   2   |   1    |     2      |       7        |    7    |

| Event Type      | Rules    | Models    |
| ---- | ---- | ---- |
| account-deleted | <b>T1531 - Account Access Removal</b><br> ↳ <b>AM-UA-AD-F</b>: First account deletion activity for user<br><br><b>T1136 - Create Account</b><br> ↳ <b>A-ACCT-CR-DEL</b>: Account created and deleted on asset |  • <b>AE-UA</b>: All activity for users |