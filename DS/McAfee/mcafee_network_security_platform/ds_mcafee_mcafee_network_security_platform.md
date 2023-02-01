Vendor: McAfee
==============
Product: McAfee Network Security Platform
-----------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   20   |         4          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  dlp-alert<br> ↳[mcafee-nsp-cef-alert-trigger-success-securitymanager](Ps/pC_mcafeenspcefalerttriggersuccesssecuritymanager.md)<br> ↳[mcafee-nsp-json-alert-trigger-success-threatsource](Ps/pC_mcafeenspjsonalerttriggersuccessthreatsource.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-sensorname](Ps/pC_mcafeenspkvalerttriggersuccesssensorname.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-result](Ps/pC_mcafeenspkvalerttriggersuccessresult.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_mcafee_mcafee_network_security_platform_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  dlp-alert<br> ↳[mcafee-nsp-cef-alert-trigger-success-securitymanager](Ps/pC_mcafeenspcefalerttriggersuccesssecuritymanager.md)<br> ↳[mcafee-nsp-json-alert-trigger-success-threatsource](Ps/pC_mcafeenspjsonalerttriggersuccessthreatsource.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-sensorname](Ps/pC_mcafeenspkvalerttriggersuccesssensorname.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-result](Ps/pC_mcafeenspkvalerttriggersuccessresult.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_mcafee_mcafee_network_security_platform_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  dlp-alert<br> ↳[mcafee-nsp-cef-alert-trigger-success-securitymanager](Ps/pC_mcafeenspcefalerttriggersuccesssecuritymanager.md)<br> ↳[mcafee-nsp-json-alert-trigger-success-threatsource](Ps/pC_mcafeenspjsonalerttriggersuccessthreatsource.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-sensorname](Ps/pC_mcafeenspkvalerttriggersuccesssensorname.md)<br> ↳[mcafee-nsp-kv-alert-trigger-success-result](Ps/pC_mcafeenspkvalerttriggersuccessresult.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_mcafee_mcafee_network_security_platform_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |