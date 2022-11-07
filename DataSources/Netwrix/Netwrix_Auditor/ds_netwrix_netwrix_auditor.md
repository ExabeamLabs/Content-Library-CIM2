Vendor: Netwrix
===============
Product: Netwrix Auditor
------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  49   |   17   |     6      |       7        |    7    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-lockout<br> ↳[netwrix-auditor-cef-user-lock-success-useraccount](Ps/pC_netwrixauditorcefuserlocksuccessuseraccount.md)<br><br> account-password-reset<br> ↳[netwrix-auditor-cef-user-password-reset-success-administrativepasswordreset](Ps/pC_netwrixauditorcefuserpasswordresetsuccessadministrativepasswordreset.md)<br><br> app-login<br> ↳[netwrix-auditor-cef-app-login-success-successfullogon](Ps/pC_netwrixauditorcefapploginsuccesssuccessfullogon.md)<br><br> database-access<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br><br> database-failed-login<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br><br> failed-app-login<br> ↳[netwrix-auditor-cef-app-login-fail-failedlogon](Ps/pC_netwrixauditorcefapploginfailfailedlogon.md)<br><br> nac-failed-logon<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br> | T1078 - Valid Accounts<br>T1110 - Brute Force<br>T1133 - External Remote Services<br> | [<ul><li>16 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_netwrix_netwrix_auditor_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  account-lockout<br> ↳[netwrix-auditor-cef-user-lock-success-useraccount](Ps/pC_netwrixauditorcefuserlocksuccessuseraccount.md)<br><br> account-password-reset<br> ↳[netwrix-auditor-cef-user-password-reset-success-administrativepasswordreset](Ps/pC_netwrixauditorcefuserpasswordresetsuccessadministrativepasswordreset.md)<br><br> app-login<br> ↳[netwrix-auditor-cef-app-login-success-successfullogon](Ps/pC_netwrixauditorcefapploginsuccesssuccessfullogon.md)<br><br> database-access<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br><br> database-failed-login<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br><br> failed-app-login<br> ↳[netwrix-auditor-cef-app-login-fail-failedlogon](Ps/pC_netwrixauditorcefapploginfailfailedlogon.md)<br><br> nac-failed-logon<br> ↳[netwrix-auditor-kv-database-who](Ps/pC_netwrixauditorkvdatabasewho.md)<br> | T1098 - Account Manipulation<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_netwrix_netwrix_auditor_Account_Manipulation.md)    |
[Next Page -->>](2_ds_netwrix_netwrix_auditor.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                               | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------------------------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Brute Force](https://attack.mitre.org/techniques/T1110)<br><br> |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |