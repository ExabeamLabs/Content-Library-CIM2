Vendor: Trend Micro
===================
Product: Trend Micro ScanMail
-----------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   20   |         4          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  config-change<br> ↳[trendmicro-scanmail-cef-configuration-modify-300101](Ps/pC_trendmicroscanmailcefconfigurationmodify300101.md)<br><br> dlp-alert<br> ↳[trendmicro-scanmail-cef-alert-trigger-success-100104](Ps/pC_trendmicroscanmailcefalerttriggersuccess100104.md)<br> ↳[trendmicro-scanmail-json-alert-trigger-success-wineventlog](Ps/pC_trendmicroscanmailjsonalerttriggersuccesswineventlog.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_trend_micro_trend_micro_scanmail_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  config-change<br> ↳[trendmicro-scanmail-cef-configuration-modify-300101](Ps/pC_trendmicroscanmailcefconfigurationmodify300101.md)<br><br> dlp-alert<br> ↳[trendmicro-scanmail-cef-alert-trigger-success-100104](Ps/pC_trendmicroscanmailcefalerttriggersuccess100104.md)<br> ↳[trendmicro-scanmail-json-alert-trigger-success-wineventlog](Ps/pC_trendmicroscanmailjsonalerttriggersuccesswineventlog.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_trend_micro_trend_micro_scanmail_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  config-change<br> ↳[trendmicro-scanmail-cef-configuration-modify-300101](Ps/pC_trendmicroscanmailcefconfigurationmodify300101.md)<br><br> dlp-alert<br> ↳[trendmicro-scanmail-cef-alert-trigger-success-100104](Ps/pC_trendmicroscanmailcefalerttriggersuccess100104.md)<br> ↳[trendmicro-scanmail-json-alert-trigger-success-wineventlog](Ps/pC_trendmicroscanmailjsonalerttriggersuccesswineventlog.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_trend_micro_trend_micro_scanmail_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |