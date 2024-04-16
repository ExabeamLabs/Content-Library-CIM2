Vendor: PostgreSQL
==================
Product: PostgreSQL
-------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  19   |   11   |         1          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[postgresql-p-csv-database-login-success-authentication](Ps/pC_postgresqlpcsvdatabaseloginsuccessauthentication.md)<br> ↳[postgresql-p-cef-database-178272478](Ps/pC_postgresqlpcefdatabase178272478.md)<br><br> database-query<br> ↳[postgresql-p-cef-database-178272478](Ps/pC_postgresqlpcefdatabase178272478.md)<br> ↳[postgresql-p-json-database-query-success-databasequery](Ps/pC_postgresqlpjsondatabasequerysuccessdatabasequery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_postgresql_postgresql_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[postgresql-p-csv-database-login-success-authentication](Ps/pC_postgresqlpcsvdatabaseloginsuccessauthentication.md)<br> ↳[postgresql-p-cef-database-178272478](Ps/pC_postgresqlpcefdatabase178272478.md)<br><br> database-query<br> ↳[postgresql-p-cef-database-178272478](Ps/pC_postgresqlpcefdatabase178272478.md)<br> ↳[postgresql-p-json-database-query-success-databasequery](Ps/pC_postgresqlpjsondatabasequerysuccessdatabasequery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>19 Rules</li></ul><ul><li>11 Models</li></ul>](RM/r_m_postgresql_postgresql_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |