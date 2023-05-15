Vendor: Amazon
==============
Product: Amazon RDS
-------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[amazon-ards-sk4-database-login-success-connectionauthorized](Ps/pC_amazonardssk4databaseloginsuccessconnectionauthorized.md)<br><br> database-query<br> ↳[amazon-rds-str-database-query-modify-success-auditevent](Ps/pC_amazonrdsstrdatabasequerymodifysuccessauditevent.md)<br> ↳[amazon-rds-str-database-query-modify-success-auditevent-1](Ps/pC_amazonrdsstrdatabasequerymodifysuccessauditevent1.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_amazon_amazon_rds_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[amazon-ards-sk4-database-login-success-connectionauthorized](Ps/pC_amazonardssk4databaseloginsuccessconnectionauthorized.md)<br><br> database-query<br> ↳[amazon-rds-str-database-query-modify-success-auditevent](Ps/pC_amazonrdsstrdatabasequerymodifysuccessauditevent.md)<br> ↳[amazon-rds-str-database-query-modify-success-auditevent-1](Ps/pC_amazonrdsstrdatabasequerymodifysuccessauditevent1.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_amazon_amazon_rds_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |