Vendor: OpenLDAP
================
Product: OpenLDAP
-----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  44   |   12   |         9          |       5        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  user-create:success (account-creation)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br><br> user-delete:success (account-deleted)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br><br> user-password-modify:success (account-password-change)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br><br> endpoint-login:fail (authentication-failed)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br> ↳[openldap-o-str-user-success-err](Ps/pC_openldapostrusersuccesserr.md)<br><br> endpoint-login:success (authentication-successful)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br> ↳[openldap-o-str-user-success-err](Ps/pC_openldapostrusersuccesserr.md)<br> | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>15 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_openldap_openldap_Abnormal_Authentication_&_Access.md) |
|    [Account Manipulation](../../../UseCases/uc_account_manipulation.md)    |  user-create:success (account-creation)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br><br> user-delete:success (account-deleted)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br><br> user-password-modify:success (account-password-change)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br>    | T1098 - Account Manipulation<br>T1136 - Create Account<br>T1136.001 - Create Account: Create: Local Account<br>T1136.002 - T1136.002<br>T1531 - Account Access Removal<br> | [<ul><li>22 Rules</li></ul><ul><li>8 Models</li></ul>](RM/r_m_openldap_openldap_Account_Manipulation.md)    |
|          [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md)          |  endpoint-login:success (authentication-successful)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br> ↳[openldap-o-str-user-success-err](Ps/pC_openldapostrusersuccesserr.md)<br>    | T1078 - Valid Accounts<br>T1133 - External Remote Services<br>    | [<ul><li>7 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_openldap_openldap_Compromised_Credentials.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  endpoint-login:success (authentication-successful)<br> ↳[openldap-o-str-user-success-fd](Ps/pC_openldapostrusersuccessfd.md)<br> ↳[openldap-o-str-user-success-op](Ps/pC_openldapostrusersuccessop.md)<br> ↳[openldap-o-str-user-success-err](Ps/pC_openldapostrusersuccesserr.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_openldap_openldap_Malware.md)    |
[Next Page -->>](2_ds_openldap_openldap.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                   | Execution | Persistence                                                                                                                                                                                                                                                                                                                                                                                | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                                                                                       | Exfiltration | Impact                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------------------------------------------------------------------- |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Create Account](https://attack.mitre.org/techniques/T1136)<br><br>[External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br>[Create Account: Create: Local Account](https://attack.mitre.org/techniques/T1136/001)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              | [Account Access Removal](https://attack.mitre.org/techniques/T1531)<br><br> |