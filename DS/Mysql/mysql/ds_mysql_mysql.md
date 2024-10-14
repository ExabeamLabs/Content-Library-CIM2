Vendor: Mysql
=============
Product: Mysql
--------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       1        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-query:success (database-query)<br> ↳[mysql-m-csv-database-query-success-query](Ps/pC_mysqlmcsvdatabasequerysuccessquery.md)<br> ↳[mysql-m-json-database-query-success-activity](Ps/pC_mysqlmjsondatabasequerysuccessactivity.md)<br> ↳[mysql-m-csv-database-query-success-write](Ps/pC_mysqlmcsvdatabasequerysuccesswrite.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_mysql_mysql_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-query:success (database-query)<br> ↳[mysql-m-csv-database-query-success-query](Ps/pC_mysqlmcsvdatabasequerysuccessquery.md)<br> ↳[mysql-m-json-database-query-success-activity](Ps/pC_mysqlmjsondatabasequerysuccessactivity.md)<br> ↳[mysql-m-csv-database-query-success-write](Ps/pC_mysqlmcsvdatabasequerysuccesswrite.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_mysql_mysql_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |