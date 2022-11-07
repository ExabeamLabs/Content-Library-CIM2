Vendor: Zeek
============
Product: zeek
-------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  37   |   16   |     3      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br> | [<ul><li>32 Rules</li></ul><ul><li>15 Models</li></ul>](RM/r_m_zeek_zeek_Data_Leak.md)          |
|    [Malware](../../../UseCases/uc_malware.md)    |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1190 - Exploit Public Fasing Application<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_zeek_zeek_Malware.md)    |
|    [Phishing](../../../UseCases/uc_phishing.md)    |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br> | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_zeek_zeek_Phishing.md)    |
|      [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)      |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_zeek_zeek_Privilege_Abuse.md)    |
|  [Privileged Activity](../../../UseCases/uc_privileged_activity.md)  |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_zeek_zeek_Privileged_Activity.md)    |
| [Workforce Protection](../../../UseCases/uc_workforce_protection.md) |  dlp-email-alert-in<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br><br> dlp-email-alert-out<br> ↳[zeek-z-json-email-send-receive-rcptto](Ps/pC_zeekzjsonemailsendreceivercptto.md)<br> | T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol<br> | [<ul><li>4 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_zeek_zeek_Workforce_Protection.md) |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                                                                                                            | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration                                                                                                                                                                                                                                         | Impact |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   |           |                  |            |                     | [Exfiltration Over Alternative Protocol](https://attack.mitre.org/techniques/T1048)<br><br>[Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted/Obfuscated Non-C2 Protocol](https://attack.mitre.org/techniques/T1048/003)<br><br> |        |