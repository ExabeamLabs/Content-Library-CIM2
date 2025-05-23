Vendor: Trellix
===============
Product: Trellix Database Security
----------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  40   |   21   |         2          |       2        |    2    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  alert-trigger:success (database-alert)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br><br> database-query:success (database-query)<br> ↳[mcafee-mdam-kv-database-dbactivity](Ps/pC_mcafeemdamkvdatabasedbactivity.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>36 Rules</li></ul><ul><li>19 Models</li></ul>](RM/r_m_trellix_trellix_database_security_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  alert-trigger:success (database-alert)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br><br> database-query:success (database-query)<br> ↳[mcafee-mdam-kv-database-dbactivity](Ps/pC_mcafeemdamkvdatabasedbactivity.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>36 Rules</li></ul><ul><li>19 Models</li></ul>](RM/r_m_trellix_trellix_database_security_Data_Access.md)    |
|       [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)       |  alert-trigger:success (database-alert)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br>    | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_trellix_trellix_database_security_Data_Exfiltration.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (database-alert)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br>    | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_trellix_trellix_database_security_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |