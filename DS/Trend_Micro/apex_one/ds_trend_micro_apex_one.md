Vendor: Trend Micro
===================
Product: Apex One
-----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  34   |   13   |         9          |       3        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  alert-trigger:success (security-alert)<br> ↳[trendmicro-ddi-cef-alert-trigger-success-473](Ps/pC_trendmicroddicefalerttriggersuccess473.md)<br>    | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>T1078 - Valid Accounts<br>T1133 - External Remote Services<br>T1190 - Exploit Public Fasing Application<br> | [<ul><li>23 Rules</li></ul><ul><li>9 Models</li></ul>](RM/r_m_trend_micro_apex_one_Compromised_Credentials.md) |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  email-send:fail (dlp-email-alert-out-failed)<br> ↳[trendmicro-apexone-cef-email-receive-fail-apexcentral](Ps/pC_trendmicroapexonecefemailreceivefailapexcentral.md)<br>    | T1048 - Exfiltration Over Alternative Protocol<br>T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br>    | [<ul><li>3 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_trend_micro_apex_one_Data_Leak.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  alert-trigger:success (security-alert)<br> ↳[trendmicro-ddi-cef-alert-trigger-success-473](Ps/pC_trendmicroddicefalerttriggersuccess473.md)<br>    | T1027 - Obfuscated Files or Information<br>T1027.005 - Obfuscated Files or Information: Indicator Removal from Tools<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_trend_micro_apex_one_Lateral_Movement.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (security-alert)<br> ↳[trendmicro-ddi-cef-alert-trigger-success-473](Ps/pC_trendmicroddicefalerttriggersuccess473.md)<br>    | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_trend_micro_apex_one_Malware.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  email-receive:fail (dlp-email-alert-in-failed)<br> ↳[trendmicro-apexone-cef-email-receive-fail-apexcentral](Ps/pC_trendmicroapexonecefemailreceivefailapexcentral.md)<br><br> email-send:fail (dlp-email-alert-out-failed)<br> ↳[trendmicro-apexone-cef-email-receive-fail-apexcentral](Ps/pC_trendmicroapexonecefemailreceivefailapexcentral.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_trend_micro_apex_one_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  email-receive:fail (dlp-email-alert-in-failed)<br> ↳[trendmicro-apexone-cef-email-receive-fail-apexcentral](Ps/pC_trendmicroapexonecefemailreceivefailapexcentral.md)<br><br> email-send:fail (dlp-email-alert-out-failed)<br> ↳[trendmicro-apexone-cef-email-receive-fail-apexcentral](Ps/pC_trendmicroapexonecefemailreceivefailapexcentral.md)<br><br> alert-trigger:success (security-alert)<br> ↳[trendmicro-ddi-cef-alert-trigger-success-473](Ps/pC_trendmicroddicefalerttriggersuccess473.md)<br> | T1068 - Exploitation for Privilege Escalation<br>T1078 - Valid Accounts<br>    | [<ul><li>2 Rules</li></ul>](RM/r_m_trend_micro_apex_one_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                                                                                                         | Execution | Persistence                                                                                                                                      | Privilege Escalation                                                                                                                                          | Defense Evasion                                                                                                                                                                                                                                                               | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration                                                                                                                                                                                                                                         | Impact |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [External Remote Services](https://attack.mitre.org/techniques/T1133)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploitation for Privilege Escalation](https://attack.mitre.org/techniques/T1068)<br><br> | [Obfuscated Files or Information: Indicator Removal from Tools](https://attack.mitre.org/techniques/T1027/005)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027)<br><br> |                   |           |                  |            |                     | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol](https://attack.mitre.org/techniques/T1048/003)<br><br> |        |