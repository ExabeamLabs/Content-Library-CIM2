Vendor: IMSS
============
Product: IMSS
-------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[imss-i-str-alert-trigger-success-dlpalert](Ps/pC_imssistralerttriggersuccessdlpalert.md)<br> ↳[imss-i-str-alert-trigger-success-securityalert](Ps/pC_imssistralerttriggersuccesssecurityalert.md)<br> ↳[imss-i-json-alert-trigger-success-spf](Ps/pC_imssijsonalerttriggersuccessspf.md)<br> ↳[imss-i-str-alert-trigger-success-antispamrules](Ps/pC_imssistralerttriggersuccessantispamrules.md)<br> ↳[imss-i-str-alert-trigger-success-spoofedemailfilter](Ps/pC_imssistralerttriggersuccessspoofedemailfilter.md)<br> ↳[imss-i-str-alert-trigger-success-capacityregulation](Ps/pC_imssistralerttriggersuccesscapacityregulation.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_imss_imss_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[imss-i-str-alert-trigger-success-dlpalert](Ps/pC_imssistralerttriggersuccessdlpalert.md)<br> ↳[imss-i-str-alert-trigger-success-securityalert](Ps/pC_imssistralerttriggersuccesssecurityalert.md)<br> ↳[imss-i-json-alert-trigger-success-spf](Ps/pC_imssijsonalerttriggersuccessspf.md)<br> ↳[imss-i-str-alert-trigger-success-antispamrules](Ps/pC_imssistralerttriggersuccessantispamrules.md)<br> ↳[imss-i-str-alert-trigger-success-spoofedemailfilter](Ps/pC_imssistralerttriggersuccessspoofedemailfilter.md)<br> ↳[imss-i-str-alert-trigger-success-capacityregulation](Ps/pC_imssistralerttriggersuccesscapacityregulation.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_imss_imss_Data_Leak.md)         |
[Next Page -->>](2_ds_imss_imss.md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |