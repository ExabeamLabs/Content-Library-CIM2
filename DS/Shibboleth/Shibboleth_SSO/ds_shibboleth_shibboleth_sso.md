Vendor: Shibboleth
==================
Product: Shibboleth SSO
-----------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  41   |   17   |     5      |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  ""app-notification:success""<br> ↳[shibboleth-sso-kv-app-notification-warn](Ps/pC_shibbolethssokvappnotificationwarn.md)<br><br> account-password-change<br> ↳[shibboleth-sso-str-user-password-modify-success-passwordchange](Ps/pC_shibbolethssostruserpasswordmodifysuccesspasswordchange.md)<br><br> app-login<br> ↳[shibboleth-sso-str-app-login-success-shibbolethaudit](Ps/pC_shibbolethssostrapploginsuccessshibbolethaudit.md)<br> ↳[shibboleth-sso-str-app-login-success-3877](Ps/pC_shibbolethssostrapploginsuccess3877.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br> | [<ul><li>12 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_shibboleth_shibboleth_sso_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  ""app-notification:success""<br> ↳[shibboleth-sso-kv-app-notification-warn](Ps/pC_shibbolethssokvappnotificationwarn.md)<br><br> account-password-change<br> ↳[shibboleth-sso-str-user-password-modify-success-passwordchange](Ps/pC_shibbolethssostruserpasswordmodifysuccesspasswordchange.md)<br><br> app-login<br> ↳[shibboleth-sso-str-app-login-success-shibbolethaudit](Ps/pC_shibbolethssostrapploginsuccessshibbolethaudit.md)<br> ↳[shibboleth-sso-str-app-login-success-3877](Ps/pC_shibbolethssostrapploginsuccess3877.md)<br> | T1098 - Account Manipulation<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_shibboleth_shibboleth_sso_Account_Manipulation.md)    |
[Next Page -->>](2_ds_shibboleth_shibboleth_sso.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                                                                                               | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |