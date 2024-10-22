Vendor: Abnormal Security
=========================
Product: Abnormal Security
--------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  35   |   19   |         6          |       2        |    0    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
|   [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)   |  alert-trigger:success (dlp-alert)<br> ↳[abnormalsecurity-as-json-alert-trigger-success-attacktype-1](Ps/pC_abnormalsecurityasjsonalerttriggersuccessattacktype1.md)<br>    | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_abnormal_security_abnormal_security_Data_Exfiltration.md) |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  alert-trigger:success (dlp-alert)<br> ↳[abnormalsecurity-as-json-alert-trigger-success-attacktype-1](Ps/pC_abnormalsecurityasjsonalerttriggersuccessattacktype1.md)<br>    | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_abnormal_security_abnormal_security_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (dlp-alert)<br> ↳[abnormalsecurity-as-json-alert-trigger-success-attacktype-1](Ps/pC_abnormalsecurityasjsonalerttriggersuccessattacktype1.md)<br><br> email-receive:success (dlp-email-alert-in)<br> ↳[abnormalsecurity-as-json-email-receive-success-spam](Ps/pC_abnormalsecurityasjsonemailreceivesuccessspam.md)<br> | T1190 - Exploit Public Fasing Application<br>TA0002 - TA0002<br>    | [<ul><li>5 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_abnormal_security_abnormal_security_Malware.md)    |
|     [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)     |  email-receive:success (dlp-email-alert-in)<br> ↳[abnormalsecurity-as-json-email-receive-success-spam](Ps/pC_abnormalsecurityasjsonemailreceivesuccessspam.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_abnormal_security_abnormal_security_Privilege_Abuse.md)    |
| [Privileged Activity](../../../UseCases/uc_privileged_activity.md) |  email-receive:success (dlp-email-alert-in)<br> ↳[abnormalsecurity-as-json-email-receive-success-spam](Ps/pC_abnormalsecurityasjsonemailreceivesuccessspam.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_abnormal_security_abnormal_security_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                            | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |