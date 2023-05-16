Vendor: Palo Alto Networks
==========================
Product: Traps Endpoint Security Manager
----------------------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  34   |   21   |         5          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Cloud Data Protection](../../../UseCases/uc_cloud_data_protection.md) |  aws-role-assumepolicy<br> ↳[pan-tesm-csv-policy-modify-success-agent](Ps/pC_pantesmcsvpolicymodifysuccessagent.md)<br>    | TA0004 - TA0004<br>    | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_palo_alto_networks_traps_endpoint_security_manager_Cloud_Data_Protection.md) |
|     [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md)     |  dlp-alert<br> ↳[pan-tesm-mix-alert-trigger-success-trapsagent](Ps/pC_pantesmmixalerttriggersuccesstrapsagent.md)<br> ↳[pan-tesm-kv-alert-trigger-success-alerttrigger](Ps/pC_pantesmkvalerttriggersuccessalerttrigger.md)<br> ↳[pan-tesm-str-alert-trigger-success-trapsagent](Ps/pC_pantesmstralerttriggersuccesstrapsagent.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_palo_alto_networks_traps_endpoint_security_manager_Data_Exfiltration.md)   |
|    [Data Leak](../../../UseCases/uc_data_leak.md)    |  dlp-alert<br> ↳[pan-tesm-mix-alert-trigger-success-trapsagent](Ps/pC_pantesmmixalerttriggersuccesstrapsagent.md)<br> ↳[pan-tesm-kv-alert-trigger-success-alerttrigger](Ps/pC_pantesmkvalerttriggersuccessalerttrigger.md)<br> ↳[pan-tesm-str-alert-trigger-success-trapsagent](Ps/pC_pantesmstralerttriggersuccesstrapsagent.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>18 Models</li></ul>](RM/r_m_palo_alto_networks_traps_endpoint_security_manager_Data_Leak.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  dlp-alert<br> ↳[pan-tesm-mix-alert-trigger-success-trapsagent](Ps/pC_pantesmmixalerttriggersuccesstrapsagent.md)<br> ↳[pan-tesm-kv-alert-trigger-success-alerttrigger](Ps/pC_pantesmkvalerttriggersuccessalerttrigger.md)<br> ↳[pan-tesm-str-alert-trigger-success-trapsagent](Ps/pC_pantesmstralerttriggersuccesstrapsagent.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_palo_alto_networks_traps_endpoint_security_manager_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |