Vendor: AMD
===========
Product: Pensando
-----------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  66   |   25   |         6          |       3        |    3    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  database-login<br> ↳[amd-p-csv-network-notification-success-flowdelete](Ps/pC_amdpcsvnetworknotificationsuccessflowdelete.md)<br>    | T1213 - Data from Information Repositories<br>    | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_amd_pensando_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  database-login<br> ↳[amd-p-csv-network-notification-success-flowdelete](Ps/pC_amdpcsvnetworknotificationsuccessflowdelete.md)<br>    | T1213 - Data from Information Repositories<br>    | [<ul><li>10 Rules</li></ul><ul><li>5 Models</li></ul>](RM/r_m_amd_pensando_Data_Access.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  network-connection-failed<br> ↳[amd-p-csv-network-session-flowcreate](Ps/pC_amdpcsvnetworksessionflowcreate.md)<br><br> network-connection-successful<br> ↳[amd-p-csv-network-session-flowcreate](Ps/pC_amdpcsvnetworksessionflowcreate.md)<br> | T1071 - Application Layer Protocol<br>T1090.003 - Proxy: Multi-hop Proxy<br>T1190 - Exploit Public Fasing Application<br>TA0010 - TA0010<br>TA0011 - TA0011<br> | [<ul><li>56 Rules</li></ul><ul><li>20 Models</li></ul>](RM/r_m_amd_pensando_Lateral_Movement.md)       |
|    [Malware](../../../UseCases/uc_malware.md)    |  network-connection-failed<br> ↳[amd-p-csv-network-session-flowcreate](Ps/pC_amdpcsvnetworksessionflowcreate.md)<br><br> network-connection-successful<br> ↳[amd-p-csv-network-session-flowcreate](Ps/pC_amdpcsvnetworksessionflowcreate.md)<br> | TA0011 - TA0011<br>    | [<ul><li>4 Rules</li></ul>](RM/r_m_amd_pensando_Malware.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                         | Execution | Persistence | Privilege Escalation | Defense Evasion | Credential Access | Discovery | Lateral Movement | Collection                                                                              | Command and Control                                                                                                                                                                                                      | Exfiltration | Impact |
| -------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- | --------------- | ----------------- | --------- | ---------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | ------ |
| [Exploit Public Fasing Application](https://attack.mitre.org/techniques/T1190)<br><br> |           |             |                      |                 |                   |           |                  | [Data from Information Repositories](https://attack.mitre.org/techniques/T1213)<br><br> | [Proxy: Multi-hop Proxy](https://attack.mitre.org/techniques/T1090/003)<br><br>[Application Layer Protocol](https://attack.mitre.org/techniques/T1071)<br><br>[Proxy](https://attack.mitre.org/techniques/T1090)<br><br> |              |        |