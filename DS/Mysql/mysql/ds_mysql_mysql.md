Vendor: Mysql
=============
Product: Mysql
--------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  19   |   11   |         1          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-query<br> ↳[mysql-m-csv-database-query-success-query](Ps/pC_mysqlmcsvdatabasequerysuccessquery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_mysql_mysql_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-query<br> ↳[mysql-m-csv-database-query-success-query](Ps/pC_mysqlmcsvdatabasequerysuccessquery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_mysql_mysql_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |