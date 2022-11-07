Vendor: MariaDB
===============
Product: MariaDB
----------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  10   |   5    |     1      |       4        |    4    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  ""database-logout:success""<br> ↳[mariadb-m-str-database-logout-success-disconnect](Ps/pC_mariadbmstrdatabaselogoutsuccessdisconnect.md)<br><br> database-failed-login<br> ↳[mariadb-m-csv-database-login-fail-failedconnect](Ps/pC_mariadbmcsvdatabaseloginfailfailedconnect.md)<br><br> database-login<br> ↳[mariadb-m-csv-database-login-success-connect-1](Ps/pC_mariadbmcsvdatabaseloginsuccessconnect1.md)<br> ↳[mariadb-m-csv-database-login-success-connect](Ps/pC_mariadbmcsvdatabaseloginsuccessconnect.md)<br><br> database-update<br> ↳[mariadb-m-csv-database-modify-success-write](Ps/pC_mariadbmcsvdatabasemodifysuccesswrite.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_mariadb_mariadb_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  ""database-logout:success""<br> ↳[mariadb-m-str-database-logout-success-disconnect](Ps/pC_mariadbmstrdatabaselogoutsuccessdisconnect.md)<br><br> database-failed-login<br> ↳[mariadb-m-csv-database-login-fail-failedconnect](Ps/pC_mariadbmcsvdatabaseloginfailfailedconnect.md)<br><br> database-login<br> ↳[mariadb-m-csv-database-login-success-connect-1](Ps/pC_mariadbmcsvdatabaseloginsuccessconnect1.md)<br> ↳[mariadb-m-csv-database-login-success-connect](Ps/pC_mariadbmcsvdatabaseloginsuccessconnect.md)<br><br> database-update<br> ↳[mariadb-m-csv-database-modify-success-write](Ps/pC_mariadbmcsvdatabasemodifysuccesswrite.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_mariadb_mariadb_Data_Access.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |