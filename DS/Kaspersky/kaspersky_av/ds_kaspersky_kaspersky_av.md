Vendor: Kaspersky
=================
Product: Kaspersky AV
---------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   2    |         2          |       1        |    0    |

|    Use-Case    | Activity Types(Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
|   [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)   |  alert-trigger:success(file-alert)<br> ↳[kaspersky-av-cef-alert-trigger-success-objnotprocessed](Ps/pC_kasperskyavcefalerttriggersuccessobjnotprocessed.md)<br> | TA0002 - TA0002<br>        | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_kaspersky_kaspersky_av_Data_Exfiltration.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success(file-alert)<br> ↳[kaspersky-av-cef-alert-trigger-success-objnotprocessed](Ps/pC_kasperskyavcefalerttriggersuccessobjnotprocessed.md)<br> | TA0002 - TA0002<br>        | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_kaspersky_kaspersky_av_Malware.md)    |
|     [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)     |  alert-trigger:success(file-alert)<br> ↳[kaspersky-av-cef-alert-trigger-success-objnotprocessed](Ps/pC_kasperskyavcefalerttriggersuccessobjnotprocessed.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_kaspersky_kaspersky_av_Privilege_Abuse.md)    |
| [Privileged Activity](../../../UseCases/uc_privileged_activity.md) |  alert-trigger:success(file-alert)<br> ↳[kaspersky-av-cef-alert-trigger-success-objnotprocessed](Ps/pC_kasperskyavcefalerttriggersuccessobjnotprocessed.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_kaspersky_kaspersky_av_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |