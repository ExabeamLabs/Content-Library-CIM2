Vendor: Cylance
===============
Product: Cylance PROTECT
------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   20   |         4          |       5        |    5    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  ""app-notification:success""<br> ↳[cylance-protect-xml-app-notification-8](Ps/pC_cylanceprotectxmlappnotification8.md)<br><br> ""endpoint-activity:success""<br> ↳[cylance-protect-kv-endpoint-activity-device](Ps/pC_cylanceprotectkvendpointactivitydevice.md)<br><br> ""endpoint-notification:success""<br> ↳[cylance-protect-xml-endpoint-notification-16](Ps/pC_cylanceprotectxmlendpointnotification16.md)<br><br> ""service-stop:success""<br> ↳[cylance-protect-xml-service-stop-success-0](Ps/pC_cylanceprotectxmlservicestopsuccess0.md)<br><br> dlp-alert<br> ↳[cylance-protect-json-alert-trigger-detection](Ps/pC_cylanceprotectjsonalerttriggerdetection.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_cylance_cylance_protect_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  ""app-notification:success""<br> ↳[cylance-protect-xml-app-notification-8](Ps/pC_cylanceprotectxmlappnotification8.md)<br><br> ""endpoint-activity:success""<br> ↳[cylance-protect-kv-endpoint-activity-device](Ps/pC_cylanceprotectkvendpointactivitydevice.md)<br><br> ""endpoint-notification:success""<br> ↳[cylance-protect-xml-endpoint-notification-16](Ps/pC_cylanceprotectxmlendpointnotification16.md)<br><br> ""service-stop:success""<br> ↳[cylance-protect-xml-service-stop-success-0](Ps/pC_cylanceprotectxmlservicestopsuccess0.md)<br><br> dlp-alert<br> ↳[cylance-protect-json-alert-trigger-detection](Ps/pC_cylanceprotectjsonalerttriggerdetection.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_cylance_cylance_protect_Data_Leak.md)         |
[Next Page -->>](2_ds_cylance_cylance_protect.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |