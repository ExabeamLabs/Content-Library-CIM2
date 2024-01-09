Vendor: Snort
=============
Product: Snort
--------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  25   |   11   |         3          |       1        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  network-alert<br> ↳[snort-s-str-alert-trigger-success-priority](Ps/pC_snortsstralerttriggersuccesspriority.md)<br> ↳[snort-s-json-alert-trigger-success-idssnort](Ps/pC_snortsjsonalerttriggersuccessidssnort.md)<br> ↳[snort-s-str-alert-trigger-success-snortids](Ps/pC_snortsstralerttriggersuccesssnortids.md)<br> | T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>21 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_snort_snort_Compromised_Credentials.md) |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-alert<br> ↳[snort-s-str-alert-trigger-success-priority](Ps/pC_snortsstralerttriggersuccesspriority.md)<br> ↳[snort-s-json-alert-trigger-success-idssnort](Ps/pC_snortsjsonalerttriggersuccessidssnort.md)<br> ↳[snort-s-str-alert-trigger-success-snortids](Ps/pC_snortsstralerttriggersuccesssnortids.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_snort_snort_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion                                                                                                                                                                                            | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     |              |        |