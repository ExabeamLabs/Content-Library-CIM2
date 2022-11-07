Vendor: Vectra
==============
Product: Vectra Cognito Detect
------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  32   |   12   |     6      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> security-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>25 Rules</li></ul><ul><li>10 Models</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Compromised_Credentials.md) |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> security-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> security-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Malware.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  ""app-notification:success""<br> ↳[vectra-cd-kv-app-notification-account](Ps/pC_vectracdkvappnotificationaccount.md)<br><br> security-alert<br> ↳[vectra-cd-kv-alert-trigger-success-detection](Ps/pC_vectracdkvalerttriggersuccessdetection.md)<br> ↳[vectra-cd-json-alert-trigger-success-headendaddr](Ps/pC_vectracdjsonalerttriggersuccessheadendaddr.md)<br> | T1068 - Exploitation for Privilege Escalation<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_vectra_vectra_cognito_detect_Privileged_Activity.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                               | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |