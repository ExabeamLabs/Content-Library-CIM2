Vendor: Halcyon
===============
Product: Halcyon
----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   5   |   2    |         2          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP          | Content    |
|:----:| ---- | ---- | ---- |
|   [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)   |  alert-trigger:success (file-alert)<br> ↳[halcyon-halcyon-json-alert-trigger-success-alert](Ps/pC_halcyonhalcyonjsonalerttriggersuccessalert.md)<br> | TA0002 - TA0002<br>        | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_halcyon_halcyon_Data_Exfiltration.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (file-alert)<br> ↳[halcyon-halcyon-json-alert-trigger-success-alert](Ps/pC_halcyonhalcyonjsonalerttriggersuccessalert.md)<br> | TA0002 - TA0002<br>        | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_halcyon_halcyon_Malware.md)    |
|     [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)     |  alert-trigger:success (file-alert)<br> ↳[halcyon-halcyon-json-alert-trigger-success-alert](Ps/pC_halcyonhalcyonjsonalerttriggersuccessalert.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_halcyon_halcyon_Privilege_Abuse.md)    |
| [Privileged Activity](../../../UseCases/uc_privileged_activity.md) |  alert-trigger:success (file-alert)<br> ↳[halcyon-halcyon-json-alert-trigger-success-alert](Ps/pC_halcyonhalcyonjsonalerttriggersuccessalert.md)<br> | T1078 - Valid Accounts<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_halcyon_halcyon_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     |              |        |