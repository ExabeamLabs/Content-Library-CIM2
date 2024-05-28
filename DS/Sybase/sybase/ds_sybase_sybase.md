Vendor: Sybase
==============
Product: Sybase
---------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       2        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[sybase-s-cef-database-login-success-login](Ps/pC_sybasescefdatabaseloginsuccesslogin.md)<br> ↳[sybase-s-json-database-login-success-login](Ps/pC_sybasesjsondatabaseloginsuccesslogin.md)<br><br> database-query<br> ↳[sybase-s-cef-database-query-success-selecttable](Ps/pC_sybasescefdatabasequerysuccessselecttable.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_sybase_sybase_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[sybase-s-cef-database-login-success-login](Ps/pC_sybasescefdatabaseloginsuccesslogin.md)<br> ↳[sybase-s-json-database-login-success-login](Ps/pC_sybasesjsondatabaseloginsuccesslogin.md)<br><br> database-query<br> ↳[sybase-s-cef-database-query-success-selecttable](Ps/pC_sybasescefdatabasequerysuccessselecttable.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_sybase_sybase_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |