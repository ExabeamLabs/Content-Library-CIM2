Vendor: Cisco
=============
Product: Cisco IOS
------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  ""app-notification:success""<br> ↳[cisco-ios-str-app-notification-success-isis](Ps/pC_ciscoiosstrappnotificationsuccessisis.md)<br><br> ""endpoint-notification:success""<br> ↳[cisco-ios-kv-endpoint-notification-success-endpointnotification](Ps/pC_ciscoioskvendpointnotificationsuccessendpointnotification.md)<br> ↳[cisco-ios-kv-endpoint-notification-success-endpointnotification-1](Ps/pC_ciscoioskvendpointnotificationsuccessendpointnotification1.md)<br><br> dlp-alert<br> ↳[cisco-ios-str-alert-trigger-success-snoopingdeny](Ps/pC_ciscoiosstralerttriggersuccesssnoopingdeny.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_cisco_cisco_ios_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  ""app-notification:success""<br> ↳[cisco-ios-str-app-notification-success-isis](Ps/pC_ciscoiosstrappnotificationsuccessisis.md)<br><br> ""endpoint-notification:success""<br> ↳[cisco-ios-kv-endpoint-notification-success-endpointnotification](Ps/pC_ciscoioskvendpointnotificationsuccessendpointnotification.md)<br> ↳[cisco-ios-kv-endpoint-notification-success-endpointnotification-1](Ps/pC_ciscoioskvendpointnotificationsuccessendpointnotification1.md)<br><br> dlp-alert<br> ↳[cisco-ios-str-alert-trigger-success-snoopingdeny](Ps/pC_ciscoiosstralerttriggersuccesssnoopingdeny.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_cisco_cisco_ios_Data_Leak.md)         |
[Next Page -->>](2_ds_cisco_cisco_ios.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |