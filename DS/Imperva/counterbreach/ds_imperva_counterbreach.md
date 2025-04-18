Vendor: Imperva
===============
Product: CounterBreach
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  34   |   18   |         2          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  alert-trigger:success (database-alert)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>30 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_imperva_counterbreach_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  alert-trigger:success (database-alert)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> | T1213 - Data from Information Repositories<br> | [<ul><li>30 Rules</li></ul><ul><li>16 Models</li></ul>](RM/r_m_imperva_counterbreach_Data_Access.md)    |
|       [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)       |  alert-trigger:success (database-alert)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_imperva_counterbreach_Data_Exfiltration.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (database-alert)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> ↳[imperva-counterbreach-cef-alert-trigger-success-accessedtables](Ps/pC_impervacounterbreachcefalerttriggersuccessaccessedtables.md)<br> | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_imperva_counterbreach_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control | Exfiltration | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------- | ------------ | ------ |
|                |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> |                     |              |        |