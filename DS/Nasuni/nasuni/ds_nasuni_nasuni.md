Vendor: Nasuni
==============
Product: Nasuni
---------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|  25   |   13   |         2          |       1        |    1    |

|    Use-Case    | Activity Types (Legacy Event Type)/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  file-permission-modify:success (file-permission-change)<br> ↳[nasuni-n-csv-file-permission-modify-success-setacl](Ps/pC_nasunincsvfilepermissionmodifysuccesssetacl.md)<br> | T1083 - File and Directory Discovery<br> | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_nasuni_nasuni_Compromised_Credentials.md) |
|    [Data Access](../../../UseCases/uc_data_access.md)    |  file-permission-modify:success (file-permission-change)<br> ↳[nasuni-n-csv-file-permission-modify-success-setacl](Ps/pC_nasunincsvfilepermissionmodifysuccesssetacl.md)<br> | T1083 - File and Directory Discovery<br> | [<ul><li>24 Rules</li></ul><ul><li>13 Models</li></ul>](RM/r_m_nasuni_nasuni_Data_Access.md)    |
|         [Privilege Abuse](../../../UseCases/uc_privilege_abuse.md)         |  file-permission-modify:success (file-permission-change)<br> ↳[nasuni-n-csv-file-permission-modify-success-setacl](Ps/pC_nasunincsvfilepermissionmodifysuccesssetacl.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_nasuni_nasuni_Privilege_Abuse.md)    |
|     [Privileged Activity](../../../UseCases/uc_privileged_activity.md)     |  file-permission-modify:success (file-permission-change)<br> ↳[nasuni-n-csv-file-permission-modify-success-setacl](Ps/pC_nasunincsvfilepermissionmodifysuccesssetacl.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul>](RM/r_m_nasuni_nasuni_Privileged_Activity.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                      | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access | Discovery                                                                         | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> |                   | [File and Directory Discovery](https://attack.mitre.org/techniques/T1083)<br><br> |                  |            |                     |              |        |