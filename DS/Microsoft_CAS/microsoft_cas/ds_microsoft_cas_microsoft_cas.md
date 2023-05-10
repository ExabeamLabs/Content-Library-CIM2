Vendor: Microsoft CAS
=====================
Product: Microsoft CAS
----------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   20   |         4          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[microsoft-mcas-json-alert-trigger-success-anomalydetection](Ps/pC_microsoftmcasjsonalerttriggersuccessanomalydetection.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-cabinetapppermission](Ps/pC_microsoftmcasjsonalerttriggersuccesscabinetapppermission.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-riskyipanonymous](Ps/pC_microsoftmcasjsonalerttriggersuccessriskyipanonymous.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-managementgeneric](Ps/pC_microsoftmcasjsonalerttriggersuccessmanagementgeneric.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_microsoft_cas_microsoft_cas_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[microsoft-mcas-json-alert-trigger-success-anomalydetection](Ps/pC_microsoftmcasjsonalerttriggersuccessanomalydetection.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-cabinetapppermission](Ps/pC_microsoftmcasjsonalerttriggersuccesscabinetapppermission.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-riskyipanonymous](Ps/pC_microsoftmcasjsonalerttriggersuccessriskyipanonymous.md)<br> ↳[microsoft-mcas-json-alert-trigger-success-managementgeneric](Ps/pC_microsoftmcasjsonalerttriggersuccessmanagementgeneric.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_microsoft_cas_microsoft_cas_Data_Leak.md)         |
[Next Page -->>](2_ds_microsoft_cas_microsoft_cas.md)

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |