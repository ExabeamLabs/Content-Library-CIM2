Vendor: Tufin
=============
Product: Tufin SecureTrack
--------------------------
| Rules | Models | MITRE ATT&CK® TTPs | Activity Types | Parsers |
|:-----:|:------:|:------------------:|:--------------:|:-------:|
|   8   |   8    |         3          |       1        |    1    |

|    Use-Case    | Activity Types/Parsers    | MITRE ATT&CK® TTP    | Content    |
|:----:| ---- | ---- | ---- |
|   [Cloud Data Protection](../../../UseCases/uc_cloud_data_protection.md)   |  aws-role-assumepolicy<br> ↳[tufin-securetrack-kv-policy-modify-saved](Ps/pC_tufinsecuretrackkvpolicymodifysaved.md)<br> | TA0004 - TA0004<br>    | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_tufin_tufin_securetrack_Cloud_Data_Protection.md)   |
| [Compromised Credentials](../../../UseCases/uc_compromised_credentials.md) |  aws-role-assumepolicy<br> ↳[tufin-securetrack-kv-policy-modify-saved](Ps/pC_tufinsecuretrackkvpolicymodifysaved.md)<br> | T1078.004 - Valid Accounts: Cloud Accounts<br>T1535 - Unused/Unsupported Cloud Regions<br> | [<ul><li>6 Rules</li></ul><ul><li>6 Models</li></ul>](RM/r_m_tufin_tufin_securetrack_Compromised_Credentials.md) |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  aws-role-assumepolicy<br> ↳[tufin-securetrack-kv-policy-modify-saved](Ps/pC_tufinsecuretrackkvpolicymodifysaved.md)<br> | TA0004 - TA0004<br>    | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_tufin_tufin_securetrack_Privilege_Escalation.md)    |

MITRE ATT&CK® Framework for Enterprise
--------------------------------------
| Initial Access                                                                                                                                             | Execution | Persistence                                                         | Privilege Escalation                                                | Defense Evasion                                                                                                                                          | Credential Access | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Valid Accounts: Cloud Accounts](https://attack.mitre.org/techniques/T1078/004)<br><br> |           | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Unused/Unsupported Cloud Regions](https://attack.mitre.org/techniques/T1535)<br><br> |                   |           |                  |            |                     |              |        |