Vendor: Tenable.io
==================
Product: Tenable.io
-------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  ""app-scan:success""<br> ↳[tenable-t-cef-app-scan-scaninformation](Ps/pC_tenabletcefappscanscaninformation.md)<br><br> dlp-alert<br> ↳[tenable-t-sk4-alert-trigger-vulnerability](Ps/pC_tenabletsk4alerttriggervulnerability.md)<br> ↳[tenable-t-sk4-alert-trigger-vulnerability-1](Ps/pC_tenabletsk4alerttriggervulnerability1.md)<br> ↳[tenable-t-json-alert-trigger-success-dcerpcservice](Ps/pC_tenabletjsonalerttriggersuccessdcerpcservice.md)<br> ↳[tenable-t-sk4-alert-trigger-success-dcerpcservice-1](Ps/pC_tenabletsk4alerttriggersuccessdcerpcservice1.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_tenable.io_tenable.io_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  ""app-scan:success""<br> ↳[tenable-t-cef-app-scan-scaninformation](Ps/pC_tenabletcefappscanscaninformation.md)<br><br> dlp-alert<br> ↳[tenable-t-sk4-alert-trigger-vulnerability](Ps/pC_tenabletsk4alerttriggervulnerability.md)<br> ↳[tenable-t-sk4-alert-trigger-vulnerability-1](Ps/pC_tenabletsk4alerttriggervulnerability1.md)<br> ↳[tenable-t-json-alert-trigger-success-dcerpcservice](Ps/pC_tenabletjsonalerttriggersuccessdcerpcservice.md)<br> ↳[tenable-t-sk4-alert-trigger-success-dcerpcservice-1](Ps/pC_tenabletsk4alerttriggersuccessdcerpcservice1.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_tenable.io_tenable.io_Data_Leak.md)         |
[Next Page -->>](2_ds_tenable.io_tenable.io.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |