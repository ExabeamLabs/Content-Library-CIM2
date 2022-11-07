Vendor: Sybase
==============
Product: Sybase
---------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  10   |   5    |     1      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  ""database-logout:success""<br> ↳[sybase-s-json-database-logout-logout](Ps/pC_sybasesjsondatabaselogoutlogout.md)<br><br> database-login<br> ↳[sybase-s-cef-database-login-success-login](Ps/pC_sybasescefdatabaseloginsuccesslogin.md)<br> ↳[sybase-s-json-database-login-success-login](Ps/pC_sybasesjsondatabaseloginsuccesslogin.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_sybase_sybase_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  ""database-logout:success""<br> ↳[sybase-s-json-database-logout-logout](Ps/pC_sybasesjsondatabaselogoutlogout.md)<br><br> database-login<br> ↳[sybase-s-cef-database-login-success-login](Ps/pC_sybasescefdatabaseloginsuccesslogin.md)<br> ↳[sybase-s-json-database-login-success-login](Ps/pC_sybasesjsondatabaseloginsuccesslogin.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_sybase_sybase_Data_Access.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |