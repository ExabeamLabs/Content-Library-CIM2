Vendor: Vectra
==============
Product: Vectra Cognito Detect
------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> dlp-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> dlp-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> dlp-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Malware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |