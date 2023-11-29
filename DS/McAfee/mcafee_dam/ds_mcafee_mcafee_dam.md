Vendor: McAfee
==============
Product: McAfee DAM
-------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  34   |   18   |         2          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-alert<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert](Ps/pC_mcafeemdamcefalerttriggersuccessalert.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>30 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_mcafee_mcafee_dam_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-alert<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert](Ps/pC_mcafeemdamcefalerttriggersuccessalert.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>30 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_mcafee_mcafee_dam_Data_Access.md)    |
|       [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)       |  database-alert<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert](Ps/pC_mcafeemdamcefalerttriggersuccessalert.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_mcafee_mcafee_dam_Data_Exfiltration.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  database-alert<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert](Ps/pC_mcafeemdamcefalerttriggersuccessalert.md)<br> ↳[mcafee-mdam-cef-alert-trigger-success-alert-1](Ps/pC_mcafeemdamcefalerttriggersuccessalert1.md)<br> | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_mcafee_mcafee_dam_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |