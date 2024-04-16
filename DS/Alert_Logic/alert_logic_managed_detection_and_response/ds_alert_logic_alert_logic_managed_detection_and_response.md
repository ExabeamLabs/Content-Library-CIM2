Vendor: Alert Logic
===================
Product: Alert Logic Managed Detection and Response
---------------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  28   |   11   |         3          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  network-alert<br> ↳[alertlogic-al-json-alert-trigger-success-ids](Ps/pC_alertlogicaljsonalerttriggersuccessids.md)<br> ↳[alertlogic-al-json-alert-trigger-success-ids](Ps/pC_alertlogicaljsonalerttriggersuccessids.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>24 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_alert_logic_alert_logic_managed_detection_and_response_Compromised_Credentials.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-alert<br> ↳[alertlogic-al-json-alert-trigger-success-ids](Ps/pC_alertlogicaljsonalerttriggersuccessids.md)<br> ↳[alertlogic-al-json-alert-trigger-success-ids](Ps/pC_alertlogicaljsonalerttriggersuccessids.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_alert_logic_alert_logic_managed_detection_and_response_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion                                                                                                                                                                                            | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |