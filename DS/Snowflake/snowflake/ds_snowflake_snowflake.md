Vendor: Snowflake
=================
Product: Snowflake
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       2        |    5    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login:success (database-login)<br> ↳[snowflake-s-sk4-database-login-success-login](Ps/pC_snowflakessk4databaseloginsuccesslogin.md)<br> ↳[snowflake-s-kv-database-login-success-login](Ps/pC_snowflakeskvdatabaseloginsuccesslogin.md)<br> ↳[snowflake-s-sk4-database-login-success-login-1](Ps/pC_snowflakessk4databaseloginsuccesslogin1.md)<br><br> database-query:success (database-query)<br> ↳[snowflake-s-sk4-database-query-success-queryhistory](Ps/pC_snowflakessk4databasequerysuccessqueryhistory.md)<br> ↳[snowflake-s-kv-database-query-success-databasequery](Ps/pC_snowflakeskvdatabasequerysuccessdatabasequery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_snowflake_snowflake_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login:success (database-login)<br> ↳[snowflake-s-sk4-database-login-success-login](Ps/pC_snowflakessk4databaseloginsuccesslogin.md)<br> ↳[snowflake-s-kv-database-login-success-login](Ps/pC_snowflakeskvdatabaseloginsuccesslogin.md)<br> ↳[snowflake-s-sk4-database-login-success-login-1](Ps/pC_snowflakessk4databaseloginsuccesslogin1.md)<br><br> database-query:success (database-query)<br> ↳[snowflake-s-sk4-database-query-success-queryhistory](Ps/pC_snowflakessk4databasequerysuccessqueryhistory.md)<br> ↳[snowflake-s-kv-database-query-success-databasequery](Ps/pC_snowflakeskvdatabasequerysuccessdatabasequery.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_snowflake_snowflake_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |