Vendor: Ordr
============
Product: Ordr SCE
-----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   3   |   1    |         2          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  network-alert<br> ↳[ordr-sce-json-alert-trigger-success-warning](Ps/pC_ordrscejsonalerttriggersuccesswarning.md)<br> | T1190 - Exploit Public Fasing Application<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_ordr_ordr_sce_Compromised_Credentials.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-alert<br> ↳[ordr-sce-json-alert-trigger-success-warning](Ps/pC_ordrscejsonalerttriggersuccesswarning.md)<br> | TA0002 - TA0002<br>    | [<ul><li>2 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_ordr_ordr_sce_Malware.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  |            |                     |              |        |