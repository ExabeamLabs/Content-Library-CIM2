Vendor: Trellix
===============
Product: Trellix DLP Endpoint
-----------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  33   |   19   |         4          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Exfiltration](../../../UseCases/uc_data_exfiltration.md) |  alert-trigger:success (dlp-alert)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_trellix_trellix_dlp_endpoint_Data_Exfiltration.md) |
|         [Data Leak](../../../UseCases/uc_data_leak.md)         |  alert-trigger:success (dlp-alert)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> | T1020 - Automated Exfiltration<br>T1071 - Application Layer Protocol<br>TA0010 - TA0010<br> | [<ul><li>29 Rules</li></ul><ul><li>17 Models</li></ul>](RM/r_m_trellix_trellix_dlp_endpoint_Data_Leak.md)         |
|    [Malware](../../../UseCases/uc_malware.md)    |  alert-trigger:success (dlp-alert)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> ↳[mcafee-dlp-kv-alert-trigger-success-lossprevention](Ps/pC_mcafeedlpkvalerttriggersuccesslossprevention.md)<br> | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_trellix_trellix_dlp_endpoint_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection | Command and Control                                                             | Exfiltration                                                                | Impact |
| -------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | ---------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------ |
|                |           |             |                      |                 |                   |           |                  |            | [Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br> | [Automated Exfiltration](https://attack.mitre.org/techniques/T1020)<br><br> |        |