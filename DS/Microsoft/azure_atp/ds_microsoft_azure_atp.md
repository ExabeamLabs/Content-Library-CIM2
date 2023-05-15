Vendor: Microsoft
=================
Product: Azure ATP
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  51   |   30   |         5          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-query<br> ↳[microsoft-mssql-xml-database-query-success-33205-1](Ps/pC_microsoftmssqlxmldatabasequerysuccess332051.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205](Ps/pC_microsoftmssqlkvdatabasequerysuccess33205.md)<br> ↳[microsoft-mssql-xml-database-query-success-33205](Ps/pC_microsoftmssqlxmldatabasequerysuccess33205.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205-1](Ps/pC_microsoftmssqlkvdatabasequerysuccess332051.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205-2](Ps/pC_microsoftmssqlkvdatabasequerysuccess332052.md)<br> ↳[microsoft-mssql-xml-database-query-success-30205-2](Ps/pC_microsoftmssqlxmldatabasequerysuccess302052.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_microsoft_azure_atp_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-query<br> ↳[microsoft-mssql-xml-database-query-success-33205-1](Ps/pC_microsoftmssqlxmldatabasequerysuccess332051.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205](Ps/pC_microsoftmssqlkvdatabasequerysuccess33205.md)<br> ↳[microsoft-mssql-xml-database-query-success-33205](Ps/pC_microsoftmssqlxmldatabasequerysuccess33205.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205-1](Ps/pC_microsoftmssqlkvdatabasequerysuccess332051.md)<br> ↳[microsoft-mssql-kv-database-query-success-33205-2](Ps/pC_microsoftmssqlkvdatabasequerysuccess332052.md)<br> ↳[microsoft-mssql-xml-database-query-success-30205-2](Ps/pC_microsoftmssqlxmldatabasequerysuccess302052.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>18 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_microsoft_azure_atp_Data_Access.md)    |
[Next Page -->>](2_ds_microsoft_azure_atp.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |