Vendor: IBM
===========
Product: IBM
------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  10   |   5    |     1      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-failed-login<br> ↳[ibm-db2-kv-database-login-fail-validate](Ps/pC_ibmdb2kvdatabaseloginfailvalidate.md)<br><br> database-login<br> ↳[ibm-db2-kv-database-login-fail-validate](Ps/pC_ibmdb2kvdatabaseloginfailvalidate.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_ibm_ibm_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-failed-login<br> ↳[ibm-db2-kv-database-login-fail-validate](Ps/pC_ibmdb2kvdatabaseloginfailvalidate.md)<br><br> database-login<br> ↳[ibm-db2-kv-database-login-fail-validate](Ps/pC_ibmdb2kvdatabaseloginfailvalidate.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_ibm_ibm_Data_Access.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |