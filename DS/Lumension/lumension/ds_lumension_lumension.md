Vendor: Lumension
=================
Product: Lumension
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  13   |   4    |         3          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Leak](../../../UseCases/uc_data_leak.md) |  peripheral_device-insert:success (usb-insert)<br> ↳[lumension-l-kv-peripheral-storage-insert-success-mediuminserted](Ps/pC_lumensionlkvperipheralstorageinsertsuccessmediuminserted.md)<br> | T1052 - Exfiltration Over Physical Medium<br>T1052.001 - Exfiltration Over Physical Medium: Exfiltration over USB<br>T1091 - Replication Through Removable Media<br> | [<ul><li>13 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_lumension_lumension_Data_Leak.md) |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                           | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement                                                                         | Collection | Command and Control | Exfiltration                                                                                                                                                                                            | Impact |
| ---------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------------------------------------------------------------------------------- | ---------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Replication Through Removable Media](https://attack.mitre.org/techniques/T1091)<br><br> |           |             |                      |                 |                   |           | [Replication Through Removable Media](https://attack.mitre.org/techniques/T1091)<br><br> |            |                     | [Exfiltration Over Physical Medium: Exfiltration over USB](https://attack.mitre.org/techniques/T1052/001)<br><br>[Exfiltration Over Physical Medium](https://attack.mitre.org/techniques/T1052)<br><br> |        |