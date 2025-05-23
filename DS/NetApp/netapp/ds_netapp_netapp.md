Vendor: NetApp
==============
Product: NetApp
---------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  27   |   13   |         6          |       2        |    3    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  file-delete:success (file-delete)<br> ↳[netapp-n-xml-file-delete-success-4660](Ps/pC_netappnxmlfiledeletesuccess4660.md)<br>    | T1083 - File and Directory Discovery<br>    | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_netapp_netapp_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  file-delete:success (file-delete)<br> ↳[netapp-n-xml-file-delete-success-4660](Ps/pC_netappnxmlfiledeletesuccess4660.md)<br>    | T1083 - File and Directory Discovery<br>    | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_netapp_netapp_Data_Access.md)    |
|     [Destruction of Data](../../../UseCases/uc_destruction_of_data.md)     |  file-delete:success (file-delete)<br> ↳[netapp-n-xml-file-delete-success-4660](Ps/pC_netappnxmlfiledeletesuccess4660.md)<br>    | T1070 - Indicator Removal on Host<br>T1070.004 - Indicator Removal on Host: File Deletion<br>T1485 - Data Destruction<br> | [<ul><li>1 Rules</li></ul>](RM/r_m_netapp_netapp_Destruction_of_Data.md)    |
|        [Lateral Movement](../../../UseCases/uc_lateral_movement.md)        |  endpoint-logout:success (logout-remote)<br> ↳[microsoft-evsecurity-json-endpoint-logout-success-4634](Ps/pC_microsoftevsecurityjsonendpointlogoutsuccess4634.md)<br> ↳[microsoft-evsecurity-json-endpoint-endpoint-logout-success-userinitiatedlogoff](Ps/pC_microsoftevsecurityjsonendpointendpointlogoutsuccessuserinitiatedlogoff.md)<br> | T1210 - Exploitation of Remote Services<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_netapp_netapp_Lateral_Movement.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  file-delete:success (file-delete)<br> ↳[netapp-n-xml-file-delete-success-4660](Ps/pC_netappnxmlfiledeletesuccess4660.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_netapp_netapp_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  file-delete:success (file-delete)<br> ↳[netapp-n-xml-file-delete-success-4660](Ps/pC_netappnxmlfiledeletesuccess4660.md)<br>    | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_netapp_netapp_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                                                                                                                                                                                                    | Credential Access | Discovery                                                                         | Lateral Movement                                                                     | Collection | Command and Control | Exfiltration | Impact                                                                |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ | ---------- | ------------------- | ------------ | --------------------------------------------------------------------- |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Indicator Removal on Host: File Deletion](https://attack.mitre.org/techniques/T1070/004)<br><br>[Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Indicator Removal on Host](https://attack.mitre.org/techniques/T1070)<br><br> |                   | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> | [Exploitation of Remote Services](https://attack.mitre.org/techniques/T1210)<br><br> |            |                     |              | [Data Destruction](https://attack.mitre.org/techniques/T1485)<br><br> |