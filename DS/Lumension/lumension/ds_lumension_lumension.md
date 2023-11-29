Vendor: Lumension
=================
Product: Lumension
------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  18   |   6    |         3          |       2        |    2    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Data Leak](../../../UseCases/uc_data_leak.md) |  usb-insert<br> ↳[lumension-l-kv-peripheral-storage-insert-success-deviceattached](Ps/pC_lumensionlkvperipheralstorageinsertsuccessdeviceattached.md)<br> ↳[lumension-l-kv-peripheral-storage-insert-success-mediuminserted](Ps/pC_lumensionlkvperipheralstorageinsertsuccessmediuminserted.md)<br> ↳[lumension-l-kv-peripheral-storage-insert-usb](Ps/pC_lumensionlkvperipheralstorageinsertusb.md)<br><br> usb-write<br> ↳[lumension-l-kv-file-write-success-writegranted](Ps/pC_lumensionlkvfilewritesuccesswritegranted.md)<br> | T1052.001 - Exfiltration Over Physical Medium: Exfiltration over USB<br>T1091 - Replication Through Removable Media<br> | [<ul><li>14 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_lumension_lumension_Data_Leak.md) |
|   [Malware](../../../UseCases/uc_malware.md)   |  usb-write<br> ↳[lumension-l-kv-file-write-success-writegranted](Ps/pC_lumensionlkvfilewritesuccesswritegranted.md)<br>    | TA0002 - TA0002<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_lumension_lumension_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                           | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement                                                                         | Collection | Command and Control | Exfiltration                                                                                                                                                                                            | Impact |
| ---------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------------------------------------------------------------------------------- | ---------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| [Replication Through Removable Media](https://attack.mitre.org/techniques/T1091)<br><br> |           |             |                      |                 |                   |           | [Replication Through Removable Media](https://attack.mitre.org/techniques/T1091)<br><br> |            |                     | [Exfiltration Over Physical Medium: Exfiltration over USB](https://attack.mitre.org/techniques/T1052/001)<br><br>[Exfiltration Over Physical Medium](https://attack.mitre.org/techniques/T1052)<br><br> |        |