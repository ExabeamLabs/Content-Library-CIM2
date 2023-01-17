Vendor: FireEye
===============
Product: FireEye Network Security (NX)
--------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[fireeye-networksecurity-cef-alert-trigger-success-mailciousmail](Ps/pC_fireeyenetworksecuritycefalerttriggersuccessmailciousmail.md)<br> ↳[fireeye-networksecurity-leef-alert-trigger-success-malwareobject](Ps/pC_fireeyenetworksecurityleefalerttriggersuccessmalwareobject.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-webmps](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccesswebmps.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-1alert](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccess1alert.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-fenotify](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccessfenotify.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_network_security_(nx)_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[fireeye-networksecurity-cef-alert-trigger-success-mailciousmail](Ps/pC_fireeyenetworksecuritycefalerttriggersuccessmailciousmail.md)<br> ↳[fireeye-networksecurity-leef-alert-trigger-success-malwareobject](Ps/pC_fireeyenetworksecurityleefalerttriggersuccessmalwareobject.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-webmps](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccesswebmps.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-1alert](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccess1alert.md)<br> ↳[fireeye-networksecurity-xml-alert-trigger-success-fenotify](Ps/pC_fireeyenetworksecurityxmlalerttriggersuccessfenotify.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_network_security_(nx)_Data_Leak.md)         |
[Next Page -->>](2_ds_fireeye_fireeye_network_security_(nx).md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |