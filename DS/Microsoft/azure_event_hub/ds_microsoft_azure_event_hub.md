Vendor: Microsoft
=================
Product: Azure Event Hub
------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  29   |   14   |         4          |       1        |    0    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  file-read<br> ↳[microsoft-azureeh-csv-alert-trigger-security](Ps/pC_microsoftazureehcsvalerttriggersecurity.md)<br> | T1003.001 - T1003.001<br>T1003.003 - T1003.003<br>T1083 - File and Directory Discovery<br> | [<ul><li>28 Rules</li></ul><ul><li>14 Models</li></ul>](RM/r_m_microsoft_azure_event_hub_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  file-read<br> ↳[microsoft-azureeh-csv-alert-trigger-security](Ps/pC_microsoftazureehcsvalerttriggersecurity.md)<br> | T1083 - File and Directory Discovery<br>    | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_microsoft_azure_event_hub_Data_Access.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  file-read<br> ↳[microsoft-azureeh-csv-alert-trigger-security](Ps/pC_microsoftazureehcsvalerttriggersecurity.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_azure_event_hub_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  file-read<br> ↳[microsoft-azureeh-csv-alert-trigger-security](Ps/pC_microsoftazureehcsvalerttriggersecurity.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_microsoft_azure_event_hub_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                          | Discovery                                                                         | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [OS Credential Dumping](https://attack.mitre.org/techniques/T1003)<br><br> | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  |            |                     |              |        |