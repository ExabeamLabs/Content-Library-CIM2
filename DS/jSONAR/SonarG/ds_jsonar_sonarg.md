Vendor: jSONAR
==============
Product: SonarG
---------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  10   |   5    |     1      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[jsonar-sonarg-json-database-login-success-sonarw](Ps/pC_jsonarsonargjsondatabaseloginsuccesssonarw.md)<br> ↳[jsonar-sonarg-leef-database-login-success-logout](Ps/pC_jsonarsonargleefdatabaseloginsuccesslogout.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_jsonar_sonarg_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[jsonar-sonarg-json-database-login-success-sonarw](Ps/pC_jsonarsonargjsondatabaseloginsuccesssonarw.md)<br> ↳[jsonar-sonarg-leef-database-login-success-logout](Ps/pC_jsonarsonargleefdatabaseloginsuccesslogout.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_jsonar_sonarg_Data_Access.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |