Vendor: FireEye
===============
Product: FireEye Endpoint Security (HX)
---------------------------------------
| Rules | Models | MITRE TTPs | Activity Types | Parsers |
|:-----:|:------:|:----------:|:--------------:|:-------:|
|  33   |   20   |     4      |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[fireeye-endpointsecurity-cef-alert-trigger-containment](Ps/pC_fireeyeendpointsecuritycefalerttriggercontainment.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-fireeyehx](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessfireeyehx.md)<br> ↳[fireeye-endpointsecurity-cef-alert-trigger-success-iochitfound](Ps/pC_fireeyeendpointsecuritycefalerttriggersuccessiochitfound.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-ipv4networkevent](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessipv4networkevent.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-processevent](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessprocessevent.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_endpoint_security_(hx)_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[fireeye-endpointsecurity-cef-alert-trigger-containment](Ps/pC_fireeyeendpointsecuritycefalerttriggercontainment.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-fireeyehx](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessfireeyehx.md)<br> ↳[fireeye-endpointsecurity-cef-alert-trigger-success-iochitfound](Ps/pC_fireeyeendpointsecuritycefalerttriggersuccessiochitfound.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-ipv4networkevent](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessipv4networkevent.md)<br> ↳[fireeye-endpointsecurity-json-alert-trigger-success-processevent](Ps/pC_fireeyeendpointsecurityjsonalerttriggersuccessprocessevent.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_fireeye_fireeye_endpoint_security_(hx)_Data_Leak.md)         |
[Next Page -->>](2_ds_fireeye_fireeye_endpoint_security_(hx).md)

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |