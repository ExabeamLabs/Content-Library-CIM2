Vendor: Teradata
================
Product: Teradata RDBMS
-----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[teradata-rdbms-str-database-login-success-req8](Ps/pC_teradatardbmsstrdatabaseloginsuccessreq8.md)<br><br> database-query<br> ↳[teradata-rdbms-str-database-query-success-req2](Ps/pC_teradatardbmsstrdatabasequerysuccessreq2.md)<br> ↳[teradata-rdbms-str-database-query-success-req4](Ps/pC_teradatardbmsstrdatabasequerysuccessreq4.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_teradata_teradata_rdbms_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[teradata-rdbms-str-database-login-success-req8](Ps/pC_teradatardbmsstrdatabaseloginsuccessreq8.md)<br><br> database-query<br> ↳[teradata-rdbms-str-database-query-success-req2](Ps/pC_teradatardbmsstrdatabasequerysuccessreq2.md)<br> ↳[teradata-rdbms-str-database-query-success-req4](Ps/pC_teradatardbmsstrdatabasequerysuccessreq4.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_teradata_teradata_rdbms_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |