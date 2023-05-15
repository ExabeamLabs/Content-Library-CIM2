Vendor: IBM
===========
Product: Guardium
-----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   10   |         1          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[ibm-guardium-csv-database-login-success-no](Ps/pC_ibmguardiumcsvdatabaseloginsuccessno.md)<br><br> database-query<br> ↳[ibm-guardium-kv-database-query-success-dbuser](Ps/pC_ibmguardiumkvdatabasequerysuccessdbuser.md)<br> ↳[ibm-guardium-leef-database-query-success-sql-1](Ps/pC_ibmguardiumleefdatabasequerysuccesssql1.md)<br> ↳[ibm-guardium-kv-database-query-success-sql](Ps/pC_ibmguardiumkvdatabasequerysuccesssql.md)<br> ↳[ibm-guardium-cef-database-query-success-command](Ps/pC_ibmguardiumcefdatabasequerysuccesscommand.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_ibm_guardium_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[ibm-guardium-csv-database-login-success-no](Ps/pC_ibmguardiumcsvdatabaseloginsuccessno.md)<br><br> database-query<br> ↳[ibm-guardium-kv-database-query-success-dbuser](Ps/pC_ibmguardiumkvdatabasequerysuccessdbuser.md)<br> ↳[ibm-guardium-leef-database-query-success-sql-1](Ps/pC_ibmguardiumleefdatabasequerysuccesssql1.md)<br> ↳[ibm-guardium-kv-database-query-success-sql](Ps/pC_ibmguardiumkvdatabasequerysuccesssql.md)<br> ↳[ibm-guardium-cef-database-query-success-command](Ps/pC_ibmguardiumcefdatabasequerysuccesscommand.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_ibm_guardium_Data_Access.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |