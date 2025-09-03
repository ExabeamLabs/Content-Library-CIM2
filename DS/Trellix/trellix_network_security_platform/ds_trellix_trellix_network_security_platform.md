Vendor: Trellix
===============
Product: Trellix Network Security Platform
------------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  25   |   11   |         4          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  alert-trigger:success (network-alert)<br> ↳[mcafee-nsm-str-alert-trigger-success-attack](Ps/pC_mcafeensmstralerttriggersuccessattack.md)<br> ↳[mcafee-nsm-str-alert-trigger-success-attack](Ps/pC_mcafeensmstralerttriggersuccessattack.md)<br> | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>21 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_trellix_trellix_network_security_platform_Compromised_Credentials.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (network-alert)<br> ↳[mcafee-nsm-str-alert-trigger-success-attack](Ps/pC_mcafeensmstralerttriggersuccessattack.md)<br> ↳[mcafee-nsm-str-alert-trigger-success-attack](Ps/pC_mcafeensmstralerttriggersuccessattack.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_trellix_trellix_network_security_platform_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion                                                                                                                                                                                            | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |