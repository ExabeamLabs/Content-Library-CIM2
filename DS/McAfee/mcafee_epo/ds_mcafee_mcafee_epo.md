Vendor: McAfee
==============
Product: Mcafee EPO
-------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[mcafee-epo-xml-alert-trigger-success-1027](Ps/pC_mcafeeepoxmlalerttriggersuccess1027.md)<br> ↳[mcafee-epo-kv-alert-trigger-success-string](Ps/pC_mcafeeepokvalerttriggersuccessstring.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_mcafee_mcafee_epo_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[mcafee-epo-xml-alert-trigger-success-1027](Ps/pC_mcafeeepoxmlalerttriggersuccess1027.md)<br> ↳[mcafee-epo-kv-alert-trigger-success-string](Ps/pC_mcafeeepokvalerttriggersuccessstring.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_mcafee_mcafee_epo_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  dlp-alert<br> ↳[mcafee-epo-xml-alert-trigger-success-1027](Ps/pC_mcafeeepoxmlalerttriggersuccess1027.md)<br> ↳[mcafee-epo-kv-alert-trigger-success-string](Ps/pC_mcafeeepokvalerttriggersuccessstring.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_mcafee_mcafee_epo_Malware.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |