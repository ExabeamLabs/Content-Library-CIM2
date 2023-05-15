Vendor: FireEye
===============
Product: FireEye CMS
--------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   20   |         4          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[fireeye-escm-json-alert-trigger-success-fireeyecm](Ps/pC_fireeyeescmjsonalerttriggersuccessfireeyecm.md)<br> ↳[fireeye-networksecurity-leef-alert-trigger-success-malwareobject](Ps/pC_fireeyenetworksecurityleefalerttriggersuccessmalwareobject.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-fenotify](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccessfenotify.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_cms_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[fireeye-escm-json-alert-trigger-success-fireeyecm](Ps/pC_fireeyeescmjsonalerttriggersuccessfireeyecm.md)<br> ↳[fireeye-networksecurity-leef-alert-trigger-success-malwareobject](Ps/pC_fireeyenetworksecurityleefalerttriggersuccessmalwareobject.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-fenotify](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccessfenotify.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_cms_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  dlp-alert<br> ↳[fireeye-escm-json-alert-trigger-success-fireeyecm](Ps/pC_fireeyeescmjsonalerttriggersuccessfireeyecm.md)<br> ↳[fireeye-networksecurity-leef-alert-trigger-success-malwareobject](Ps/pC_fireeyenetworksecurityleefalerttriggersuccessmalwareobject.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-fenotify](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccessfenotify.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_fireeye_fireeye_cms_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |